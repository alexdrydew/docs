# AssignmentSubmitTime
`toloka.client.collectors.AssignmentSubmitTime` | [Source code](https://github.com/Toloka/toloka-kit/blob/v1.0.1/src/client/collectors.py#L192)

```python
AssignmentSubmitTime(
    self,
    *,
    uuid: Optional[UUID] = None,
    fast_submit_threshold_seconds: Optional[int] = None,
    history_size: Optional[int] = None
)
```

Filtering cheating Tolokers who respond too quickly


Helpful when you need to:
- Use this Restrict the pool access for Tolokers who respond too quickly.
- Provide protection from robots.

Used with conditions:
* TotalSubmittedCount - The number of assignments a specific Toloker completed.
* FastSubmittedCount - The number of assignments a specific Toloker completed too fast.

Used with actions:
* RestrictionV2 - Block access to projects or pools.
* ApproveAllAssignments - Approve all replies from the Toloker.
* RejectAllAssignments - Reject all replies from the Toloker.
* SetSkill - Set Toloker's skill value.

## Parameters Description

| Parameters | Type | Description |
| :----------| :----| :-----------|
`fast_submit_threshold_seconds`|**Optional\[int\]**|<p>The task suite completion time (in seconds). Everything that is completed faster is considered a fast response.</p>
`history_size`|**Optional\[int\]**|<p>The number of the recent task suites completed by the Toloker.</p>

**Examples:**

How to reject all assignments if Toloker sends answers too fast.

```python
new_pool = toloka.pool.Pool(....)
new_pool.quality_control.add_action(
    collector=toloka.collectors.AssignmentSubmitTime(history_size=5, fast_submit_threshold_seconds=20),
    conditions=[toloka.conditions.FastSubmittedCount > 3],
    action=toloka.actions.RejectAllAssignments(public_comment='Too fast answering. You are cheater!')
)
```
