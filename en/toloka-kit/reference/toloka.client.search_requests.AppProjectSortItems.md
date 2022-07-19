# AppProjectSortItems
`toloka.client.search_requests.AppProjectSortItems`

```python
AppProjectSortItems(self, items=None)
```

Keys for sorting App projects in search results.


You can specify multiple keys separated by a comma. To sort in descending order, add the `-` sign before a key.
Example: `sort='-created,id'`.

## Parameters Description

| Parameters | Type | Description |
| :----------| :----| :-----------|
`key`|**-**|<p>The sorting key. Supported keys:<ul><li>`id` — An App project ID.</li><li>`name` — An App project name.</li><li>`created` — A project creation date.</li></ul></p>
