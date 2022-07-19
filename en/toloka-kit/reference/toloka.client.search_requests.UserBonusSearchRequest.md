# UserBonusSearchRequest
`toloka.client.search_requests.UserBonusSearchRequest` | [Source code](https://github.com/Toloka/toloka-kit/blob/v1.0.1/src/client/search_requests.py#L794)

```python
UserBonusSearchRequest(
    self,
    user_id: Optional[str] = None,
    assignment_id: Optional[str] = None,
    private_comment: Optional[str] = None,
    id_lt: Optional[str] = None,
    id_lte: Optional[str] = None,
    id_gt: Optional[str] = None,
    id_gte: Optional[str] = None,
    created_lt: Optional[datetime] = None,
    created_lte: Optional[datetime] = None,
    created_gt: Optional[datetime] = None,
    created_gte: Optional[datetime] = None
)
```

Parameters for searching `UserBonus` instances.

## Parameters Description

| Parameters | Type | Description |
| :----------| :----| :-----------|
`user_id`|**Optional\[str\]**|<p>The ID of the Toloker.</p>
`assignment_id`|**Optional\[str\]**|<p>The ID of the Toloker&#x27;s response to the task a reward is issued for.</p>
`private_comment`|**Optional\[str\]**|<p>Comments for the requester.</p>
`id_lt`|**Optional\[str\]**|<p>Bonuses with an ID less than the specified value.</p>
`id_lte`|**Optional\[str\]**|<p>Bonuses with an ID less than or equal to the specified value.</p>
`id_gt`|**Optional\[str\]**|<p>Bonuses with an ID greater than the specified value.</p>
`id_gte`|**Optional\[str\]**|<p>Bonuses with an ID greater than or equal to the specified value.</p>
`created_lt`|**Optional\[datetime\]**|<p>Bonuses awarded before the specified date.</p>
`created_lte`|**Optional\[datetime\]**|<p>Bonuses awarded before or on the specified date.</p>
`created_gt`|**Optional\[datetime\]**|<p>Bonuses awarded after the specified date.</p>
`created_gte`|**Optional\[datetime\]**|<p>Bonuses awarded after or on the specified date.</p>
