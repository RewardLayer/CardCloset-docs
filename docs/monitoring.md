## Monitoring
***
### ```GET``` v1/heartbeat
#### Heartbeat Message

A heart resource that allows for the monitoring and testing of the API
***
Request
```sh
GET https://api-cardnow.com/v1/heartbeat
Accept-Encoding: gzip,deflate
correlationid: 7e79f263-57a7-4d59-bd0a-69e03806488f
Host: api.cardnow.com
Connection: Keep-Alive
User-Agent: Apache-HttpClient/4.1.1 (java 1.5)
```
***
=== "Response - 200 OK"

```json
{
  "heartbeat": "ok"
}
```

=== "Response - 500 "

```json
{
  "ErrorCode": "cardnow.error.heartbeat",
  "Message": "The is something wrong with the heartbeat message",
  "MoreInfoUrl": "docs.cardnow.com/api-reference/exchange.invalid.heartbeat",
  "UserMessage": "There was an error when calling the heartbeat message. Please contact support@cardnow.com to address the issue. "
}
```

=== "Response - 503"

```json

```

***
##### Headers

|Name|Type|Description|
|---|---|---|
|correlationid|`guid`|The correlation Id is used to track the API request|
|x-api-key|`guid`|The API key from your developer account used to identify the limits on your account|

***
##### Status Returns
|Http Status|Response Model|Notes|
|---|---|---|
|200|None||
|400|`Error`||
|400| |Rate Limited|
|500| ||
|503| ||

***
##### Status Returns
