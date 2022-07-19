# AppItemSortItems
`toloka.client.search_requests.AppItemSortItems`

```python
AppItemSortItems(self, items=None)
```

Keys for sorting App task items in search results.


You can specify multiple keys separated by a comma. To sort in descending order, add the `-` sign before a key.
Example: `sort='-created,id'`.

## Parameters Description

| Parameters | Type | Description |
| :----------| :----| :-----------|
`key`|**-**|<p>The sorting key. Supported keys:<ul><li>`id` — A task item ID.</li><li>`created` — The date and time when the item was created.</li><li>`finished` — The date and time when the item processing was completed.</li><li>`status` — The item status.</li></ul></p>
