
<h2 id="tocS_SbPAM.Models.HostScanJobRequest">SbPAM.Models.HostScanJobRequest</h2>

<a id="schemasbpam.models.hostscanjobrequest"></a>
<a id="schema_SbPAM.Models.HostScanJobRequest"></a>
<a id="tocSsbpam.models.hostscanjobrequest"></a>
<a id="tocssbpam.models.hostscanjobrequest"></a>

<details><summary>JSON</summary>


```json
{
  "dnsHostName": "string",
  "ipAddress": "string",
  "os": "string",
  "credentialId": "f568fec0-10b6-4b94-9daf-e62c50c9bf3e",
  "credentialName": "string",
  "platformName": "string",
  "acceptThumbprintOnFirstDiscovery": true,
  "sshTrustActionType": null,
  "certificateType": null,
  "trustedThumbprint": "string",
  "sshPort": 0,
  "source": "string"
}

```


</details>

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|dnsHostName|string¦null|false|none|none|
|ipAddress|string¦null|false|none|none|
|os|string¦null|false|none|none|
|credentialId|string(uuid)|false|none|none|
|credentialName|string¦null|false|none|none|
|platformName|string¦null|false|none|none|
|acceptThumbprintOnFirstDiscovery|boolean|false|none|none|
|sshTrustActionType|[SbPAM.Constants.SshConstants+SshTrustActionType](../Models/sbpam.constants.sshconstants+sshtrustactiontype.md)|false|none|none|
|certificateType|[SbPAM.Constants.SshConstants+CertificateType](../Models/sbpam.constants.sshconstants+certificatetype.md)|false|none|none|
|trustedThumbprint|string¦null|false|none|none|
|sshPort|integer(int32)¦null|false|none|none|
|source|string¦null|false|none|none|


