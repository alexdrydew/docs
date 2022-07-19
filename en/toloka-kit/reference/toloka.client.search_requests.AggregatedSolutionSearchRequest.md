# AggregatedSolutionSearchRequest
`toloka.client.search_requests.AggregatedSolutionSearchRequest` | [Source code](https://github.com/Toloka/toloka-kit/blob/v1.0.1/src/client/search_requests.py#L494)

```python
AggregatedSolutionSearchRequest(
    self,
    task_id_lt: Optional[str] = None,
    task_id_lte: Optional[str] = None,
    task_id_gt: Optional[str] = None,
    task_id_gte: Optional[str] = None
)
```

Parameters for filtering aggregated responses.

## Parameters Description

| Parameters | Type | Description |
| :----------| :----| :-----------|
`task_id_lt`|**Optional\[str\]**|<p>Tasks with an ID less than the specified value.</p>
`task_id_lte`|**Optional\[str\]**|<p>Tasks with an ID less than or equal to the specified value.</p>
`task_id_gt`|**Optional\[str\]**|<p>Tasks with an ID greater than the specified value.</p>
`task_id_gte`|**Optional\[str\]**|<p>Tasks with an ID greater than or equal to the specified value.</p>
