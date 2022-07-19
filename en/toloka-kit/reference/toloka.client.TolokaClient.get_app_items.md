# get_app_items
`toloka.client.TolokaClient.get_app_items`

Finds all App task items that match certain criteria in an App project.


`get_app_items` returns a generator. You can iterate over all found items using the generator. Several requests to the Toloka server are possible while iterating.

If you need to sort items use the [find_app_items](toloka.client.TolokaClient.find_app_items.md) method.

## Parameters Description

| Parameters | Type | Description |
| :----------| :----| :-----------|
`app_project_id`|**str**|<p>The ID of the App project.</p>
`after_id`|**Optional\[str\]**|<p>The ID of the item used for cursor pagination.</p>
`batch_id`|**Optional\[str\]**|<p>The ID of the batch to look in.</p>
`status`|**Optional\[[AppItem.Status](toloka.client.app.AppItem.Status.md)\]**|<p>Items with the specified status.</p>
`id_gt`|**Optional\[str\]**|<p>Items with IDs greater than the specified value.</p>
`id_gte`|**Optional\[str\]**|<p>Items with IDs greater than or equal to the specified value.</p>
`id_lt`|**Optional\[str\]**|<p>Items with IDs less than the specified value.</p>
`id_lte`|**Optional\[str\]**|<p>Items with IDs less than or equal to the specified value.</p>
`created_gt`|**Optional\[datetime\]**|<p>Items created after the specified date. The date is specified in UTC in ISO 8601 format: YYYY-MM-DDThh:mm:ss[.sss].</p>
`created_gte`|**Optional\[datetime\]**|<p>Items created after or on the specified date. The date is specified in UTC in ISO 8601 format: YYYY-MM-DDThh:mm:ss[.sss].</p>
`created_lt`|**Optional\[datetime\]**|<p>Items created before the specified date. The date is specified in UTC in ISO 8601 format: YYYY-MM-DDThh:mm:ss[.sss].</p>
`created_lte`|**Optional\[datetime\]**|<p>Items created before or on the specified date. The date is specified in UTC in ISO 8601 format: YYYY-MM-DDThh:mm:ss[.sss].</p>
`finished_gt`|**Optional\[datetime\]**|<p>Items labeled after the specified date.</p>
`finished_gte`|**Optional\[datetime\]**|<p>Items labeled after or on the specified date.</p>
`finished_lt`|**Optional\[datetime\]**|<p>Items labeled before the specified date.</p>
`finished_lte`|**Optional\[datetime\]**|<p>Items labeled before or on the specified date.</p>

* **Yields:**

  Next matching item.

* **Yield type:**

  Generator\[[AppItem](toloka.client.app.AppItem.md), None, None\]
