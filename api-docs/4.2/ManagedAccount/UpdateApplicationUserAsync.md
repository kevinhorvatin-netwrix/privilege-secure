
## Update Application user (Auth roles: Admin)

<a id="opIdUpdateApplicationUserAsync"></a>

> Code samples

<details><summary>Shell</summary>


```shell
# You can also use wget
curl -X PUT /api/v1/ManagedAccount/UpdateApplicationUser \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer TOKEN'

```


</details>

<details><summary>PowerShell</summary>


```powershell
# PowerShell example
$JsonBody = @"
{
  "entityType": "ManagedAccount",
  "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
  "hostUserId": "f49f66da-8e90-4a2e-90ba-36f4d97bfbe9",
  "name": "string",
  "displayName": "string",
  "samAccountName": "string",
  "department": "string",
  "userPrincipalName": "string",
  "email": "string",
  "domainConfigId": "0ef2a0ae-0442-42e8-9ed5-4a4ed3f7578e",
  "domainName": "string",
  "lastLogonTimestamp": "2019-08-24T14:15:22Z",
  "activeSessionCount": 0,
  "scheduledSessionCount": 0,
  "accessPolicyCount": 0,
  "certificateSerialNumber": "string",
  "locked": true,
  "lockoutEnd": "2019-08-24T14:15:22Z",
  "isReviewer": true
}
"@

$NPSUrl = "https://localhost:6500"

$Login = @{
    Login = "User"
    Password = "Password"
}
# Cookie container for multi-factor authentication
$WebSession = New-Object Microsoft.PowerShell.Commands.WebRequestSession
$Token = Invoke-RestMethod -Uri "$($NPSUrl)/signinBody" -Method POST -Body (ConvertTo-Json $Login) -WebSession $WebSession -ContentType "application/json"
$Token = Invoke-RestMethod -Uri "$($NPSUrl)/signin2fa" -Method Post -Body $MfaCode -Headers @{Authorization = "Bearer $Token"} -WebSession $WebSession -ContentType "application/json"

$Headers = @{
    Authorization = "Bearer $Token"
}
Invoke-RestMethod -Method PUT -Uri "$($NPSUrl)/api/v1/ManagedAccount/UpdateApplicationUser" -Body $JsonBody -Headers $Headers -ContentType "application/json"
```


</details>

`PUT /api/v1/ManagedAccount/UpdateApplicationUser`

> Body parameter

<details><summary>JSON</summary>


```json
{
  "entityType": "ManagedAccount",
  "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
  "hostUserId": "f49f66da-8e90-4a2e-90ba-36f4d97bfbe9",
  "name": "string",
  "displayName": "string",
  "samAccountName": "string",
  "department": "string",
  "userPrincipalName": "string",
  "email": "string",
  "domainConfigId": "0ef2a0ae-0442-42e8-9ed5-4a4ed3f7578e",
  "domainName": "string",
  "lastLogonTimestamp": "2019-08-24T14:15:22Z",
  "activeSessionCount": 0,
  "scheduledSessionCount": 0,
  "accessPolicyCount": 0,
  "certificateSerialNumber": "string",
  "locked": true,
  "lockoutEnd": "2019-08-24T14:15:22Z",
  "isReviewer": true
}
```


</details>

<h3 id="update-application-user-(auth-roles:-admin)-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[SbPAM.Models.ManagedAccountView](../Models/sbpam.models.managedaccountview.md)|false|Update to apply|

> Example responses

> 200 Response

<details><summary>JSON</summary>


```json
{
  "entityType": "ManagedAccount",
  "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
  "hostUserId": "f49f66da-8e90-4a2e-90ba-36f4d97bfbe9",
  "name": "string",
  "displayName": "string",
  "samAccountName": "string",
  "department": "string",
  "userPrincipalName": "string",
  "email": "string",
  "domainConfigId": "0ef2a0ae-0442-42e8-9ed5-4a4ed3f7578e",
  "domainName": "string",
  "lastLogonTimestamp": "2019-08-24T14:15:22Z",
  "activeSessionCount": 0,
  "scheduledSessionCount": 0,
  "accessPolicyCount": 0,
  "certificateSerialNumber": "string",
  "locked": true,
  "lockoutEnd": "2019-08-24T14:15:22Z",
  "isReviewer": true
}
```


</details>

<h3 id="update-application-user-(auth-roles:-admin)-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|[SbPAM.Models.ManagedAccountView](../Models/sbpam.models.managedaccountview.md)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Error updating Application user|[Microsoft.AspNetCore.Mvc.ProblemDetails](../Models/microsoft.aspnetcore.mvc.problemdetails.md)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|User is not an Administrator|[Microsoft.AspNetCore.Mvc.ProblemDetails](../Models/microsoft.aspnetcore.mvc.problemdetails.md)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
Bearer
</aside>


