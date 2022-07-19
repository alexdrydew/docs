# PoolAggregatedSolutionRequest
`toloka.client.aggregation.PoolAggregatedSolutionRequest` | [Source code](https://github.com/Toloka/toloka-kit/blob/v1.0.1/src/client/aggregation.py#L31)

```python
PoolAggregatedSolutionRequest(
    self,
    *,
    type: Union[AggregatedSolutionType, str, None] = None,
    pool_id: Optional[str] = None,
    answer_weight_skill_id: Optional[str] = None,
    fields: Optional[List[Field]] = None
)
```

Parameters for aggregating results in a pool using the [aggregate_solutions_by_pool](toloka.client.TolokaClient.aggregate_solutions_by_pool.md) method.

## Parameters Description

| Parameters | Type | Description |
| :----------| :----| :-----------|
`type`|**Optional\[[AggregatedSolutionType](toloka.client.aggregation.AggregatedSolutionType.md)\]**|<p>Aggregation model:<ul><li>`WEIGHTED_DYNAMIC_OVERLAP` — [Aggregation](https://toloka.ai/docs/guide/concepts/result-aggregation.html#aggr__aggr-by-skill) based on Tolokers&#x27; skill in a pool with a dynamic overlap.</li><li>`DAWID_SKENE` — [Dawid-Skene aggregation model](https://toloka.ai/docs/guide/concepts/result-aggregation.html#aggr__dawid-skene). It is used in pools without a dynamic overlap.</li></ul></p>
`pool_id`|**Optional\[str\]**|<p>The ID of the pool.</p>
`answer_weight_skill_id`|**Optional\[str\]**|<p>The ID of the skill that determines the weight of the Toloker&#x27;s responses.</p>
`fields`|**Optional\[List\[[Field](toloka.client.aggregation.PoolAggregatedSolutionRequest.Field.md)\]\]**|<p>Output data fields to aggregate. For the best results, each of these fields should have limited number of response options.</p>
