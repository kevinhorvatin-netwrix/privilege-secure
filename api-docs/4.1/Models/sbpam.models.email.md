
<h2 id="tocS_SbPAM.Models.Email">SbPAM.Models.Email</h2>

<a id="schemasbpam.models.email"></a>
<a id="schema_SbPAM.Models.Email"></a>
<a id="tocSsbpam.models.email"></a>
<a id="tocssbpam.models.email"></a>

<details><summary>JSON</summary>


```json
{
  "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
  "expiresDateTimeUtc": "2019-08-24T14:15:22Z",
  "emailSettingsId": "f97b605c-a258-4007-967b-14f8a52c230d",
  "emailSettings": {
    "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
    "name": "string",
    "description": "string",
    "sendNotification": true,
    "useTls": true,
    "useAuth": true,
    "smtpHost": "string",
    "smtpPort": 0,
    "fromAddress": "string",
    "credentialId": "f568fec0-10b6-4b94-9daf-e62c50c9bf3e",
    "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177",
    "createdDateTimeUtc": "2019-08-24T14:15:22Z",
    "modifiedDateTimeUtc": "2019-08-24T14:15:22Z"
  },
  "subject": "string",
  "toAddress": "string",
  "htmlBody": "string",
  "importance": "Low",
  "priority": "NonUrgent",
  "wasSent": true,
  "sentDateTimeUtc": "2019-08-24T14:15:22Z",
  "attachmentPath": "string",
  "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177",
  "createdDateTimeUtc": "2019-08-24T14:15:22Z",
  "modifiedDateTimeUtc": "2019-08-24T14:15:22Z"
}

```


</details>

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|string(uuid)|false|none|none|
|expiresDateTimeUtc|string(date-time)¦null|false|none|none|
|emailSettingsId|string(uuid)¦null|false|none|none|
|emailSettings|[SbPAM.Models.EmailSettings](../Models/sbpam.models.emailsettings.md)|false|none|none|
|subject|string¦null|false|none|none|
|toAddress|string¦null|false|none|none|
|htmlBody|string¦null|false|none|none|
|importance|[SbPAM.Models.ImportanceEnums](../Models/sbpam.models.importanceenums.md)|false|none|none|
|priority|[SbPAM.Models.PriorityEnums](../Models/sbpam.models.priorityenums.md)|false|none|none|
|wasSent|boolean|false|none|none|
|sentDateTimeUtc|string(date-time)¦null|false|none|none|
|attachmentPath|string¦null|false|none|none|
|nodeId|string(uuid)|false|none|none|
|createdDateTimeUtc|string(date-time)|false|none|none|
|modifiedDateTimeUtc|string(date-time)|false|none|none|


