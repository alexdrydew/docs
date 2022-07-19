# get_assignments
`toloka.client.TolokaClient.get_assignments`

Finds all assignments that match certain criteria.


`get_assignments` returns a generator. You can iterate over all found assignments using the generator. Several requests to the Toloka server are possible while iterating.

Note that assignments can not be sorted. If you need to sort assignments use [find_assignments](toloka.client.TolokaClient.find_assignments.md).

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

* **Yields:**

  Next matching assignment.

* **Yield type:**

  Generator\[[Assignment](toloka.client.assignment.Assignment.md), None, None\]

**Examples:**

The following example creates the list with IDs of `SUBMITTED` assignments in the specified pool.

```python
from toloka.client import Assignment
assignments = toloka_client.get_assignments(pool_id='1', status=Assignment.SUBMITTED)
result_list = [assignment.id for assignment in assignments]
```
