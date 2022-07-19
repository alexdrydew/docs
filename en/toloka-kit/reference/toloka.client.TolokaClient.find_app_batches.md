# find_app_batches
`toloka.client.TolokaClient.find_app_batches`

Finds batches that match certain criteria in an App project.


The number of returned batches is limited. Find remaining matching batches with subsequent `find_app_batches` calls.

To iterate over all matching batches you may use the [get_app_batches](toloka.client.TolokaClient.get_app_batches.md) method.

## Parameters Description

| Parameters | Type | Description |
| :----------| :----| :-----------|
`app_project_id`|**str**|<p>The ID of the App project.</p>
`after_id`|**Optional\[str\]**|<p>The ID of the batch used for cursor pagination.</p>
`status`|**Optional\[[AppBatch.Status](toloka.client.app.AppBatch.Status.md)\]**|<p>Batches with the specified status.</p>
`id_gt`|**Optional\[str\]**|<p>Batches with IDs greater than the specified value.</p>
`id_gte`|**Optional\[str\]**|<p>Batches with IDs greater than or equal to the specified value.</p>
`id_lt`|**Optional\[str\]**|<p>Batches with IDs less than the specified value.</p>
`id_lte`|**Optional\[str\]**|<p>Batches with IDs less than or equal to the specified value.</p>
`name_gt`|**Optional\[str\]**|<p>Batches with names lexicographically greater than the specified value.</p>
`name_gte`|**Optional\[str\]**|<p>Batches with names lexicographically greater than or equal to the specified value.</p>
`name_lt`|**Optional\[str\]**|<p>Batches with names lexicographically less than the specified value.</p>
`name_lte`|**Optional\[str\]**|<p>Batches with names lexicographically less than or equal to the specified value.</p>
`created_gt`|**Optional\[datetime\]**|<p>Batches created after the specified date. The date is specified in UTC in ISO 8601 format: YYYY-MM-DDThh:mm:ss[.sss].</p>
`created_gte`|**Optional\[datetime\]**|<p>Batches created after or on the specified date. The date is specified in UTC in ISO 8601 format: YYYY-MM-DDThh:mm:ss[.sss].</p>
`created_lt`|**Optional\[datetime\]**|<p>Batches created before the specified date. The date is specified in UTC in ISO 8601 format: YYYY-MM-DDThh:mm:ss[.sss].</p>
`created_lte`|**Optional\[datetime\]**|<p>Batches created before or on the specified date. The date is specified in UTC in ISO 8601 format: YYYY-MM-DDThh:mm:ss[.sss].</p>
`sort`|**Union\[List\[str\], [AppBatchSortItems](toloka.client.search_requests.AppBatchSortItems.md), None\]**|<p>Sorting options. Default: `None`.</p>
`limit`|**Optional\[int\]**|<p>Returned batches limit. The default limit is 50. The maximum allowed limit is 100,000.</p>

* **Returns:**

  Found batches and a flag showing whether there are more matching batches.

* **Return type:**

  [AppBatchSearchResult](toloka.client.search_results.AppBatchSearchResult.md)
