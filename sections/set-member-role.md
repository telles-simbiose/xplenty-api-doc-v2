## Set Member's Role

### Description
Set existing account [member's](https://github.com/xplenty/xplenty-api-doc-v2/blob/master/resources/user.md) role to either: `member`, `admin` or `owner` (only current owner can transfer ownership to another member).

### Input Parameters

|Name|Required?|Default|Description|
|----|---------|-------|-----------|
user_id|Y| |ID of user, must be supplied at the end of the request URL.
role|Y| |Possible values are `member`, `admin`, `owner`.

### Request (Curl Call) Syntax
```shell
$ curl -X PUT -u api_key: "https://api.xplenty.com/:account_id/api/members/:user_id" \
  -H "Accept: application/vnd.xplenty+json, version=2" \
  -H "Content-Type: application/json" \
  -d '{
    "role":"admin"
  }'
```

### Response Example
```HTTP
HTTP/1.1 200 OK
```

```json
{
  "id":1,
  "name":"Xplenty Admin",
  "email":"admin@example.com",
  "gravatar_email":"admin@example.com",
  "avatar_url":"http://gravatar.com/avatar/20760f72db6d9c7498dc0ba2f6e95fba.png?d=retro&s=140",
  "created_at": "2013-01-17T22:41:21Z",
  "updated_at": "2013-01-17T22:41:21Z",
  "role":"admin",
  "owner":false,
  "url": "https://api.xplenty.com/xplenation/api/members/1",
}
```
