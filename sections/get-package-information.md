## Get Package Information

### Description
The calls returns information for a [package](https://github.com/xplenty/xplenty-api-doc-v2/blob/master/resources/package.md) with the given package ID.

### Input Parameters
The **package ID** must be supplied at the end of the request URL.

### Request (Curl Call) Syntax
```shell
curl -X GET -H "Accept: application/vnd.xplenty+json" -u <APIkey>: "https://api.xplenty.com/<accountID>/api/packages/<packageID>"
```

### Response Example
```HTTP
HTTP/1.1 200 OK
```

```json
{
  "id": 2373,
  "name": "AWS CloudFront Log Analysis",
  "description": "This package processes AWS CloudFront logs and extracts traffic information by time, geography and URIs",
  "variables": {},
  "owner_id": 8,
  "created_at": "2014-03-12T07:09:18Z",
  "updated_at": "2014-04-13T19:38:04Z",
  "url": "https://api.xplenty.com/xplenation/api/packages/2373"
}
```