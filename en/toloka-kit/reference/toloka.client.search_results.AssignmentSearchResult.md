# AssignmentSearchResult
`toloka.client.search_results.AssignmentSearchResult`

```python
AssignmentSearchResult(
    self,
    *,
    items: Optional[List[Assignment]] = None,
    has_more: Optional[bool] = None
)
```

The list of found assignments.


The number of assignments in the list is limited by the [find_assignments](toloka.client.TolokaClient.find_assignments.md) method.

## Parameters Description

| Parameters | Type | Description |
| :----------| :----| :-----------|
`items`|**Optional\[List\[[Assignment](toloka.client.assignment.Assignment.md)\]\]**|<p>The list of found assignments.</p>
`has_more`|**Optional\[bool\]**|<p>More items flag:<ul><li>`True` — Not all assignments matching search criteria are returned in the `items` due to the limit.</li><li>`False` — All matching assignments are in the `items`.</li></ul></p>
