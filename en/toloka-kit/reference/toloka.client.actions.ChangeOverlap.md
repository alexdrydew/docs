# ChangeOverlap
`toloka.client.actions.ChangeOverlap` | [Source code](https://github.com/Toloka/toloka-kit/blob/v1.0.1/src/client/actions.py#L131)

```python
ChangeOverlap(
    self,
    *,
    delta: Optional[int] = None,
    open_pool: Optional[bool] = None
)
```

Increases the overlap of a task.


You can use this rule only with [UsersAssessment](https://toloka.ai/en/docs/toloka-kit/reference/toloka.client.collectors.UsersAssessment) and [AssignmentsAssessment](https://toloka.ai/en/docs/toloka-kit/reference/toloka.client.collectors.AssignmentsAssessment) collectors.  # noqa: E501

## Parameters Description

| Parameters | Type | Description |
| :----------| :----| :-----------|
`delta`|**Optional\[int\]**|<p>An overlap increment.</p>
`open_pool`|**Optional\[bool\]**|<p><ul><li>`True` — Open the pool after changing the overlap value.</li><li>`False` — Don&#x27;t reopen the pool if it is closed.</li></ul></p>

**Examples:**

The example shows how to increase task overlap when you reject assignments.

```python
new_pool = toloka.pool.Pool(....)
new_pool.quality_control.add_action(
    collector=toloka.collectors.AssignmentsAssessment(),
    conditions=[toloka.conditions.AssessmentEvent == toloka.conditions.AssessmentEvent.REJECT],
    action=toloka.actions.ChangeOverlap(delta=1, open_pool=True),
)
```
