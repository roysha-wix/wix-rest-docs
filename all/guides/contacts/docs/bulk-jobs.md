SortOrder: 3
# Bulk Jobs

The Contacts API allows you to perform these actions in bulk:

- [Bulk Add and Remove Labels][bulk-add-remove]
- [Bulk Update Contacts][bulk-update]
- [Bulk Delete Contacts][bulk-delete]

When your app calls one of the bulk endpoints listed above,
a new bulk job is created, and the `jobId` is returned.
You can get the status of any active or completed job with
[Get Bulk Job][get-bulk-job] and [List Bulk Jobs][list-bulk-jobs].

## Performing a dry run

Your app will use [`filter`][md-field-support]
and plain text `search` parameters
to specify the target contacts for a bulk job.
All contacts that meet the filter and search criteria
will be affected by the bulk operation.

Before running a bulk operation, can optionally perform a dry run
by running a [query][query] with the intended filter and search options.
You can show the query results to the user
and ask them to confirm that they want to continue with the bulk action.

[bulk-add-remove]: crm.contacts.contacts-v4.bulk-add-and-remove-labels
[bulk-update]: crm.contacts.contacts-v4.bulk-update-contacts
[bulk-delete]: crm.contacts.contacts-v4.bulk-delete-contacts
[get-bulk-job]: crm.contacts.bulk-jobs.get-bulk-job
[list-bulk-jobs]: crm.contacts.bulk-jobs.list-bulk-jobs
[query]: crm.contacts.contacts-v4.query-contacts
[md-field-support]: sort-and-filter.md#field-support-for-filtering-sorting-and-searching