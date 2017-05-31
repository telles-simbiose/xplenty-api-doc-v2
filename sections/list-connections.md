## List Account Connections

### Description
List [connections](https://github.com/xplenty/xplenty-api-doc-v2/blob/master/resources/connection.md) that are accessible by the authenticated user.
Optionally, you can supply the input parameters to filter the connection list so that it contains only connections with specific types and to determine the order by which the list will be sorted.

### Input Parameters

|Name|Required?|Default|Description|
|----|---------|-------|-----------|
type|N|"all" |Possible values are listed above or ```all```. The call will return only connections with the given types, or all the connections if the "all" value is specified. Values can be joined with commas, e.g. 's3,postgres'.
sort|N|"created"|Possible values are ```id```, ```name```, ```type```, ```updated``` or ```created```.
direction|N|"desc"|Possible values are: ```asc```, ```desc```. The connection will be sorted in ascending or descending order of the "sort" attribute.
since|N| |The connection list will only contain connections updated at the given time or later. The time must be formatted as UTC in the ISO 8601 format: ```YYYY-MM-DDTHH:MM:SSZ```. Example: “2013-01-17T22:41:21Z”.

### Request (Curl Call) Syntax
```shell
$ curl -X GET -u api_key: "https://api.xplenty.com/:account_id/api/connections" \
  -H "Accept: application/vnd.xplenty+json; version=2"
```

### Response Example
```HTTP
HTTP/1.1 200 OK
```

```json
[
  {
    "id":53,
    "name":"Amazon S3 sample connection",
    "username": "johndoe",
    "unique_id":"S3_CONNECTION_53",
    "created_at":"2016-04-21T13:55:43Z",
    "updated_at":"2016-04-21T13:55:43Z",
    "type":"s3",
    "url":"https://api.xplenty.com/xplenation/api/connections/s3/53"
  },
  {
    "id":54,
    "name":"Amazon S3 sample connection 2",
    "username": "johndoe",
    "unique_id":"S3_CONNECTION_54",
    "created_at":"2016-04-21T13:55:43Z",
    "updated_at":"2016-04-21T13:55:43Z",
    "type":"s3",
    "url":"https://api.xplenty.com/xplenation/api/connections/s3/54"
  },
  {
    "id":55,
    "name":"Amazon S3 sample connection 3",
    "username": "johndoe",
    "unique_id":"S3_CONNECTION_55",
    "created_at":"2016-04-21T13:55:43Z",
    "updated_at":"2016-04-21T13:55:43Z",
    "type":"s3",
    "url":"https://api.xplenty.com/xplenation/api/connections/s3/55"
  }
]
```
