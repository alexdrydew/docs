# UsersAssessment
`toloka.client.collectors.UsersAssessment` | [Source code](https://github.com/Toloka/toloka-kit/blob/v1.0.1/src/client/collectors.py#L483)

```python
UsersAssessment(self, *, uuid: Optional[UUID] = None)
```

Recompletion of assignments from banned Tolokers


If you or the system banned a Toloker and you want someone else to complete their tasks.
This rule will help you do this automatically.

Used with conditions:
* PoolAccessRevokedReason - Reason for loss of access of the Toloker to the current pool.
* SkillId - The Toloker no longer meets the specific skill filter.

Used with actions:
* ChangeOverlap - Increase the overlap of the set of tasks.


**Examples:**

How to resend rejected assignments for re-completion to other Tolokers.

```python
new_pool = toloka.pool.Pool(....)
new_pool.quality_control.add_action(
    collector=toloka.collectors.UsersAssessment(),
    conditions=[toloka.conditions.PoolAccessRevokedReason == toloka.conditions.PoolAccessRevokedReason.RESTRICTION],
    action=toloka.actions.ChangeOverlap(delta=1, open_pool=True),
)
```
