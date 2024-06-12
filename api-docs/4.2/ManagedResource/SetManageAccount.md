
## Set the manage account setting for the list of given resources (Auth policies: MfaRequired; roles: Admin,App)

<a id="opIdSetManageAccount"></a>

> Code samples

<details><summary>Shell</summary>


```shell
# You can also use wget
curl -X PUT /api/v1/ManagedResource/ManageAccount/{manageAccount} \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer TOKEN'

```


</details>

<details><summary>PowerShell</summary>


```powershell
# PowerShell example
$JsonBody = @"
[
  "497f6eca-6276-4993-bfeb-53cbbbba6f08"
]
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
Invoke-RestMethod -Method PUT -Uri "$($NPSUrl)/api/v1/ManagedResource/ManageAccount/{manageAccount}" -Body $JsonBody -Headers $Headers -ContentType "application/json"
```


</details>

`PUT /api/v1/ManagedResource/ManageAccount/{manageAccount}`

> Body parameter

<details><summary>JSON</summary>


```json
[
  "497f6eca-6276-4993-bfeb-53cbbbba6f08"
]
```


</details>

<h3 id="set-the-manage-account-setting-for-the-list-of-given-resources-(auth-policies:-mfarequired;-roles:-admin,app)-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|manageAccount|path|[SbPAM.Models.ManagedResourceManageAccountEnum](../Models/sbpam.models.managedresourcemanageaccountenum.md)|true|One of Unmanaged, Managed|
|body|body|array[string]|false|List of resource ids to update|

#### Enumerated Values

|Parameter|Value|
|---|---|
|manageAccount|Unmanaged|
|manageAccount|Managed|

> Example responses

> 403 Response

<details><summary>JSON</summary>


```json
{
  "type": "string",
  "title": "string",
  "status": 0,
  "detail": "string",
  "instance": "string",
  "property1": null,
  "property2": null
}
```


</details>

<h3 id="set-the-manage-account-setting-for-the-list-of-given-resources-(auth-policies:-mfarequired;-roles:-admin,app)-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|User is not an Administrator|[Microsoft.AspNetCore.Mvc.ProblemDetails](../Models/microsoft.aspnetcore.mvc.problemdetails.md)|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Error has occurred, see Web log for details|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
Bearer
</aside>


