# GoldenSet
`toloka.client.collectors.GoldenSet` | [Source code](https://github.com/Toloka/toloka-kit/blob/v1.0.1/src/client/collectors.py#L286)

```python
GoldenSet(
    self,
    *,
    uuid: Optional[UUID] = None,
    history_size: Optional[int] = None
)
```

How Toloker answers on control tasks


Use control tasks to assign a skill to Tolokers based on their responses and ban Tolokers who submit incorrect responses.

Don't use it if:
- You have a lot of response options.
- Tolokers need to attach a file to their assignment.
- Tolokers need to transcribe text.
- Tolokers need to select objects in a photo.
- Tasks don't have a correct or incorrect response. For example: "Which image do you like best?" or
"Choose the page design option that you like best".

Used with conditions:
* TotalAnswersCount - The number of completed control and training tasks.
* CorrectAnswersRate - The percentage of correct responses in training and control tasks.
* IncorrectAnswersRate - The percentage of incorrect responses in training and control tasks.
* GoldenSetAnswersCount - The number of completed control tasks
* GoldenSetCorrectAnswersRate - The percentage of correct responses in control tasks.
* GoldenSetIncorrectAnswersRate - The percentage of incorrect responses in control tasks.

Used with actions:
* RestrictionV2 - Block access to projects or pools.
* ApproveAllAssignments - Approve all replies from the Toloker.
* RejectAllAssignments - Reject all replies from the Toloker.
* SetSkill - Set Toloker's skill value.
* SetSkillFromOutputField - Set Toloker's skill value from source.

## Parameters Description

| Parameters | Type | Description |
| :----------| :----| :-----------|
`history_size`|**Optional\[int\]**|<p>The number of the Toloker&#x27;s last responses to control tasks.</p>

**Examples:**

How to approve all assignments if the Toloker gives correct answers in control tasks.

```python
new_pool = toloka.pool.Pool(....)
new_pool.quality_control.add_action(
    collector=toloka.collectors.GoldenSet(history_size=5),
    conditions=[toloka.conditions.GoldenSetCorrectAnswersRate > 90],
    action=toloka.actions.ApproveAllAssignments()
)
```
