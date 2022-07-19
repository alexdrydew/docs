# Captcha
`toloka.client.collectors.Captcha` | [Source code](https://github.com/Toloka/toloka-kit/blob/v1.0.1/src/client/collectors.py#L237)

```python
Captcha(
    self,
    *,
    uuid: Optional[UUID] = None,
    history_size: Optional[int] = None
)
```

Captchas provide a high level of protection from robots


Used with conditions:
* StoredResultsCount - How many times the Toloker entered captcha.
* SuccessRate - Percentage of correct answers of the Toloker to the captcha.
* FailRate - Percentage of wrong answers of the Toloker to the captcha.

Used with actions:
* RestrictionV2 - Block access to projects or pools.
* ApproveAllAssignments - Approve all replies from the Toloker.
* RejectAllAssignments - Reject all replies from the Toloker.
* SetSkill - Set Toloker's skill value.
* SetSkillFromOutputField - Set Toloker's skill value from source.

## Parameters Description

| Parameters | Type | Description |
| :----------| :----| :-----------|
`history_size`|**Optional\[int\]**|<p>The number of times the Toloker was shown a captcha recently.</p>

**Examples:**

How to ban a Toloker in this project if he mistakes in captcha.

```python
new_pool = toloka.pool.Pool(....)
new_pool.set_captcha_frequency('MEDIUM')
new_pool.quality_control.add_action(
collector=toloka.collectors.Captcha(history_size=5),
    conditions=[
        toloka.conditions.SuccessRate < 60,
    ],
    action=toloka.actions.RestrictionV2(
        scope=toloka.user_restriction.UserRestriction.PROJECT,
        duration=15,
        duration_unit='DAYS',
        private_comment='Toloker often makes mistakes in captcha',
    )
)
```
