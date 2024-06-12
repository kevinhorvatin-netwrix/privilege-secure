
## Add multiple users/groups to NPS (Auth roles: Admin,App)

<a id="opIdAddMultipleAsync"></a>

> Code samples

<details><summary>Shell</summary>


```shell
# You can also use wget
curl -X POST /api/v1/ManagedAccount/AddMultiple \
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
  {
    "entityType": "HostUser",
    "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08"
  }
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
Invoke-RestMethod -Method POST -Uri "$($NPSUrl)/api/v1/ManagedAccount/AddMultiple" -Body $JsonBody -Headers $Headers -ContentType "application/json"
```


</details>

`POST /api/v1/ManagedAccount/AddMultiple`

> Body parameter

<details><summary>JSON</summary>


```json
[
  {
    "entityType": "HostUser",
    "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08"
  }
]
```


</details>

<h3 id="add-multiple-users/groups-to-nps-(auth-roles:-admin,app)-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[SbPAM.Actors.Interfaces.HostUserOrGroupId](../Models/sbpam.actors.interfaces.hostuserorgroupid.md)|false|List of users/groups to add to NPS|

> Example responses

> 200 Response

<details><summary>JSON</summary>


```json
{
  "item1": 0,
  "item2": 0
}
```


</details>

<h3 id="add-multiple-users/groups-to-nps-(auth-roles:-admin,app)-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|[System.TupleSystem.Int32,[System.Int32]](../Models/system.tuplesystem.int32,_system.int32.md)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Error adding user/groups to NPS|[Microsoft.AspNetCore.Mvc.ProblemDetails](../Models/microsoft.aspnetcore.mvc.problemdetails.md)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|User is not an Administrator|[Microsoft.AspNetCore.Mvc.ProblemDetails](../Models/microsoft.aspnetcore.mvc.problemdetails.md)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
Bearer
</aside>


