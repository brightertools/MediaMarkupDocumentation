# WebHooks

WebHooks or callbacks to your own application are available for integration, WebHooks are posted to a specified url for various events within MediaMarkup.

The WebHook Url is configured within the account details and is available to all account administrators.

A webhook or callback will be posted to the specified url upon various events and post a JSON object, the properties of the JSON object will contain an eventType, id, created date and data properties. The data property structure will change for each event type. each event will have a unique id and created date \(unix time stamp\)

### Example webhook data

Approval.Create = Approval Created

```javascript
{ 
    "eventType": "Approval.Create", 
    "id":" 0faf1b6b04be4faea95af964466cb54b", 
    "created": 1527883431, 
    "data": 
        { 
            "approvalId": "38cfbf80b38d4a01a4f29027985d792d", 
            "name": "11111" 
        } 
}
```



