# Integration APIs

## APIs for DropIn to apply & manage integration

### Create an app

### Get an app

### Update an app

### Generate app secret

### Update account integration

### Generate account integration ID

### Login with account token

## APIs for third parties
DropIn uses access token as the authorization method and the API to get login link is also protected by this.
Third parties need to use the provided App ID and App Secret to get an access token,
then use this access token to get the login link.

### Get app access token
```javascript
POST /apps/auth
```

#### Body
- Required fields: `appId`, `appSecret`, `ttl`
- `ttl` - time until the token expires, defined in milliseconds, send `0` to create a token with no expiration time
```javascript
{
  "appId": "<App ID>",
  "appSecret": "<App Secret>",
  "ttl": 0
}
```

#### Sample success response
```javascript
200 OK
{
  "token": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJhcHBJZCI6IjU4NGVkODQ3ZGVhOThlOWNjMWE0NzhkOCIsImV4cGlyZXNPbiI6IjIwMjEtMTItMTlUMTA6MTM6MzguODMwWiIsInNjb3BlIjpudWxsLCJvcmdhbml6YXRpb25JZCI6IjU4MDczZDUyMTMwMTQ4YzA0NzY3NDQ4YiIsInR5cGUiOiJhcHAiLCJpYXQiOjE0ODIyMjg4MTgsImV4cCI6MjQ4MjIyODgxOCwiYXVkIjoiZHJvcGluLmNvbSIsImlzcyI6ImRyb3Bpbi5jb20ifQ.QZcyKLRetF3U9nIJThtjqqARdKn0E2lAxHu9IV0glxo",
  "expiresOn": "2021-12-19T10:13:38.830Z"
}
```

### Get login link
```javascript
POST /apps/auth
```

#### Headers
- Need `Authorization` header with value is the app access token
```javascript
Authorization: Bearer <app access token>
```

#### Body
- required field: `integrationId`
- `integrationId` - Integration ID of an account, this can be retrieved/changed in the admin page
- `meta` - metadata for the login URL, must be an array of { key, value }
```javascript
{
	"integrationId": "<Account's integration ID>",
	"meta": [{
		"key": "key",
		"value": "value"
	}]
}
```

#### Sample success response
- `url` - the generated login link, can be used only once
```javascript
200 OK
{
  "url": "https://appdev.dropininc.com/loginwithtoken?logintoken=1546&integrationid=5858b6eb08f03837084781f0",
  "loginToken": "1546",
  "integrationId": "5858b6eb08f03837084781f0"
}
```
