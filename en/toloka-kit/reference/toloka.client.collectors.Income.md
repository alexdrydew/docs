# Income
`toloka.client.collectors.Income` | [Source code](https://github.com/Toloka/toloka-kit/blob/v1.0.1/src/client/collectors.py#L343)

```python
Income(self, *, uuid: Optional[UUID] = None)
```

Limit the Toloker's daily earnings in the pool


Helpful when you need to:
- Get responses from as many Tolokers as possible.

Used with conditions:
* IncomeSumForLast24Hours - The Toloker earnings for completed tasks in the pool over the last 24 hours.

Used with actions:
* RestrictionV2 - Block access to projects or pools.
* ApproveAllAssignments - Approve all replies from the Toloker.
* RejectAllAssignments - Reject all replies from the Toloker.
* SetSkill - Set Toloker's skill value.


**Examples:**

How to ban a Toloker in this project if he made enough answers.

```python
new_pool = toloka.pool.Pool(....)
new_pool.quality_control.add_action(
    collector=toloka.collectors.Income(),
    conditions=[toloka.conditions.IncomeSumForLast24Hours > 1],
    action=toloka.actions.RestrictionV2(
        scope=toloka.user_restriction.UserRestriction.PROJECT,
        duration=15,
        duration_unit='DAYS',
        private_comment='Answer limit is reached',
    )
)
```
