# TaskOverlapPatch
`toloka.client.task.TaskOverlapPatch` | [Source code](https://github.com/Toloka/toloka-kit/blob/v1.0.1/src/client/task.py#L154)

```python
TaskOverlapPatch(
    self,
    *,
    overlap: Optional[int] = None,
    infinite_overlap: Optional[bool] = None
)
```

Parameters for changing the overlap of a specific Task

## Parameters Description

| Parameters | Type | Description |
| :----------| :----| :-----------|
`overlap`|**Optional\[int\]**|<p>Overlap value.</p>
`infinite_overlap`|**Optional\[bool\]**|<p>Infinite overlap:<ul><li>True — Assign the task to all Tolokers. It is useful for training tasks.</li><li>False — Overlap value specified for the task or for the pool is used. </li></ul></p><p>Default value: False.</p>
