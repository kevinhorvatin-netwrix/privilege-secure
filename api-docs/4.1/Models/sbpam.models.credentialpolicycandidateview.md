
<h2 id="tocS_SbPAM.Models.CredentialPolicyCandidateView">SbPAM.Models.CredentialPolicyCandidateView</h2>

<a id="schemasbpam.models.credentialpolicycandidateview"></a>
<a id="schema_SbPAM.Models.CredentialPolicyCandidateView"></a>
<a id="tocSsbpam.models.credentialpolicycandidateview"></a>
<a id="tocssbpam.models.credentialpolicycandidateview"></a>

<details><summary>JSON</summary>


```json
{
  "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
  "username": "string",
  "name": "string",
  "description": "string",
  "domain": "string",
  "userId": "2c4a230c-5085-4924-a3e1-25fb4fc5965b",
  "os": "string",
  "activeSessionCount": 0,
  "entityType": "Credential",
  "vaultConnectorId": "da5bc90a-dbcd-442c-91be-be4204003524"
}

```


</details>

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|string(uuid)|false|none|none|
|username|string¦null|false|none|none|
|name|string¦null|false|none|none|
|description|string¦null|false|none|none|
|domain|string¦null|false|none|none|
|userId|string(uuid)¦null|false|none|none|
|os|string¦null|false|none|none|
|activeSessionCount|integer(int32)|false|none|none|
|entityType|[SbPAM.Models.CredentialOrHostUser](../Models/sbpam.models.credentialorhostuser.md)|false|none|none|
|vaultConnectorId|string(uuid)¦null|false|none|none|


