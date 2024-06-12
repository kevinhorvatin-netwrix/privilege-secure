
## Change the password for a Local user

<a id="opIdChangeLocalUserPasswordAsync"></a>

> Code samples

<details><summary>Shell</summary>


```shell
# You can also use wget
curl -X PUT /api/v1/ManagedAccount/ChangeLocalUserPassword \
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
  "managedAccountId": "98c25b84-2c06-4fcd-94c7-306443f45a3d",
  "username": "string",
  "passwordOld": "string",
  "passwordNew": "string"
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
Invoke-RestMethod -Method PUT -Uri "$($NPSUrl)/api/v1/ManagedAccount/ChangeLocalUserPassword" -Body $JsonBody -Headers $Headers -ContentType "application/json"
```


</details>

`PUT /api/v1/ManagedAccount/ChangeLocalUserPassword`

> Body parameter

<details><summary>JSON</summary>


```json
{
  "managedAccountId": "98c25b84-2c06-4fcd-94c7-306443f45a3d",
  "username": "string",
  "passwordOld": "string",
  "passwordNew": "string"
}
```


</details>

<h3 id="change-the-password-for-a-local-user-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|forced|query|boolean|false|If true, generates returns a new access jwt|
|body|body|[SbPAM.Models.LocalUserPasswordChangeRequest](../Models/sbpam.models.localuserpasswordchangerequest.md)|false|Password change information|

> Example responses

> 200 Response

<details><summary>JSON</summary>


```json
"string"
```


</details>

<h3 id="change-the-password-for-a-local-user-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|string|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Error changing password|[Microsoft.AspNetCore.Mvc.ProblemDetails](../Models/microsoft.aspnetcore.mvc.problemdetails.md)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Invalid Local user|[Microsoft.AspNetCore.Mvc.ProblemDetails](../Models/microsoft.aspnetcore.mvc.problemdetails.md)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
Bearer
</aside>


