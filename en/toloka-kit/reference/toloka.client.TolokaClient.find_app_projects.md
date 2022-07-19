# find_app_projects
`toloka.client.TolokaClient.find_app_projects`

Finds App projects that match certain criteria.


The number of returned projects is limited. Find remaining matching projects with subsequent `find_app_projects` calls.
To iterate over all matching projects you may use the [get_app_projects](toloka.client.TolokaClient.get_app_projects.md) method.

## Parameters Description

| Parameters | Type | Description |
| :----------| :----| :-----------|
`app_id`|**Optional\[str\]**|<p>Projects created using the solution with the specified ID.</p>
`parent_app_project_id`|**Optional\[str\]**|<p>Projects cloned from the project with the specified ID. Projects can be cloned in the web version of Toloka.</p>
`status`|**Optional\[[AppProject.Status](toloka.client.app.AppProject.Status.md)\]**|<p>Projects with the specified status.</p>
`after_id`|**Optional\[str\]**|<p>The ID of a project used for cursor pagination.</p>
`scope`|**Optional\[[AppProjectSearchRequest.Scope](toloka.client.search_requests.AppProjectSearchRequest.Scope.md)\]**|<p>Values:<ul><li>`MY` — Projects created by you.</li><li>`COMPANY` — Projects created by requesters from your company.</li><li>`REQUESTER_LIST` — Projects created by requesters in the `requester_ids` list.</li></ul></p>
`requester_ids`|**Union\[str, List\[str\], None\]**|<p>A list with requester IDs separated by a comma. Use the list with parameter `scope = REQUESTER_LIST`.</p>
`id_gt`|**Optional\[str\]**|<p>Projects with IDs greater than the specified value.</p>
`id_gte`|**Optional\[str\]**|<p>Projects with IDs greater than or equal to the specified value.</p>
`id_lt`|**Optional\[str\]**|<p>Projects with IDs less than the specified value.</p>
`id_lte`|**Optional\[str\]**|<p>Projects with IDs less than or equal to the specified value.</p>
`name_gt`|**Optional\[str\]**|<p>Projects with a name lexicographically greater than the specified value.</p>
`name_gte`|**Optional\[str\]**|<p>Projects with a name lexicographically greater than or equal to the specified value.</p>
`name_lt`|**Optional\[str\]**|<p>Projects with a name lexicographically less than the specified value.</p>
`name_lte`|**Optional\[str\]**|<p>Projects with a name lexicographically less than or equal to the specified value.</p>
`created_gt`|**Optional\[datetime\]**|<p>Projects created after the specified date. The date is specified in UTC in ISO 8601 format: YYYY-MM-DDThh:mm:ss[.sss].</p>
`created_gte`|**Optional\[datetime\]**|<p>Projects created after or on the specified date. The date is specified in UTC in ISO 8601 format: YYYY-MM-DDThh:mm:ss[.sss].</p>
`created_lt`|**Optional\[datetime\]**|<p>Projects created before the specified date. The date is specified in UTC in ISO 8601 format: YYYY-MM-DDThh:mm:ss[.sss].</p>
`created_lte`|**Optional\[datetime\]**|<p>Projects created before or on the specified date. The date is specified in UTC in ISO 8601 format: YYYY-MM-DDThh:mm:ss[.sss].</p>
`sort`|**Union\[List\[str\], [AppProjectSortItems](toloka.client.search_requests.AppProjectSortItems.md), None\]**|<p>The order and direction of sorting the results.</p>
`limit`|**Optional\[int\]**|<p>Returned projects limit. The default limit is 50. The maximum limit is 100,000.</p>

* **Returns:**

  Found projects and a flag showing whether there are more matching projects.

* **Return type:**

  [AppProjectSearchResult](toloka.client.search_results.AppProjectSearchResult.md)
