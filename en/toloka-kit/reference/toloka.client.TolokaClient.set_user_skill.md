# set_user_skill
`toloka.client.TolokaClient.set_user_skill`

Assigns a skill to a Toloker.

## Parameters Description

| Parameters | Type | Description |
| :----------| :----| :-----------|
`skill_id`|**Optional\[str\]**|<p>Skill ID. What skill to set.</p>
`user_id`|**Optional\[str\]**|<p>Toloker&#x27;s ID.</p>
`value`|**Optional\[Decimal\]**|<p>Fractional value of the skill. Minimum - 0, maximum - 100.</p>

* **Returns:**

  Updated skill information.

* **Return type:**

  [UserSkill](toloka.client.user_skill.UserSkill.md)

**Examples:**

```python
from decimal import *
toloka_client.set_user_skill(skill_id='1', user_id='1', value=Decimal(100))
```
