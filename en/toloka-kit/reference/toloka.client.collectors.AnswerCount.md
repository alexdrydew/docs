# AnswerCount
`toloka.client.collectors.AnswerCount` | [Source code](https://github.com/Toloka/toloka-kit/blob/v1.0.1/src/client/collectors.py#L116)

```python
AnswerCount(self, *, uuid: Optional[UUID] = None)
```

How many assignments were accepted from a Toloker.


Use this rule if you want to:
- Get responses from as many Tolokers as possible (for this purpose, set a low threshold, such as one task suite).
- Protect yourself from robots (for this purpose, the threshold should be higher, such as 10% of the pool's tasks).
- Mark Tolokers completing a task so that you can filter them later in the checking project.

Used with conditions:
* AssignmentsAcceptedCount - How many assignments were accepted from a Toloker.

Used with actions:
* RestrictionV2 - Block access to projects or pools.
* ApproveAllAssignments - Approve all replies from the Toloker.
* RejectAllAssignments - Reject all replies from the Toloker.
* SetSkill - Set Toloker's skill value.


**Examples:**

How to mark Tolokers completing a task so that you can filter them later in the checking project.

```python
new_pool = toloka.pool.Pool(....)
new_pool.quality_control.add_action(
    collector=toloka.collectors.AnswerCount(),
    conditions=[toloka.conditions.AssignmentsAcceptedCount > 0],
    action=toloka.actions.SetSkill(skill_id=some_skill_id, skill_value=1),
)
```
