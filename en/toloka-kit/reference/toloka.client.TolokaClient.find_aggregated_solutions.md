# find_aggregated_solutions
`toloka.client.TolokaClient.find_aggregated_solutions`

Gets aggregated responses from Toloka that match certain criteria.


Pass to the `find_aggregated_solutions` the ID of the operation started by the [aggregate_solutions_by_pool](toloka.client.TolokaClient.aggregate_solutions_by_pool.md) method.

The number of returned aggregated responses is limited. To find remaining matching responses, call `find_aggregated_solutions` with updated filter criteria.

To iterate over all aggregated responses in one call use [get_aggregated_solutions](toloka.client.TolokaClient.get_aggregated_solutions.md).

## Parameters Description

| Parameters | Type | Description |
| :----------| :----| :-----------|
`operation_id`|**str**|<p>The ID of the aggregation operation.</p>
`task_id_lt`|**Optional\[str\]**|<p>Tasks with an ID less than the specified value.</p>
`task_id_lte`|**Optional\[str\]**|<p>Tasks with an ID less than or equal to the specified value.</p>
`task_id_gt`|**Optional\[str\]**|<p>Tasks with an ID greater than the specified value.</p>
`task_id_gte`|**Optional\[str\]**|<p>Tasks with an ID greater than or equal to the specified value.</p>
`sort`|**Union\[List\[str\], [AggregatedSolutionSortItems](toloka.client.search_requests.AggregatedSolutionSortItems.md), None\]**|<p>Sorting options. </p><p>Default value: `None`.</p>
`limit`|**Optional\[int\]**|<p>Returned aggregated responses limit. The maximum value is 100,000. </p><p>Default value: 50.</p>

* **Returns:**

  Found responses and a flag showing whether there are more matching responses.

* **Return type:**

  [AggregatedSolutionSearchResult](toloka.client.search_results.AggregatedSolutionSearchResult.md)

**Examples:**

The example shows how to get all aggregated responses using the `find_aggregated_solutions` method.

```python
current_result = toloka_client.find_aggregated_solutions(aggregation_operation.id)
aggregation_results = current_result.items
while current_result.has_more:
    current_result = toloka_client.find_aggregated_solutions(
        aggregation_operation.id,
        task_id_gt=current_result.items[-1].task_id,
    )
    aggregation_results = aggregation_results + current_result.items
print(len(aggregation_results))
```
