
## Set platform for batch of resources (Auth policies: MfaRequired; roles: Admin,App)

<a id="opIdSetPlatformBatchAsync"></a>

> Code samples

<details><summary>Shell</summary>


```shell
# You can also use wget
curl -X PUT /api/v1/ManagedResource/Platform/Bulk \
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
  "resourceIds": [
    "497f6eca-6276-4993-bfeb-53cbbbba6f08"
  ],
  "property": "938535c8-2515-42f9-852e-1720db2e50c1"
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
Invoke-RestMethod -Method PUT -Uri "$($NPSUrl)/api/v1/ManagedResource/Platform/Bulk" -Body $JsonBody -Headers $Headers -ContentType "application/json"
```


</details>

`PUT /api/v1/ManagedResource/Platform/Bulk`

> Body parameter

<details><summary>JSON</summary>


```json
{
  "resourceIds": [
    "497f6eca-6276-4993-bfeb-53cbbbba6f08"
  ],
  "property": "938535c8-2515-42f9-852e-1720db2e50c1"
}
```


</details>

<h3 id="set-platform-for-batch-of-resources-(auth-policies:-mfarequired;-roles:-admin,app)-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[SbPAM.WebAPI.Controllers.ManagedResourceBatch[System.Guid]](../Models/sbpam.webapi.controllers.managedresourcebatch_system.guid.md)|false|none|

> Example responses

> 200 Response

<details><summary>JSON</summary>


```json
[
  {
    "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
    "status": 0,
    "message": "string"
  }
]
```


</details>

<h3 id="set-platform-for-batch-of-resources-(auth-policies:-mfarequired;-roles:-admin,app)-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|An error has occurred, please see web log for more information|[Microsoft.AspNetCore.Mvc.ProblemDetails](../Models/microsoft.aspnetcore.mvc.problemdetails.md)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|User is not an Administrator|[Microsoft.AspNetCore.Mvc.ProblemDetails](../Models/microsoft.aspnetcore.mvc.problemdetails.md)|

<h3 id="set-platform-for-batch-of-resources-(auth-policies:-mfarequired;-roles:-admin,app)-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|[[SbPAM.WebAPI.Controllers.BatchResponse](../Models/sbpam.webapi.controllers.batchresponse.md)]|false|none|[Batched response]|
|» id|string(uuid)|false|none|Id of record that this response corresponds to|
|» status|integer(int32)|false|none|HttpStatus of response|
|» message|string¦null|false|none|Human readable message|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
Bearer
</aside>


