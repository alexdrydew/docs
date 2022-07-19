# TaskSuitePatch
`toloka.client.task_suite.TaskSuitePatch` | [Source code](https://github.com/Toloka/toloka-kit/blob/v1.0.1/src/client/task_suite.py#L111)

```python
TaskSuitePatch(
    self,
    *,
    infinite_overlap=None,
    overlap=None,
    issuing_order_override: Optional[float] = None,
    open_pool: Optional[bool] = None
)
```

Parameters for changing specific TaskSuite

## Parameters Description

| Parameters | Type | Description |
| :----------| :----| :-----------|
`issuing_order_override`|**Optional\[float\]**|<p>The priority of a task suite among other sets in the pool. Defines the order in which task suites are assigned to Tolokers. The larger the parameter value, the higher the priority. This parameter can be used if the pool has issue_task_suites_in_creation_order: true. Allowed values: from -99999.99999 to 99999.99999.</p>
`open_pool`|**Optional\[bool\]**|<p>Open the pool immediately after changing a task suite, if the pool is closed.</p>
