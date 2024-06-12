
## Get list of hosts where credential has been discovered (Auth policies: MfaRequired; roles: Admin)

<a id="opIdGetDistinctHostsForCredentialAsync"></a>

> Code samples

<details><summary>Shell</summary>


```shell
# You can also use wget
curl -X GET /api/v1/Credential/Hosts/{credentialId} \
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
Invoke-RestMethod -Method GET -Uri "$($NPSUrl)/api/v1/Credential/Hosts/{credentialId}" -Headers $Headers -ContentType "application/json"
```


</details>

`GET /api/v1/Credential/Hosts/{credentialId}`

This is returning the HostId for any computers where a
Windows Service or Windows Scheduled Task has been discovered
with a stored username and password that can be managed.
            
You can get more details about the host by using the
<see cref="M:SbPAM.WebAPI.Controllers.ManagedResourceController.GetManagedResourceByHostId(System.Guid)">/api/v1/ManagedResource/ByHostId</see>

<h3 id="get-list-of-hosts-where-credential-has-been-discovered-(auth-policies:-mfarequired;-roles:-admin)-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|credentialId|path|string(uuid)|true|Credential Id|

> Example responses

> 200 Response

<details><summary>JSON</summary>


```json
[
  "497f6eca-6276-4993-bfeb-53cbbbba6f08"
]
```


</details>

<h3 id="get-list-of-hosts-where-credential-has-been-discovered-(auth-policies:-mfarequired;-roles:-admin)-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|User is not an Administrator|[Microsoft.AspNetCore.Mvc.ProblemDetails](../Models/microsoft.aspnetcore.mvc.problemdetails.md)|

<h3 id="get-list-of-hosts-where-credential-has-been-discovered-(auth-policies:-mfarequired;-roles:-admin)-responseschema">Response Schema</h3>

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
Bearer
</aside>


