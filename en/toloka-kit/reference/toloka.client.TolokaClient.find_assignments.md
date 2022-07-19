# find_assignments
`toloka.client.TolokaClient.find_assignments`

Finds all assignments that match certain criteria.


The number of returned assignments is limited. Find remaining matching assignments with subsequent `find_assignments` calls.

To iterate over all matching assignments in one call use [get_assignments](toloka.client.TolokaClient.get_assignments.md). Note that `get_assignments` can't sort results.

## Parameters Description

| Parameters | Type | Description |
| :----------| :----| :-----------|
`status`|**Union\[str, [Assignment.Status](toloka.client.assignment.Assignment.Status.md), List\[Union\[str, [Assignment.Status](toloka.client.assignment.Assignment.Status.md)\]\], None\]**|<p>The status of an assigned task suite:<ul><li>`ACTIVE` — Assigned but not completed.</li><li>`SUBMITTED` — Completed but not checked.</li><li>`ACCEPTED` — Accepted by the requester.</li><li>`REJECTED` — Rejected by the requester.</li><li>`SKIPPED` — Skipped by the Toloker.</li><li>`EXPIRED` — Time for completing tasks has expired.</li></ul></p>
`task_id`|**Optional\[str\]**|<p>The ID of a task. The task suite containing that task, matches this search criteria.</p>
`task_suite_id`|**Optional\[str\]**|<p>The ID of a task suite.</p>
`pool_id`|**Optional\[str\]**|<p>Task suites in the pool with the specified ID.</p>
`user_id`|**Optional\[str\]**|<p>Task suites assigned to the Toloker with the specified ID.</p>
`id_lt`|**Optional\[str\]**|<p>Task suites with assignment IDs less than the specified value.</p>
`id_lte`|**Optional\[str\]**|<p>Task suites with assignment IDs less than or equal to the specified value.</p>
`id_gt`|**Optional\[str\]**|<p>Task suites with assignment IDs greater than the specified value.</p>
`id_gte`|**Optional\[str\]**|<p>Task suites with assignment IDs greater than or equal to the specified value.</p>
`created_lt`|**Optional\[datetime\]**|<p>Task suites assigned before the specified date.</p>
`created_lte`|**Optional\[datetime\]**|<p>Task suites assigned before or on the specified date.</p>
`created_gt`|**Optional\[datetime\]**|<p>Task suites assigned after the specified date.</p>
`created_gte`|**Optional\[datetime\]**|<p>Task suites assigned after or on the specified date.</p>
`submitted_lt`|**Optional\[datetime\]**|<p>Task suites completed before the specified date.</p>
`submitted_lte`|**Optional\[datetime\]**|<p>Task suites completed before or on the specified date.</p>
`submitted_gt`|**Optional\[datetime\]**|<p>Task suites completed after the specified date.</p>
`submitted_gte`|**Optional\[datetime\]**|<p>Task suites completed after or on the specified date.</p>
`accepted_lt`|**Optional\[datetime\]**|<p>Task suites accepted before the specified date.</p>
`accepted_lte`|**Optional\[datetime\]**|<p>Task suites accepted before or on the specified date.</p>
`accepted_gt`|**Optional\[datetime\]**|<p>Task suites accepted after the specified date.</p>
`accepted_gte`|**Optional\[datetime\]**|<p>Task suites accepted after or on the specified date.</p>
`rejected_lt`|**Optional\[datetime\]**|<p>Task suites rejected before the specified date.</p>
`rejected_lte`|**Optional\[datetime\]**|<p>Task suites rejected before or on the specified date.</p>
`rejected_gt`|**Optional\[datetime\]**|<p>Task suites rejected after the specified date.</p>
`rejected_gte`|**Optional\[datetime\]**|<p>Task suites rejected after or on the specified date.</p>
`skipped_lt`|**Optional\[datetime\]**|<p>Task suites skipped before the specified date.</p>
`skipped_lte`|**Optional\[datetime\]**|<p>Task suites skipped before or on the specified date.</p>
`skipped_gt`|**Optional\[datetime\]**|<p>Task suites skipped after the specified date.</p>
`skipped_gte`|**Optional\[datetime\]**|<p>Task suites skipped after or on the specified date.</p>
`expired_lt`|**Optional\[datetime\]**|<p>Task suites expired before the specified date.</p>
`expired_lte`|**Optional\[datetime\]**|<p>Task suites expired before or on the specified date.</p>
`expired_gt`|**Optional\[datetime\]**|<p>Task suites expired after the specified date.</p>
`expired_gte`|**Optional\[datetime\]**|<p>Task suites expired after or on the specified date.</p>
`sort`|**Union\[List\[str\], [AssignmentSortItems](toloka.client.search_requests.AssignmentSortItems.md), None\]**|<p>Sorting options. </p><p>Default value: `None`.</p>
`limit`|**Optional\[int\]**|<p>Returned assignments limit. The maximum value is 100,000. </p><p>Default value: 50.</p>

* **Returns:**

  Found assignments and a flag showing whether there are more matching assignments.

* **Return type:**

  [AssignmentSearchResult](toloka.client.search_results.AssignmentSearchResult.md)

**Examples:**

Search for `SKIPPED` or `EXPIRED` assignments in the specified pool.

```python
toloka_client.find_assignments(pool_id='1', status = ['SKIPPED', 'EXPIRED'])
```
