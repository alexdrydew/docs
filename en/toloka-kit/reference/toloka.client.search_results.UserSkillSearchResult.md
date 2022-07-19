# UserSkillSearchResult
`toloka.client.search_results.UserSkillSearchResult`

```python
UserSkillSearchResult(
    self,
    *,
    items: Optional[List[UserSkill]] = None,
    has_more: Optional[bool] = None
)
```

The list of found Toloker skills and whether there is something else on the original request


It's better to use TolokaClient.get_user_skills(), which already implements the correct handling of the search result.

## Parameters Description

| Parameters | Type | Description |
| :----------| :----| :-----------|
`items`|**Optional\[List\[[UserSkill](toloka.client.user_skill.UserSkill.md)\]\]**|<p>List of found Toloker skills</p>
`has_more`|**Optional\[bool\]**|<p>Whether the list is complete:<ul><li>True - Not all elements are included in the output due to restrictions in the limit parameter.</li><li>False - The output lists all the items.</li></ul></p>
