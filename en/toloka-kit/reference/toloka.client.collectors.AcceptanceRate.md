# AcceptanceRate
`toloka.client.collectors.AcceptanceRate` | [Source code](https://github.com/Toloka/toloka-kit/blob/v1.0.1/src/client/collectors.py#L62)

```python
AcceptanceRate(
    self,
    *,
    uuid: Optional[UUID] = None,
    history_size: Optional[int] = None
)
```

Results of checking the answers of the Toloker.


If non-automatic acceptance (assignment review) is set in the pool, add a rule to:
- Set the Toloker's skill based on their responses.
- Block access for Tolokers who give incorrect responses.

Used with conditions:
* TotalAssignmentsCount - How many assignments from this Toloker were checked.
* AcceptedAssignmentsRate - Percentage of how many assignments were accepted from this Toloker out of all checked assignment.
* RejectedAssignmentsRate - Percentage of how many assignments were rejected from this Toloker out of all checked assignment.

Used with actions:
* RestrictionV2 - Block access to projects or pools.
* ApproveAllAssignments - Approve all replies from the Toloker.
* RejectAllAssignments - Reject all replies from the Toloker.
* SetSkill - Set Toloker's skill value.
* SetSkillFromOutputField - Set Toloker's skill value from source.

## Parameters Description

| Parameters | Type | Description |
| :----------| :----| :-----------|
`history_size`|**Optional\[int\]**|<p>The maximum number of recent tasks that the Toloker completed in the project to use for the calculation. If this field is omitted, the calculation is based on all the tasks that the Toloker completed in the pool.</p>

**Examples:**

How to ban a Toloker in this project if he makes mistakes.

```python
new_pool = toloka.pool.Pool(....)
new_pool.quality_control.add_action(
collector=toloka.collectors.AcceptanceRate(),
    conditions=[
        toloka.conditions.TotalAssignmentsCount > 2,
        toloka.conditions.RejectedAssignmentsRate > 35,
    ],
    action=toloka.actions.RestrictionV2(
        scope=toloka.user_restriction.UserRestriction.PROJECT,
        duration=15,
        duration_unit='DAYS',
        private_comment='The Toloker often makes mistakes',
    )
)
```
