
## Test platform setting is valid for operating system (Auth policies: MfaRequired, MfaRequired; roles: Admin,App)

<a id="opIdTestPlatformAsync"></a>

> Code samples

<details><summary>Shell</summary>


```shell
# You can also use wget
curl -X GET /api/v1/ManagedResource/TestPlatform \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer TOKEN'

```


</details>

<details><summary>PowerShell</summary>


```powershell
# PowerShell example

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
Invoke-RestMethod -Method GET -Uri "$($NPSUrl)/api/v1/ManagedResource/TestPlatform" -Headers $Headers -ContentType "application/json"
```


</details>

`GET /api/v1/ManagedResource/TestPlatform`

<h3 id="test-platform-setting-is-valid-for-operating-system-(auth-policies:-mfarequired,-mfarequired;-roles:-admin,app)-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|operatingSystem|query|string|false|Operating system string e.g. "Microsoft Windows Server 2019"|
|platformId|query|string(uuid)|false|Platform Guid|
|platformType|query|[SbPAM.Models.PlatformTypeEnum](../Models/sbpam.models.platformtypeenum.md)|false|Name of platform (can be used instead of Guid)|

#### Enumerated Values

|Parameter|Value|
|---|---|
|platformType|Unspecified|
|platformType|Cloud|
|platformType|Database|

> Example responses

> 200 Response

<details><summary>JSON</summary>


```json
true
```


</details>

<h3 id="test-platform-setting-is-valid-for-operating-system-(auth-policies:-mfarequired,-mfarequired;-roles:-admin,app)-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|boolean|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Unable to test, see web logs for details|[Microsoft.AspNetCore.Mvc.ProblemDetails](../Models/microsoft.aspnetcore.mvc.problemdetails.md)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|User is not an Administrator|[Microsoft.AspNetCore.Mvc.ProblemDetails](../Models/microsoft.aspnetcore.mvc.problemdetails.md)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
Bearer
</aside>


