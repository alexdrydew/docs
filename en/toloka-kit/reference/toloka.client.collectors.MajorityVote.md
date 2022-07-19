# MajorityVote
`toloka.client.collectors.MajorityVote` | [Source code](https://github.com/Toloka/toloka-kit/blob/v1.0.1/src/client/collectors.py#L381)

```python
MajorityVote(
    self,
    *,
    uuid: Optional[UUID] = None,
    answer_threshold: Optional[int] = None,
    history_size: Optional[int] = None
)
```

Majority vote is a quality control method based on coinciding responses from the majority


The response chosen by the majority is considered correct, and other responses are considered incorrect.
Depending on the percentage of correct responses, you can either increase the Toloker's skill value, or ban the Toloker.

Used with conditions:
* TotalAnswersCount - The number of completed tasks by the Toloker.
* CorrectAnswersRate - The percentage of correct responses.
* IncorrectAnswersRate - The percentage of incorrect responses.

Used with actions:
* RestrictionV2 - Block access to projects or pools.
* ApproveAllAssignments - Approve all replies from the Toloker.
* RejectAllAssignments - Reject all replies from the Toloker.
* SetSkill - Set Toloker's skill value.
* SetSkillFromOutputField - Set Toloker's skill value from source.

## Parameters Description

| Parameters | Type | Description |
| :----------| :----| :-----------|
`answer_threshold`|**Optional\[int\]**|<p>The number of Tolokers considered the majority (for example, 3 out of 5).</p>
`history_size`|**Optional\[int\]**|<p>The maximum number of the Toloker&#x27;s recent responses in the project to use for calculating the percentage of correct responses. If this field is omitted, the calculation is based on all the Toloker&#x27;s responses in the pool.</p>

**Examples:**

How to ban a Toloker in this project if he made enough answers (only for pools with post acceptance).

```python
new_pool = toloka.pool.Pool(....)
new_pool.quality_control.add_action(
    collector=toloka.collectors.MajorityVote(answer_threshold=2),
    conditions=[
        toloka.conditions.TotalAnswersCount > 9,
        toloka.conditions.CorrectAnswersRate < 60,
    ],
    action=toloka.actions.RejectAllAssignments(public_comment='Too low quality')
)
```
