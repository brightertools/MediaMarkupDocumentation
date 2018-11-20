# Endpoints

Please find additional documentation here on endpoints that might not be available at https://api/mediamarkup.com/api-docs

{% api-method method="post" host="https://api.mediamarkup.com/api" path="/v1/Approvals/CreatePersonalUrl" %}
{% api-method-summary %}
CreatePersonalUrl
{% endapi-method-summary %}

{% api-method-description %}
Creates a secure personal url for the specified userId and approval/comparison id and versions. PersonalUrls are time limited and must be created immediately before redirecting a user.  
  
The PersonalUrl will authenticat the user and redirect them to the annotation tool. If the uesr is not authorized, the authentication url will redirect the user to a login page or the RedirectUrl configured, with the following **redir** url parameters;   
  
NotAuthenticated - User/Tenant/Authenticatiuon token is not valid or authenticated   
  
AuthenticationExpired - if the expiry date within the validation token has expired.  
  
UserLoggedOut - User logged out via the Logout button
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="parameters" type="object" required=false %}
{ "userId": "string", "approvalId": "string", "version": 0, "compareApprovalId": "string", "compareVersion": 0, "observer": true }
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{  "url": "string",  "hasErrors": true,  "messages": ["string" ]}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

