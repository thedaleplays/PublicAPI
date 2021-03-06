# Version 1.1

## Array-based Endpoints

Since version 1.1, arrays are 0-based, so the first record is at index 0, second record is at index 1, etc. The result set returned from endpoints can be further restricted by including the following Query Parameters.

|Query Parameter|Description|Notes|
|---|---|---|
|`limit`|The result set will be restricted by the value defined. Default and max is set to 100. Any value above 100 will return a 400 error.||
|`offset`|The result set returned will start at the index furnished by offset (i.e. when working with a working set larger than the limit of 100, offset may be furnished to paginate through results).||
|`orderBy`|The specified fields will be used to create the sort-order of the response payload.|[SQL Order By](https://www.w3schools.com/sql/sql_orderby.asp)|
|`where`|Value provided will follow the rules of a SQL-style `where` clause. Note that not all columns are filterable using the `where` clause. For each column in the response field list for an endpoint, the `filterable` column specifies whether or not it can be used within a `where` clause.|[SQL Where](https://www.w3schools.com/sql/sql_where.asp)|

## Response Headers

The following response headers are included to facilitate the handling of data.

|Header|Description|Notes|
|---|---|---|
|`API-Version`|The version of the API used to fulfill the request.||
|`Cache-Control`|See: https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Cache-Control for usage||
|`ETag`|See: https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/ETag for usage||
|`Last-Modified`|Can be used to compare when a record was last updated. Useful when comparing if your data is still valid.||
|`Link`|First, Prev, Next, and Last values will be present, if applicable.|For Array-based responses; [RFC](http://www.rfc-editor.org/rfc/rfc5988.txt)|
|`Num-Records`|The number of records within the entire result set.|For Array-based responses|

## Table of Contents
* Guides
  * [How-Tos](how-tos.md)
  * [Demos](demos.md)
* Resource Reference
  * [Activity](resources/activity.md)
  * [Badges](resources/badges.md)
  * [Donations](resources/donations.md)
  * [Donors](resources/donors.md)
  * [Events](resources/events.md)
  * [Incentives](resources/incentives.md)
  * [Milestones](resources/milestones.md)
  * [Participants](resources/participants.md)
  * [Teams](resources/teams.md)
  * [Team Groups](resources/teamgroups.md)
