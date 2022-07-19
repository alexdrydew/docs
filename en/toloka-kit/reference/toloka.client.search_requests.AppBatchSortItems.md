# AppBatchSortItems
`toloka.client.search_requests.AppBatchSortItems`

```python
AppBatchSortItems(self, items=None)
```

Keys for sorting App batches in search results.


You can specify multiple keys separated by a comma. To sort in descending order, add the `-` sign before a key.
Example: `sort='-created,id'`.

## Parameters Description

| Parameters | Type | Description |
| :----------| :----| :-----------|
`key`|**-**|<p>The sorting key. Supported keys:<ul><li>`id` — A batch ID.</li><li>`name` — A batch name.</li><li>`created` — A batch creation date.</li><li>`status` — The item status.</li></ul></p>
