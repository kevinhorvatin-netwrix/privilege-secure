
## Retrieve access policy by id. (Auth policies: MfaRequired, MfaRequired; roles: Admin,App,UserPlus)

<a id="opIdGet"></a>

> Code samples

<details><summary>Shell</summary>


```shell
# You can also use wget
curl -X GET /api/v1/AccessControlPolicy/{accessControlPolicyId} \
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
Invoke-RestMethod -Method GET -Uri "$($NPSUrl)/api/v1/AccessControlPolicy/{accessControlPolicyId}" -Headers $Headers -ContentType "application/json"
```


</details>

`GET /api/v1/AccessControlPolicy/{accessControlPolicyId}`

Administrators can view all access policies.
Use an Access Policy custom role to delegate access to a specific access policy.

<h3 id="retrieve-access-policy-by-id.-(auth-policies:-mfarequired,-mfarequired;-roles:-admin,app,userplus)-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|accessControlPolicyId|path|string(uuid)|true|Id of the access control policy to return|
|ignoreStatus|query|boolean|false|If true get policy, ignoring deleted/disabled status|

> Example responses

> 200 Response

<details><summary>JSON</summary>


```json
{
  "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
  "name": "string",
  "description": "string",
  "priority": 0,
  "notesRequired": true,
  "ticketRequired": true,
  "approvalTypeRequired": "Deny",
  "policyType": "Resource",
  "managedAccountIds": [
    "497f6eca-6276-4993-bfeb-53cbbbba6f08"
  ],
  "managedAccountGroupIds": [
    "497f6eca-6276-4993-bfeb-53cbbbba6f08"
  ],
  "managedResourceIds": [
    "497f6eca-6276-4993-bfeb-53cbbbba6f08"
  ],
  "managedResourceGroupIds": [
    "497f6eca-6276-4993-bfeb-53cbbbba6f08"
  ],
  "credentialIds": [
    "497f6eca-6276-4993-bfeb-53cbbbba6f08"
  ],
  "activityIds": [
    "497f6eca-6276-4993-bfeb-53cbbbba6f08"
  ],
  "activities": [
    {
      "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
      "createdBy": "25a02396-1048-48f9-bf93-102d2fb7895e",
      "modifiedBy": "07ff0787-1af5-4fc4-9832-7aaeaa962a5e",
      "name": "string",
      "description": "string",
      "activityConfigurationId": "e649ca68-23ab-42cb-8af5-260e01dc50d6",
      "activityConfiguration": {
        "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
        "name": "string",
        "description": "string",
        "type": "Generic",
        "createdBy": "25a02396-1048-48f9-bf93-102d2fb7895e",
        "modifiedBy": "07ff0787-1af5-4fc4-9832-7aaeaa962a5e",
        "createdDateTimeUtc": "2019-08-24T14:15:22Z",
        "modifiedDateTimeUtc": "2019-08-24T14:15:22Z",
        "isDefault": true,
        "isDeleted": true,
        "isUserModified": true,
        "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177",
        "activityConfigurationSettings": [
          {
            "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
            "name": "string",
            "key": "string",
            "value": "string",
            "type": "String",
            "activityConfigurationId": "e649ca68-23ab-42cb-8af5-260e01dc50d6",
            "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177",
            "createdDateTimeUtc": "2019-08-24T14:15:22Z",
            "modifiedDateTimeUtc": "2019-08-24T14:15:22Z"
          }
        ],
        "customFields": [
          {
            "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
            "activityConfigurationId": "e649ca68-23ab-42cb-8af5-260e01dc50d6",
            "customFieldNumber": 0,
            "name": "string",
            "label": "string",
            "description": "string",
            "options": "string",
            "length": 0,
            "customFieldDataType": "Integer",
            "required": true,
            "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177",
            "createdDateTimeUtc": "2019-08-24T14:15:22Z",
            "modifiedDateTimeUtc": "2019-08-24T14:15:22Z"
          }
        ],
        "deleteAccount": true,
        "sessionRetryInterval": 0,
        "approvedWorkflowEmailTemplateId": "7323f20a-d61f-4cbd-9b9a-1ce63404d7a1",
        "notifyApproversWorkflowEmailTemplateId": "5997e1ba-a294-43d0-acaa-18d25ec8482f",
        "maxSessionLength": 0,
        "allowSessionExtension": true,
        "sessionExtensionMinutes": 0,
        "sessionExtensionCount": 0,
        "sessionMonitorInterval": 0,
        "expirationTimeoutThreshold": 0,
        "rdpProxyHost": "string",
        "sshProxyHost": "string",
        "sshScanDc": true,
        "recordAudio": true,
        "proxyAutoConnect": true,
        "record": true,
        "approvalTypeRequired": "Deny",
        "approvalWorkflowId": "2db777ef-e869-4d8f-8dc2-f01750b5b4aa",
        "approvalWorkflowEmailTemplateId": "3416bc31-9e7f-4338-b33c-7314dfcb92d4",
        "monitorEntireSession": true,
        "allowViewPassword": true,
        "allowPasswordAccess": true,
        "allowAutofillPassword": true,
        "leaveInGroup": true,
        "activityTokenComplexity": "123519da-14b2-440d-af88-b17b69fb9aa6",
        "clearWebsiteDataAfterStop": true,
        "clearWebsiteDataBeforeStart": true,
        "notesRequired": true,
        "ticketRequired": true,
        "viewPasswordInSeconds": 0
      },
      "platformId": "32a6e381-64f4-4911-86b6-3bf681b64d23",
      "platform": {
        "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
        "name": "string",
        "description": "string",
        "builtInAccount": "string",
        "passwordComplexityPolicyId": "2cd7b527-e70e-43d9-9b74-c73f64a0573e",
        "passwordComplexityPolicy": {
          "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
          "name": "string",
          "description": "string",
          "lowerCase": true,
          "upperCase": true,
          "specialCharacter": true,
          "space": true,
          "numeric": true,
          "mustEndWith": "None",
          "mustStartWith": "None",
          "length": 0,
          "maxConsecutive": 0,
          "charsToExclude": "string",
          "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177",
          "createdDateTimeUtc": "2019-08-24T14:15:22Z",
          "modifiedDateTimeUtc": "2019-08-24T14:15:22Z",
          "type": "Password"
        },
        "scheduledChangePolicyId": "17df2cc9-77aa-486d-b2c3-eb63a3689174",
        "scheduledChangePolicy": {
          "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
          "name": "string",
          "description": "string",
          "frequency": null,
          "periodValue": 0,
          "daysOfWeek": "string",
          "dayNumber": 0,
          "localTime": "2019-08-24T14:15:22Z",
          "utcTime": "2019-08-24T14:15:22Z",
          "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177",
          "createdDateTimeUtc": "2019-08-24T14:15:22Z",
          "modifiedDateTimeUtc": "2019-08-24T14:15:22Z"
        },
        "protectionPolicyScheduleId": "fb8b7dbf-b4af-4812-a27d-fdffc3b2498b",
        "protectionPolicySchedule": {
          "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
          "name": "string",
          "description": "string",
          "frequency": null,
          "periodValue": 0,
          "daysOfWeek": "string",
          "dayNumber": 0,
          "localTime": "2019-08-24T14:15:22Z",
          "utcTime": "2019-08-24T14:15:22Z",
          "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177",
          "createdDateTimeUtc": "2019-08-24T14:15:22Z",
          "modifiedDateTimeUtc": "2019-08-24T14:15:22Z"
        },
        "scanScheduleId": "0eb70c50-8dc6-4087-9b2a-b6a2adebf24d",
        "scanSchedule": {
          "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
          "name": "string",
          "description": "string",
          "frequency": null,
          "periodValue": 0,
          "daysOfWeek": "string",
          "dayNumber": 0,
          "localTime": "2019-08-24T14:15:22Z",
          "utcTime": "2019-08-24T14:15:22Z",
          "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177",
          "createdDateTimeUtc": "2019-08-24T14:15:22Z",
          "modifiedDateTimeUtc": "2019-08-24T14:15:22Z"
        },
        "verificationScheduleId": "cdcc8131-6845-4416-8986-86fd1614fd92",
        "verificationSchedule": {
          "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
          "name": "string",
          "description": "string",
          "frequency": null,
          "periodValue": 0,
          "daysOfWeek": "string",
          "dayNumber": 0,
          "localTime": "2019-08-24T14:15:22Z",
          "utcTime": "2019-08-24T14:15:22Z",
          "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177",
          "createdDateTimeUtc": "2019-08-24T14:15:22Z",
          "modifiedDateTimeUtc": "2019-08-24T14:15:22Z"
        },
        "resetOnMismatch": true,
        "icon": "string",
        "basePlatformId": "01dea6be-a8fe-4b3c-9c51-3efd6a2732fb",
        "type": "Unspecified",
        "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177",
        "createdDateTimeUtc": "2019-08-24T14:15:22Z",
        "modifiedDateTimeUtc": "2019-08-24T14:15:22Z"
      },
      "startActionGroupId": "fe816897-035e-41a8-b765-786a26e1fd7e",
      "duringActionGroupId": "42ac0cdb-f5d6-410c-aef7-524cbda8a405",
      "endActionGroupId": "129c4b86-8e07-4184-83ec-2719a1a163e2",
      "activityType": "Interactive",
      "loginAccount": "Requester",
      "loginAccountNameFormat": "string",
      "requesterLoginFormat": "Samaccountname",
      "applicationToLaunch": "string",
      "preferredRDSHostId": "14c3f91d-da41-4a85-9329-5b28802d466f",
      "connectCredentialId": "28819070-8040-4b05-9bbf-5d58cd54636a",
      "createAccount": true,
      "activityGroupActivities": [
        {
          "activityId": "bdfd0655-55e6-45e6-8bbc-6ed31d3820b5",
          "activity": {},
          "activityGroupId": "8a17e616-435e-4b20-86d3-9809358d6cdd",
          "activityGroup": {
            "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
            "createdBy": "25a02396-1048-48f9-bf93-102d2fb7895e",
            "modifiedBy": "07ff0787-1af5-4fc4-9832-7aaeaa962a5e",
            "modifiedDateTimeUtc": "2019-08-24T14:15:22Z",
            "name": "string",
            "description": "string",
            "activityConfigurationId": "e649ca68-23ab-42cb-8af5-260e01dc50d6",
            "activityConfiguration": {
              "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
              "name": "string",
              "description": "string",
              "type": "Generic",
              "createdBy": "25a02396-1048-48f9-bf93-102d2fb7895e",
              "modifiedBy": "07ff0787-1af5-4fc4-9832-7aaeaa962a5e",
              "createdDateTimeUtc": "2019-08-24T14:15:22Z",
              "modifiedDateTimeUtc": "2019-08-24T14:15:22Z",
              "isDefault": true,
              "isDeleted": true,
              "isUserModified": true,
              "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177",
              "activityConfigurationSettings": [
                {
                  "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
                  "name": "string",
                  "key": "string",
                  "value": "string",
                  "type": "String",
                  "activityConfigurationId": "e649ca68-23ab-42cb-8af5-260e01dc50d6",
                  "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177",
                  "createdDateTimeUtc": "2019-08-24T14:15:22Z",
                  "modifiedDateTimeUtc": "2019-08-24T14:15:22Z"
                }
              ],
              "customFields": [
                {
                  "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
                  "activityConfigurationId": "e649ca68-23ab-42cb-8af5-260e01dc50d6",
                  "customFieldNumber": 0,
                  "name": "string",
                  "label": "string",
                  "description": "string",
                  "options": "string",
                  "length": 0,
                  "customFieldDataType": "Integer",
                  "required": true,
                  "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177",
                  "createdDateTimeUtc": "2019-08-24T14:15:22Z",
                  "modifiedDateTimeUtc": "2019-08-24T14:15:22Z"
                }
              ],
              "deleteAccount": true,
              "sessionRetryInterval": 0,
              "approvedWorkflowEmailTemplateId": "7323f20a-d61f-4cbd-9b9a-1ce63404d7a1",
              "notifyApproversWorkflowEmailTemplateId": "5997e1ba-a294-43d0-acaa-18d25ec8482f",
              "maxSessionLength": 0,
              "allowSessionExtension": true,
              "sessionExtensionMinutes": 0,
              "sessionExtensionCount": 0,
              "sessionMonitorInterval": 0,
              "expirationTimeoutThreshold": 0,
              "rdpProxyHost": "string",
              "sshProxyHost": "string",
              "sshScanDc": true,
              "recordAudio": true,
              "proxyAutoConnect": true,
              "record": true,
              "approvalTypeRequired": "Deny",
              "approvalWorkflowId": "2db777ef-e869-4d8f-8dc2-f01750b5b4aa",
              "approvalWorkflowEmailTemplateId": "3416bc31-9e7f-4338-b33c-7314dfcb92d4",
              "monitorEntireSession": true,
              "allowViewPassword": true,
              "allowPasswordAccess": true,
              "allowAutofillPassword": true,
              "leaveInGroup": true,
              "activityTokenComplexity": "123519da-14b2-440d-af88-b17b69fb9aa6",
              "clearWebsiteDataAfterStop": true,
              "clearWebsiteDataBeforeStart": true,
              "notesRequired": true,
              "ticketRequired": true,
              "viewPasswordInSeconds": 0
            },
            "activityGroupActivities": [
              {}
            ],
            "isDefault": true,
            "isDeleted": true,
            "isUserModified": true,
            "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177",
            "createdDateTimeUtc": "2019-08-24T14:15:22Z"
          },
          "isDeleted": true,
          "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177",
          "createdDateTimeUtc": "2019-08-24T14:15:22Z",
          "modifiedDateTimeUtc": "2019-08-24T14:15:22Z"
        }
      ],
      "deleteAccount": true,
      "vaultId": "867f3a98-ec66-42f4-abbc-5980239e4a28",
      "vaultInfo": "string",
      "logonUrl": "string",
      "isDefault": true,
      "isDeleted": true,
      "isUserModified": true,
      "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177",
      "createdDateTimeUtc": "2019-08-24T14:15:22Z",
      "modifiedDateTimeUtc": "2019-08-24T14:15:22Z"
    }
  ],
  "activityConfiguration": "string",
  "activityConfigurationMaxSessionLength": 0,
  "activityConfigurationId": "e649ca68-23ab-42cb-8af5-260e01dc50d6",
  "activityGroups": [
    {
      "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
      "createdBy": "25a02396-1048-48f9-bf93-102d2fb7895e",
      "modifiedBy": "07ff0787-1af5-4fc4-9832-7aaeaa962a5e",
      "modifiedDateTimeUtc": "2019-08-24T14:15:22Z",
      "name": "string",
      "description": "string",
      "activityConfigurationId": "e649ca68-23ab-42cb-8af5-260e01dc50d6",
      "activityConfiguration": {
        "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
        "name": "string",
        "description": "string",
        "type": "Generic",
        "createdBy": "25a02396-1048-48f9-bf93-102d2fb7895e",
        "modifiedBy": "07ff0787-1af5-4fc4-9832-7aaeaa962a5e",
        "createdDateTimeUtc": "2019-08-24T14:15:22Z",
        "modifiedDateTimeUtc": "2019-08-24T14:15:22Z",
        "isDefault": true,
        "isDeleted": true,
        "isUserModified": true,
        "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177",
        "activityConfigurationSettings": [
          {
            "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
            "name": "string",
            "key": "string",
            "value": "string",
            "type": "String",
            "activityConfigurationId": "e649ca68-23ab-42cb-8af5-260e01dc50d6",
            "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177",
            "createdDateTimeUtc": "2019-08-24T14:15:22Z",
            "modifiedDateTimeUtc": "2019-08-24T14:15:22Z"
          }
        ],
        "customFields": [
          {
            "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
            "activityConfigurationId": "e649ca68-23ab-42cb-8af5-260e01dc50d6",
            "customFieldNumber": 0,
            "name": "string",
            "label": "string",
            "description": "string",
            "options": "string",
            "length": 0,
            "customFieldDataType": "Integer",
            "required": true,
            "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177",
            "createdDateTimeUtc": "2019-08-24T14:15:22Z",
            "modifiedDateTimeUtc": "2019-08-24T14:15:22Z"
          }
        ],
        "deleteAccount": true,
        "sessionRetryInterval": 0,
        "approvedWorkflowEmailTemplateId": "7323f20a-d61f-4cbd-9b9a-1ce63404d7a1",
        "notifyApproversWorkflowEmailTemplateId": "5997e1ba-a294-43d0-acaa-18d25ec8482f",
        "maxSessionLength": 0,
        "allowSessionExtension": true,
        "sessionExtensionMinutes": 0,
        "sessionExtensionCount": 0,
        "sessionMonitorInterval": 0,
        "expirationTimeoutThreshold": 0,
        "rdpProxyHost": "string",
        "sshProxyHost": "string",
        "sshScanDc": true,
        "recordAudio": true,
        "proxyAutoConnect": true,
        "record": true,
        "approvalTypeRequired": "Deny",
        "approvalWorkflowId": "2db777ef-e869-4d8f-8dc2-f01750b5b4aa",
        "approvalWorkflowEmailTemplateId": "3416bc31-9e7f-4338-b33c-7314dfcb92d4",
        "monitorEntireSession": true,
        "allowViewPassword": true,
        "allowPasswordAccess": true,
        "allowAutofillPassword": true,
        "leaveInGroup": true,
        "activityTokenComplexity": "123519da-14b2-440d-af88-b17b69fb9aa6",
        "clearWebsiteDataAfterStop": true,
        "clearWebsiteDataBeforeStart": true,
        "notesRequired": true,
        "ticketRequired": true,
        "viewPasswordInSeconds": 0
      },
      "activityGroupActivities": [
        {
          "activityId": "bdfd0655-55e6-45e6-8bbc-6ed31d3820b5",
          "activity": {
            "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
            "createdBy": "25a02396-1048-48f9-bf93-102d2fb7895e",
            "modifiedBy": "07ff0787-1af5-4fc4-9832-7aaeaa962a5e",
            "name": "string",
            "description": "string",
            "activityConfigurationId": "e649ca68-23ab-42cb-8af5-260e01dc50d6",
            "activityConfiguration": {
              "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
              "name": "string",
              "description": "string",
              "type": "Generic",
              "createdBy": "25a02396-1048-48f9-bf93-102d2fb7895e",
              "modifiedBy": "07ff0787-1af5-4fc4-9832-7aaeaa962a5e",
              "createdDateTimeUtc": "2019-08-24T14:15:22Z",
              "modifiedDateTimeUtc": "2019-08-24T14:15:22Z",
              "isDefault": true,
              "isDeleted": true,
              "isUserModified": true,
              "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177",
              "activityConfigurationSettings": [
                {
                  "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
                  "name": "string",
                  "key": "string",
                  "value": "string",
                  "type": "String",
                  "activityConfigurationId": "e649ca68-23ab-42cb-8af5-260e01dc50d6",
                  "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177",
                  "createdDateTimeUtc": "2019-08-24T14:15:22Z",
                  "modifiedDateTimeUtc": "2019-08-24T14:15:22Z"
                }
              ],
              "customFields": [
                {
                  "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
                  "activityConfigurationId": "e649ca68-23ab-42cb-8af5-260e01dc50d6",
                  "customFieldNumber": 0,
                  "name": "string",
                  "label": "string",
                  "description": "string",
                  "options": "string",
                  "length": 0,
                  "customFieldDataType": "Integer",
                  "required": true,
                  "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177",
                  "createdDateTimeUtc": "2019-08-24T14:15:22Z",
                  "modifiedDateTimeUtc": "2019-08-24T14:15:22Z"
                }
              ],
              "deleteAccount": true,
              "sessionRetryInterval": 0,
              "approvedWorkflowEmailTemplateId": "7323f20a-d61f-4cbd-9b9a-1ce63404d7a1",
              "notifyApproversWorkflowEmailTemplateId": "5997e1ba-a294-43d0-acaa-18d25ec8482f",
              "maxSessionLength": 0,
              "allowSessionExtension": true,
              "sessionExtensionMinutes": 0,
              "sessionExtensionCount": 0,
              "sessionMonitorInterval": 0,
              "expirationTimeoutThreshold": 0,
              "rdpProxyHost": "string",
              "sshProxyHost": "string",
              "sshScanDc": true,
              "recordAudio": true,
              "proxyAutoConnect": true,
              "record": true,
              "approvalTypeRequired": "Deny",
              "approvalWorkflowId": "2db777ef-e869-4d8f-8dc2-f01750b5b4aa",
              "approvalWorkflowEmailTemplateId": "3416bc31-9e7f-4338-b33c-7314dfcb92d4",
              "monitorEntireSession": true,
              "allowViewPassword": true,
              "allowPasswordAccess": true,
              "allowAutofillPassword": true,
              "leaveInGroup": true,
              "activityTokenComplexity": "123519da-14b2-440d-af88-b17b69fb9aa6",
              "clearWebsiteDataAfterStop": true,
              "clearWebsiteDataBeforeStart": true,
              "notesRequired": true,
              "ticketRequired": true,
              "viewPasswordInSeconds": 0
            },
            "platformId": "32a6e381-64f4-4911-86b6-3bf681b64d23",
            "platform": {
              "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
              "name": "string",
              "description": "string",
              "builtInAccount": "string",
              "passwordComplexityPolicyId": "2cd7b527-e70e-43d9-9b74-c73f64a0573e",
              "passwordComplexityPolicy": {
                "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
                "name": "string",
                "description": "string",
                "lowerCase": true,
                "upperCase": true,
                "specialCharacter": true,
                "space": true,
                "numeric": true,
                "mustEndWith": "None",
                "mustStartWith": "None",
                "length": 0,
                "maxConsecutive": 0,
                "charsToExclude": "string",
                "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177",
                "createdDateTimeUtc": "2019-08-24T14:15:22Z",
                "modifiedDateTimeUtc": "2019-08-24T14:15:22Z",
                "type": "Password"
              },
              "scheduledChangePolicyId": "17df2cc9-77aa-486d-b2c3-eb63a3689174",
              "scheduledChangePolicy": {
                "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
                "name": "string",
                "description": "string",
                "frequency": null,
                "periodValue": 0,
                "daysOfWeek": "string",
                "dayNumber": 0,
                "localTime": "2019-08-24T14:15:22Z",
                "utcTime": "2019-08-24T14:15:22Z",
                "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177",
                "createdDateTimeUtc": "2019-08-24T14:15:22Z",
                "modifiedDateTimeUtc": "2019-08-24T14:15:22Z"
              },
              "protectionPolicyScheduleId": "fb8b7dbf-b4af-4812-a27d-fdffc3b2498b",
              "protectionPolicySchedule": {
                "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
                "name": "string",
                "description": "string",
                "frequency": null,
                "periodValue": 0,
                "daysOfWeek": "string",
                "dayNumber": 0,
                "localTime": "2019-08-24T14:15:22Z",
                "utcTime": "2019-08-24T14:15:22Z",
                "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177",
                "createdDateTimeUtc": "2019-08-24T14:15:22Z",
                "modifiedDateTimeUtc": "2019-08-24T14:15:22Z"
              },
              "scanScheduleId": "0eb70c50-8dc6-4087-9b2a-b6a2adebf24d",
              "scanSchedule": {
                "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
                "name": "string",
                "description": "string",
                "frequency": null,
                "periodValue": 0,
                "daysOfWeek": "string",
                "dayNumber": 0,
                "localTime": "2019-08-24T14:15:22Z",
                "utcTime": "2019-08-24T14:15:22Z",
                "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177",
                "createdDateTimeUtc": "2019-08-24T14:15:22Z",
                "modifiedDateTimeUtc": "2019-08-24T14:15:22Z"
              },
              "verificationScheduleId": "cdcc8131-6845-4416-8986-86fd1614fd92",
              "verificationSchedule": {
                "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
                "name": "string",
                "description": "string",
                "frequency": null,
                "periodValue": 0,
                "daysOfWeek": "string",
                "dayNumber": 0,
                "localTime": "2019-08-24T14:15:22Z",
                "utcTime": "2019-08-24T14:15:22Z",
                "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177",
                "createdDateTimeUtc": "2019-08-24T14:15:22Z",
                "modifiedDateTimeUtc": "2019-08-24T14:15:22Z"
              },
              "resetOnMismatch": true,
              "icon": "string",
              "basePlatformId": "01dea6be-a8fe-4b3c-9c51-3efd6a2732fb",
              "type": "Unspecified",
              "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177",
              "createdDateTimeUtc": "2019-08-24T14:15:22Z",
              "modifiedDateTimeUtc": "2019-08-24T14:15:22Z"
            },
            "startActionGroupId": "fe816897-035e-41a8-b765-786a26e1fd7e",
            "duringActionGroupId": "42ac0cdb-f5d6-410c-aef7-524cbda8a405",
            "endActionGroupId": "129c4b86-8e07-4184-83ec-2719a1a163e2",
            "activityType": "Interactive",
            "loginAccount": "Requester",
            "loginAccountNameFormat": "string",
            "requesterLoginFormat": "Samaccountname",
            "applicationToLaunch": "string",
            "preferredRDSHostId": "14c3f91d-da41-4a85-9329-5b28802d466f",
            "connectCredentialId": "28819070-8040-4b05-9bbf-5d58cd54636a",
            "createAccount": true,
            "activityGroupActivities": [
              {}
            ],
            "deleteAccount": true,
            "vaultId": "867f3a98-ec66-42f4-abbc-5980239e4a28",
            "vaultInfo": "string",
            "logonUrl": "string",
            "isDefault": true,
            "isDeleted": true,
            "isUserModified": true,
            "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177",
            "createdDateTimeUtc": "2019-08-24T14:15:22Z",
            "modifiedDateTimeUtc": "2019-08-24T14:15:22Z"
          },
          "activityGroupId": "8a17e616-435e-4b20-86d3-9809358d6cdd",
          "activityGroup": {},
          "isDeleted": true,
          "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177",
          "createdDateTimeUtc": "2019-08-24T14:15:22Z",
          "modifiedDateTimeUtc": "2019-08-24T14:15:22Z"
        }
      ],
      "isDefault": true,
      "isDeleted": true,
      "isUserModified": true,
      "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177",
      "createdDateTimeUtc": "2019-08-24T14:15:22Z"
    }
  ],
  "activityGroupIds": [
    "497f6eca-6276-4993-bfeb-53cbbbba6f08"
  ]
}
```


</details>

<h3 id="retrieve-access-policy-by-id.-(auth-policies:-mfarequired,-mfarequired;-roles:-admin,app,userplus)-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|[SbPAM.Models.SimpleAccessControlPolicy](../Models/sbpam.models.simpleaccesscontrolpolicy.md)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|User does not have authorization to access policy.|[Microsoft.AspNetCore.Mvc.ProblemDetails](../Models/microsoft.aspnetcore.mvc.problemdetails.md)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
Bearer
</aside>


