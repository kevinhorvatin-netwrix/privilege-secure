
## Search for access policies (Auth policies: MfaRequired)

<a id="opIdSearchForPolicy"></a>

> Code samples

<details><summary>Shell</summary>


```shell
# You can also use wget
curl -X GET /api/v1/AccessControlPolicy/PolicySearch \
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
Invoke-RestMethod -Method GET -Uri "$($NPSUrl)/api/v1/AccessControlPolicy/PolicySearch" -Headers $Headers -ContentType "application/json"
```


</details>

`GET /api/v1/AccessControlPolicy/PolicySearch`

<h3 id="search-for-access-policies-(auth-policies:-mfarequired)-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|managedAccountId|query|string(uuid)|false|Managed account id of user in access policy definiton.|
|activityName|query|string|false|Activity name to find in acess policy definition.|
|resourceName|query|string|false|Resource name to find in access policy definition.|
|replacementChar|query|string|false|Replace characters in activity name and resource name with space that match this character.|
|getAll|query|boolean|false|If set to true, returns all policies. False is default|

> Example responses

> 200 Response

<details><summary>JSON</summary>


```json
[
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
]
```


</details>

<h3 id="search-for-access-policies-(auth-policies:-mfarequired)-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Unable to find a policy for given resource, credential or policy. See response body for details.|[Microsoft.AspNetCore.Mvc.ProblemDetails](../Models/microsoft.aspnetcore.mvc.problemdetails.md)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Logged in user is not an administrator and the managed account id does not match logged in id|[Microsoft.AspNetCore.Mvc.ProblemDetails](../Models/microsoft.aspnetcore.mvc.problemdetails.md)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Unable to find a matching policy|[Microsoft.AspNetCore.Mvc.ProblemDetails](../Models/microsoft.aspnetcore.mvc.problemdetails.md)|

<h3 id="search-for-access-policies-(auth-policies:-mfarequired)-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|[[SbPAM.Models.SimpleAccessControlPolicy](../Models/sbpam.models.simpleaccesscontrolpolicy.md)]|false|none|none|
|» id|string(uuid)|false|none|none|
|» name|string¦null|false|none|none|
|» description|string¦null|false|none|none|
|» priority|integer(int32)|false|none|none|
|» notesRequired|boolean|false|none|none|
|» ticketRequired|boolean|false|none|none|
|» approvalTypeRequired|[SbPAM.Models.ApprovalType](../Models/sbpam.models.approvaltype.md)(int32)|false|none|none|
|» policyType|[SbPAM.Models.PolicyType](../Models/sbpam.models.policytype.md)(int32)|false|none|none|
|» managedAccountIds|[string]¦null|false|none|none|
|» managedAccountGroupIds|[string]¦null|false|none|none|
|» managedResourceIds|[string]¦null|false|none|none|
|» managedResourceGroupIds|[string]¦null|false|none|none|
|» credentialIds|[string]¦null|false|none|none|
|» activityIds|[string]¦null|false|none|none|
|» activities|[[SbPAM.Models.Activity](../Models/sbpam.models.activity.md)]¦null|false|none|none|
|»» id|string(uuid)|false|none|none|
|»» createdBy|string(uuid)¦null|false|none|none|
|»» modifiedBy|string(uuid)¦null|false|none|none|
|»» name|string¦null|false|none|none|
|»» description|string¦null|false|none|none|
|»» activityConfigurationId|string(uuid)¦null|false|none|none|
|»» activityConfiguration|[SbPAM.Models.ActivityConfiguration](../Models/sbpam.models.activityconfiguration.md)|false|none|none|
|»»» id|string(uuid)|false|none|none|
|»»» name|string¦null|false|none|none|
|»»» description|string¦null|false|none|none|
|»»» type|[SbPAM.Models.ActivityConfigurationType](../Models/sbpam.models.activityconfigurationtype.md)(int32)|false|none|none|
|»»» createdBy|string(uuid)¦null|false|none|none|
|»»» modifiedBy|string(uuid)¦null|false|none|none|
|»»» createdDateTimeUtc|string(date-time)|false|none|none|
|»»» modifiedDateTimeUtc|string(date-time)|false|none|none|
|»»» isDefault|boolean|false|none|none|
|»»» isDeleted|boolean|false|none|none|
|»»» isUserModified|boolean|false|none|none|
|»»» nodeId|string(uuid)|false|none|none|
|»»» activityConfigurationSettings|[[SbPAM.Models.ActivityConfigurationSetting](../Models/sbpam.models.activityconfigurationsetting.md)]¦null|false|none|none|
|»»»» id|string(uuid)|false|none|none|
|»»»» name|string¦null|false|none|none|
|»»»» key|string¦null|false|none|none|
|»»»» value|string¦null|false|none|none|
|»»»» type|[SbPAM.Models.ActivityConfigurationSettingType](../Models/sbpam.models.activityconfigurationsettingtype.md)(int32)|false|none|none|
|»»»» activityConfigurationId|string(uuid)|false|none|none|
|»»»» nodeId|string(uuid)|false|none|none|
|»»»» createdDateTimeUtc|string(date-time)|false|none|none|
|»»»» modifiedDateTimeUtc|string(date-time)|false|none|none|
|»»» customFields|[[SbPAM.Models.CustomField](../Models/sbpam.models.customfield.md)]¦null|false|none|none|
|»»»» id|string(uuid)|false|none|none|
|»»»» activityConfigurationId|string(uuid)|false|none|none|
|»»»» customFieldNumber|integer(int32)|false|none|none|
|»»»» name|string¦null|false|none|none|
|»»»» label|string¦null|false|none|none|
|»»»» description|string¦null|false|none|none|
|»»»» options|string¦null|false|none|none|
|»»»» length|integer(int32)¦null|false|none|none|
|»»»» customFieldDataType|[SbPAM.Models.CustomFieldDataType](../Models/sbpam.models.customfielddatatype.md)(int32)|false|none|none|
|»»»» required|boolean|false|none|none|
|»»»» nodeId|string(uuid)|false|none|none|
|»»»» createdDateTimeUtc|string(date-time)|false|none|none|
|»»»» modifiedDateTimeUtc|string(date-time)|false|none|none|
|»»» deleteAccount|boolean|false|none|none|
|»»» sessionRetryInterval|integer(int32)¦null|false|none|none|
|»»» approvedWorkflowEmailTemplateId|string(uuid)¦null|false|none|none|
|»»» notifyApproversWorkflowEmailTemplateId|string(uuid)¦null|false|none|none|
|»»» maxSessionLength|integer(int32)¦null|false|none|none|
|»»» allowSessionExtension|boolean|false|none|none|
|»»» sessionExtensionMinutes|integer(int32)¦null|false|none|none|
|»»» sessionExtensionCount|integer(int32)¦null|false|none|none|
|»»» sessionMonitorInterval|integer(int32)¦null|false|none|none|
|»»» expirationTimeoutThreshold|integer(int32)¦null|false|none|none|
|»»» rdpProxyHost|string¦null|false|none|none|
|»»» sshProxyHost|string¦null|false|none|none|
|»»» sshScanDc|boolean|false|none|none|
|»»» recordAudio|boolean|false|none|none|
|»»» proxyAutoConnect|boolean|false|none|none|
|»»» record|boolean|false|none|none|
|»»» approvalTypeRequired|[SbPAM.Models.ApprovalType](../Models/sbpam.models.approvaltype.md)(int32)|false|none|none|
|»»» approvalWorkflowId|string(uuid)¦null|false|none|none|
|»»» approvalWorkflowEmailTemplateId|string(uuid)¦null|false|none|none|
|»»» monitorEntireSession|boolean|false|none|none|
|»»» allowViewPassword|boolean|false|none|none|
|»»» allowPasswordAccess|boolean|false|none|none|
|»»» allowAutofillPassword|boolean|false|none|none|
|»»» leaveInGroup|boolean|false|none|none|
|»»» activityTokenComplexity|string(uuid)¦null|false|none|none|
|»»» clearWebsiteDataAfterStop|boolean|false|none|none|
|»»» clearWebsiteDataBeforeStart|boolean|false|none|none|
|»»» notesRequired|boolean|false|none|none|
|»»» ticketRequired|boolean|false|none|none|
|»»» viewPasswordInSeconds|integer(int32)¦null|false|none|none|
|»» platformId|string(uuid)¦null|false|none|none|
|»» platform|[SbPAM.Models.Platform](../Models/sbpam.models.platform.md)|false|none|none|
|»»» id|string(uuid)|false|none|none|
|»»» name|string¦null|false|none|none|
|»»» description|string¦null|false|none|none|
|»»» builtInAccount|string¦null|false|none|none|
|»»» passwordComplexityPolicyId|string(uuid)¦null|false|none|none|
|»»» passwordComplexityPolicy|[SbPAM.Models.PasswordComplexity](../Models/sbpam.models.passwordcomplexity.md)|false|none|none|
|»»»» id|string(uuid)|false|none|none|
|»»»» name|string¦null|false|none|none|
|»»»» description|string¦null|false|none|none|
|»»»» lowerCase|boolean|false|none|none|
|»»»» upperCase|boolean|false|none|none|
|»»»» specialCharacter|boolean|false|none|none|
|»»»» space|boolean|false|none|none|
|»»»» numeric|boolean|false|none|none|
|»»»» mustEndWith|[SbPAM.Constants.CharacterTypeFlags](../Models/sbpam.constants.charactertypeflags.md)(int32)|false|none|none|
|»»»» mustStartWith|[SbPAM.Constants.CharacterTypeFlags](../Models/sbpam.constants.charactertypeflags.md)(int32)|false|none|none|
|»»»» length|integer(int32)|false|none|none|
|»»»» maxConsecutive|integer(int32)|false|none|none|
|»»»» charsToExclude|string¦null|false|none|none|
|»»»» nodeId|string(uuid)|false|none|none|
|»»»» createdDateTimeUtc|string(date-time)|false|none|none|
|»»»» modifiedDateTimeUtc|string(date-time)|false|none|none|
|»»»» type|[SbPAM.Models.PasswordComplexityTypeEnum](../Models/sbpam.models.passwordcomplexitytypeenum.md)(int32)|false|none|none|
|»»» scheduledChangePolicyId|string(uuid)¦null|false|none|none|
|»»» scheduledChangePolicy|[SbPAM.Models.ScheduledChangePolicy](../Models/sbpam.models.scheduledchangepolicy.md)|false|none|none|
|»»»» id|string(uuid)|false|none|none|
|»»»» name|string¦null|false|none|none|
|»»»» description|string¦null|false|none|none|
|»»»» frequency|any|false|none|none|
|»»»» periodValue|integer(int32)|false|none|none|
|»»»» daysOfWeek|string¦null|false|none|none|
|»»»» dayNumber|integer(int32)|false|none|none|
|»»»» localTime|string(date-time)|false|none|none|
|»»»» utcTime|string(date-time)¦null|false|none|none|
|»»»» nodeId|string(uuid)|false|none|none|
|»»»» createdDateTimeUtc|string(date-time)|false|none|none|
|»»»» modifiedDateTimeUtc|string(date-time)|false|none|none|
|»»» protectionPolicyScheduleId|string(uuid)¦null|false|none|none|
|»»» protectionPolicySchedule|[SbPAM.Models.ScheduledChangePolicy](../Models/sbpam.models.scheduledchangepolicy.md)|false|none|none|
|»»» scanScheduleId|string(uuid)¦null|false|none|none|
|»»» scanSchedule|[SbPAM.Models.ScheduledChangePolicy](../Models/sbpam.models.scheduledchangepolicy.md)|false|none|none|
|»»» verificationScheduleId|string(uuid)¦null|false|none|none|
|»»» verificationSchedule|[SbPAM.Models.ScheduledChangePolicy](../Models/sbpam.models.scheduledchangepolicy.md)|false|none|none|
|»»» resetOnMismatch|boolean|false|none|none|
|»»» icon|string(byte)¦null|false|none|none|
|»»» basePlatformId|string(uuid)¦null|false|none|none|
|»»» type|[SbPAM.Models.PlatformTypeEnum](../Models/sbpam.models.platformtypeenum.md)(int32)|false|none|none|
|»»» nodeId|string(uuid)|false|none|none|
|»»» createdDateTimeUtc|string(date-time)|false|none|none|
|»»» modifiedDateTimeUtc|string(date-time)|false|none|none|
|»» startActionGroupId|string(uuid)¦null|false|none|none|
|»» duringActionGroupId|string(uuid)¦null|false|none|none|
|»» endActionGroupId|string(uuid)¦null|false|none|none|
|»» activityType|[SbPAM.Models.ActivityType](../Models/sbpam.models.activitytype.md)(int32)|false|none|none|
|»» loginAccount|[SbPAM.Models.ActivityLoginType](../Models/sbpam.models.activitylogintype.md)(int32)|false|none|none|
|»» loginAccountNameFormat|string¦null|false|none|none|
|»» requesterLoginFormat|[SbPAM.Models.RequesterLoginFormat](../Models/sbpam.models.requesterloginformat.md)(int32)|false|none|none|
|»» applicationToLaunch|string¦null|false|none|none|
|»» preferredRDSHostId|string(uuid)¦null|false|none|none|
|»» connectCredentialId|string(uuid)¦null|false|none|none|
|»» createAccount|boolean|false|none|none|
|»» activityGroupActivities|[[SbPAM.Models.ActivityGroupActivity](../Models/sbpam.models.activitygroupactivity.md)]¦null|false|none|none|
|»»» activityId|string(uuid)|false|none|none|
|»»» activity|[SbPAM.Models.Activity](../Models/sbpam.models.activity.md)|false|none|none|
|»»» activityGroupId|string(uuid)|false|none|none|
|»»» activityGroup|[SbPAM.Models.ActivityGroup](../Models/sbpam.models.activitygroup.md)|false|none|none|
|»»»» id|string(uuid)|false|none|none|
|»»»» createdBy|string(uuid)¦null|false|none|none|
|»»»» modifiedBy|string(uuid)¦null|false|none|none|
|»»»» modifiedDateTimeUtc|string(date-time)|false|none|none|
|»»»» name|string¦null|false|none|none|
|»»»» description|string¦null|false|none|none|
|»»»» activityConfigurationId|string(uuid)¦null|false|none|none|
|»»»» activityConfiguration|[SbPAM.Models.ActivityConfiguration](../Models/sbpam.models.activityconfiguration.md)|false|none|none|
|»»»» activityGroupActivities|[[SbPAM.Models.ActivityGroupActivity](../Models/sbpam.models.activitygroupactivity.md)]¦null|false|none|none|
|»»»» isDefault|boolean|false|none|none|
|»»»» isDeleted|boolean|false|none|none|
|»»»» isUserModified|boolean|false|none|none|
|»»»» nodeId|string(uuid)|false|none|none|
|»»»» createdDateTimeUtc|string(date-time)|false|none|none|
|»»» isDeleted|boolean|false|none|none|
|»»» nodeId|string(uuid)|false|none|none|
|»»» createdDateTimeUtc|string(date-time)|false|none|none|
|»»» modifiedDateTimeUtc|string(date-time)|false|none|none|
|»» deleteAccount|boolean|false|none|none|
|»» vaultId|string(uuid)¦null|false|none|none|
|»» vaultInfo|string¦null|false|none|none|
|»» logonUrl|string¦null|false|none|none|
|»» isDefault|boolean|false|none|none|
|»» isDeleted|boolean|false|none|none|
|»» isUserModified|boolean|false|none|none|
|»» nodeId|string(uuid)|false|none|none|
|»» createdDateTimeUtc|string(date-time)|false|none|none|
|»» modifiedDateTimeUtc|string(date-time)|false|none|none|
|» activityConfiguration|string¦null|false|none|none|
|» activityConfigurationMaxSessionLength|integer(int32)¦null|false|none|none|
|» activityConfigurationId|string(uuid)¦null|false|none|none|
|» activityGroups|[[SbPAM.Models.ActivityGroup](../Models/sbpam.models.activitygroup.md)]¦null|false|none|none|
|» activityGroupIds|[string]¦null|false|none|none|

#### Enumerated Values

|Property|Value|
|---|---|
|approvalTypeRequired|Deny|
|approvalTypeRequired|Allow|
|approvalTypeRequired|Workflow|
|policyType|Resource|
|policyType|Credential|
|type|Generic|
|type|ConnectionProfile|
|type|EmailSettings|
|type|System|
|type|String|
|type|Integer|
|type|UnsignedInteger|
|type|Boolean|
|type|Guid|
|customFieldDataType|Integer|
|customFieldDataType|String|
|customFieldDataType|Options|
|approvalTypeRequired|Deny|
|approvalTypeRequired|Allow|
|approvalTypeRequired|Workflow|
|mustEndWith|None|
|mustEndWith|Lowercase|
|mustEndWith|Uppercase|
|mustEndWith|Numeric|
|mustEndWith|Symbol|
|mustEndWith|Space|
|mustStartWith|None|
|mustStartWith|Lowercase|
|mustStartWith|Uppercase|
|mustStartWith|Numeric|
|mustStartWith|Symbol|
|mustStartWith|Space|
|type|Password|
|type|Samaccountname|
|type|Unspecified|
|type|Cloud|
|type|Database|
|activityType|Interactive|
|activityType|InteractiveAppLaunch|
|activityType|TaskAutomation|
|activityType|CredentialRelease|
|loginAccount|Requester|
|loginAccount|Managed|
|loginAccount|ActivityIdentity|
|loginAccount|Vault|
|loginAccount|Resource|
|requesterLoginFormat|Samaccountname|
|requesterLoginFormat|UPN|
|requesterLoginFormat|Email|
|requesterLoginFormat|SamAccountNameOnly|
|requesterLoginFormat|Custom|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
Bearer
</aside>


