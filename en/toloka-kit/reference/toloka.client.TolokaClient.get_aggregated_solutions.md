# get_aggregated_solutions
`toloka.client.TolokaClient.get_aggregated_solutions`

Returns a generator that allows you to iterate over all aggregated responses.


Pass to the `get_aggregated_solutions` the ID of the operation started by the [aggregate_solutions_by_pool](toloka.client.TolokaClient.aggregate_solutions_by_pool.md) method.
Use the returned generator to iterate over aggregated responses.
Note that several calls to the Toloka API may be done while iterating.

{% note tip %}

Try [crowd-kit library](https://toloka.ai/en/docs/crowd-kit). It has many aggregation methods and executes on your computer.

{% endnote %}

## Parameters Description

| Parameters | Type | Description |
| :----------| :----| :-----------|
`operation_id`|**str**|<p>The ID of the aggregation operation.</p>
`task_id_lt`|**Optional\[str\]**|<p>Tasks with an ID less than the specified value.</p>
`task_id_lte`|**Optional\[str\]**|<p>Tasks with an ID less than or equal to the specified value.</p>
`task_id_gt`|**Optional\[str\]**|<p>Tasks with an ID greater than the specified value.</p>
`task_id_gte`|**Optional\[str\]**|<p>Tasks with an ID greater than or equal to the specified value.</p>

* **Yields:**

  The next aggregated response matching the filter parameters.

* **Yield type:**

  Generator\[[AggregatedSolution](toloka.client.aggregation.AggregatedSolution.md), None, None\]

**Examples:**

The example shows how to aggregate responses in a pool.

```python
aggregation_operation = toloka_client.aggregate_solutions_by_pool(
        type=toloka.aggregation.AggregatedSolutionType.WEIGHTED_DYNAMIC_OVERLAP,
        pool_id=some_existing_pool_id,
        answer_weight_skill_id=some_skill_id,
        fields=[toloka.aggregation.PoolAggregatedSolutionRequest.Field(name='result')]
    )
aggregation_operation = toloka_client.wait_operation(aggregation_operation)
aggregation_results = list(toloka_client.get_aggregated_solutions(aggregation_operation.id))
```
