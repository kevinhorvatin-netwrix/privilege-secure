
<h2 id="tocS_SbPAM.ActiveDirectory.Models.ActiveDirectoryDomainConfiguration">SbPAM.ActiveDirectory.Models.ActiveDirectoryDomainConfiguration</h2>

<a id="schemasbpam.activedirectory.models.activedirectorydomainconfiguration"></a>
<a id="schema_SbPAM.ActiveDirectory.Models.ActiveDirectoryDomainConfiguration"></a>
<a id="tocSsbpam.activedirectory.models.activedirectorydomainconfiguration"></a>
<a id="tocssbpam.activedirectory.models.activedirectorydomainconfiguration"></a>

<details><summary>JSON</summary>


```json
{
  "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
  "activeDirectoryDomain": [
    {
      "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
      "name": "string",
      "domainName": "string",
      "netBiosName": "string",
      "domainController": "string",
      "usnChanged": 0,
      "activeDirectoryDomainConfigurationId": "49888c94-0f98-4f12-afa0-6d4c13cf7f38",
      "activeDirectoryDomainConfiguration": {
        "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
        "activeDirectoryDomain": [],
        "name": "string",
        "controllers": [
          {
            "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
            "name": "string",
            "activeDirectoryDomain": {},
            "activeDirectoryDomainConfigurationId": "49888c94-0f98-4f12-afa0-6d4c13cf7f38",
            "activeDirectoryDomainConfiguration": {},
            "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177",
            "createdDateTimeUtc": "2019-08-24T14:15:22Z",
            "modifiedDateTimeUtc": "2019-08-24T14:15:22Z"
          }
        ],
        "enabled": true,
        "credentialId": "f568fec0-10b6-4b94-9daf-e62c50c9bf3e",
        "useSsl": true,
        "functionalLevel": "string",
        "syncActionQueueId": "52e1c928-ebc8-4a61-b81e-9a896250c15a",
        "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177",
        "createdDateTimeUtc": "2019-08-24T14:15:22Z",
        "modifiedDateTimeUtc": "2019-08-24T14:15:22Z"
      },
      "functionalLevel": "string",
      "activeDirectoryGroup": [
        {
          "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
          "samaccountname": "string",
          "usnchanged": 0,
          "description": "string",
          "distinguishedName": "string",
          "displayName": "string",
          "email": "string",
          "added": "2019-08-24T14:15:22Z",
          "groupToken": "string",
          "activeDirectoryGroupHostUser": [
            {
              "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
              "groupId": "eb54e96e-21b8-4f54-9cd4-80fccbd06f55",
              "memberId": "92983ab9-49c8-444b-85ae-6e40402cf72e",
              "group": {},
              "member": {
                "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
                "activeDirectoryObjectId": "c323cc1a-aecb-4eb0-9599-286516de7e9f",
                "activeDirectoryDomainId": "c9151464-b069-4770-b7ea-a1f6e23f2428",
                "activeDirectoryDomain": {},
                "displayName": "string",
                "enabled": true,
                "unixId": 0,
                "unixGroupId": 0,
                "homeDirectory": "string",
                "shell": "string",
                "expirationDate": "2019-08-24T14:15:22Z",
                "managed": true,
                "hostId": "70e3fb2d-1cb6-4dbc-ab8d-fa7209aca5dd",
                "host": {
                  "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
                  "activeDirectoryObjectId": "c323cc1a-aecb-4eb0-9599-286516de7e9f",
                  "name": "string",
                  "distinguishedName": "string",
                  "ipAddress": "string",
                  "os": "string",
                  "version": "string",
                  "lsaLookupCache": "string",
                  "lastUpdatedDateTimeUtc": "2019-08-24T14:15:22Z",
                  "credentialId": "f568fec0-10b6-4b94-9daf-e62c50c9bf3e",
                  "hasSSH": true,
                  "activeDirectoryDomainId": "c9151464-b069-4770-b7ea-a1f6e23f2428",
                  "activeDirectoryDomain": {},
                  "dnsHostName": "string",
                  "netBiosName": "string",
                  "users": [
                    {}
                  ],
                  "groups": [
                    {}
                  ],
                  "features": [
                    {}
                  ],
                  "services": [
                    {}
                  ],
                  "scheduledTasks": [
                    {}
                  ],
                  "databases": [
                    {}
                  ],
                  "databaseDbs": [
                    {}
                  ],
                  "databaseRoles": [
                    {}
                  ],
                  "samaccountname": "string",
                  "isDomainController": true,
                  "isGlobalCatalog": true,
                  "usnChanged": 0,
                  "objectSid": "string",
                  "added": "2019-08-24T14:15:22Z",
                  "deleted": true,
                  "isVirtual": true,
                  "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177",
                  "createdDateTimeUtc": "2019-08-24T14:15:22Z",
                  "modifiedDateTimeUtc": "2019-08-24T14:15:22Z"
                },
                "primaryGroupTokenId": 0,
                "primaryGroupToken": "string",
                "managerSamaccountname": "string",
                "title": "string",
                "samaccountname": "string",
                "userPrincipalName": "string",
                "distinguishedName": "string",
                "department": "string",
                "email": "string",
                "lastLogonTimestamp": "2019-08-24T14:15:22Z",
                "name": "string",
                "sid": "string",
                "firstName": "string",
                "lastName": "string",
                "passwordHash": "string",
                "passwordChangedDateTimeUtc": "2019-08-24T14:15:22Z",
                "passwordExpirationDateTimeUtc": "2019-08-24T14:15:22Z",
                "forcePasswordReset": true,
                "privilege": "NotSet",
                "hostUserGroupJoin": [
                  {
                    "userId": "2c4a230c-5085-4924-a3e1-25fb4fc5965b",
                    "user": {},
                    "groupId": "eb54e96e-21b8-4f54-9cd4-80fccbd06f55",
                    "group": {},
                    "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177",
                    "createdDateTimeUtc": "2019-08-24T14:15:22Z",
                    "modifiedDateTimeUtc": "2019-08-24T14:15:22Z"
                  }
                ],
                "hostDatabaseDbs": [
                  {
                    "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
                    "name": "string",
                    "databaseId": "string",
                    "ownerSid": "string",
                    "createDate": "2019-08-24T14:15:22Z",
                    "isOnline": true,
                    "statusDesc": "string",
                    "discoveredDateTimeUtc": "2019-08-24T14:15:22Z",
                    "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177",
                    "createdDateTimeUtc": "2019-08-24T14:15:22Z",
                    "modifiedDateTimeUtc": "2019-08-24T14:15:22Z",
                    "hostId": "70e3fb2d-1cb6-4dbc-ab8d-fa7209aca5dd",
                    "host": {},
                    "hostUsers": [],
                    "hostGroups": [],
                    "hostDbRoles": []
                  }
                ],
                "hostDatabaseRoles": [
                  {
                    "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
                    "name": "string",
                    "sid": "string",
                    "principalId": "string",
                    "createDate": "2019-08-24T14:15:22Z",
                    "modifyDate": "2019-08-24T14:15:22Z",
                    "isDisabled": true,
                    "discoveredDateTimeUtc": "2019-08-24T14:15:22Z",
                    "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177",
                    "createdDateTimeUtc": "2019-08-24T14:15:22Z",
                    "modifiedDateTimeUtc": "2019-08-24T14:15:22Z",
                    "hostId": "70e3fb2d-1cb6-4dbc-ab8d-fa7209aca5dd",
                    "host": {},
                    "databaseDbId": "d22cd8c7-805e-41c1-a1bf-78c5aefa7a36",
                    "databaseDb": {},
                    "hostUsers": [],
                    "hostGroups": []
                  }
                ],
                "deleted": true,
                "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177",
                "createdDateTimeUtc": "2019-08-24T14:15:22Z",
                "modifiedDateTimeUtc": "2019-08-24T14:15:22Z"
              },
              "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177",
              "createdDateTimeUtc": "2019-08-24T14:15:22Z",
              "modifiedDateTimeUtc": "2019-08-24T14:15:22Z"
            }
          ],
          "activeDirectoryGroupGroupGroup": [
            {
              "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
              "memberId": "92983ab9-49c8-444b-85ae-6e40402cf72e",
              "group": {},
              "member": {},
              "groupId": "eb54e96e-21b8-4f54-9cd4-80fccbd06f55",
              "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177",
              "createdDateTimeUtc": "2019-08-24T14:15:22Z",
              "modifiedDateTimeUtc": "2019-08-24T14:15:22Z"
            }
          ],
          "activeDirectoryGroupGroupMember": [
            {
              "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
              "memberId": "92983ab9-49c8-444b-85ae-6e40402cf72e",
              "group": {},
              "member": {},
              "groupId": "eb54e96e-21b8-4f54-9cd4-80fccbd06f55",
              "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177",
              "createdDateTimeUtc": "2019-08-24T14:15:22Z",
              "modifiedDateTimeUtc": "2019-08-24T14:15:22Z"
            }
          ],
          "activeDirectoryDomainId": "c9151464-b069-4770-b7ea-a1f6e23f2428",
          "activeDirectoryDomain": {},
          "groupTokenId": 0,
          "name": "string",
          "sid": "string",
          "hostGroupGroupJoins": [
            {
              "hostGroupId": "16b77703-e101-4cf4-94d3-1264fcec3596",
              "hostGroup": {
                "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
                "name": "string",
                "sid": "string",
                "unixId": 0,
                "hostId": "70e3fb2d-1cb6-4dbc-ab8d-fa7209aca5dd",
                "host": {
                  "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
                  "activeDirectoryObjectId": "c323cc1a-aecb-4eb0-9599-286516de7e9f",
                  "name": "string",
                  "distinguishedName": "string",
                  "ipAddress": "string",
                  "os": "string",
                  "version": "string",
                  "lsaLookupCache": "string",
                  "lastUpdatedDateTimeUtc": "2019-08-24T14:15:22Z",
                  "credentialId": "f568fec0-10b6-4b94-9daf-e62c50c9bf3e",
                  "hasSSH": true,
                  "activeDirectoryDomainId": "c9151464-b069-4770-b7ea-a1f6e23f2428",
                  "activeDirectoryDomain": {},
                  "dnsHostName": "string",
                  "netBiosName": "string",
                  "users": [
                    {}
                  ],
                  "groups": [
                    {}
                  ],
                  "features": [
                    {}
                  ],
                  "services": [
                    {}
                  ],
                  "scheduledTasks": [
                    {}
                  ],
                  "databases": [
                    {}
                  ],
                  "databaseDbs": [
                    {}
                  ],
                  "databaseRoles": [
                    {}
                  ],
                  "samaccountname": "string",
                  "isDomainController": true,
                  "isGlobalCatalog": true,
                  "usnChanged": 0,
                  "objectSid": "string",
                  "added": "2019-08-24T14:15:22Z",
                  "deleted": true,
                  "isVirtual": true,
                  "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177",
                  "createdDateTimeUtc": "2019-08-24T14:15:22Z",
                  "modifiedDateTimeUtc": "2019-08-24T14:15:22Z"
                },
                "hostUserGroupJoin": [
                  {
                    "userId": "2c4a230c-5085-4924-a3e1-25fb4fc5965b",
                    "user": {},
                    "groupId": "eb54e96e-21b8-4f54-9cd4-80fccbd06f55",
                    "group": {},
                    "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177",
                    "createdDateTimeUtc": "2019-08-24T14:15:22Z",
                    "modifiedDateTimeUtc": "2019-08-24T14:15:22Z"
                  }
                ],
                "hostGroupGroupJoins": [
                  {}
                ],
                "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177",
                "createdDateTimeUtc": "2019-08-24T14:15:22Z",
                "modifiedDateTimeUtc": "2019-08-24T14:15:22Z"
              },
              "domainGroupMemberId": "8308c9e0-575d-45d1-8ff0-a4708ed268d5",
              "domainGroupMember": {}
            }
          ],
          "deleted": true,
          "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177",
          "createdDateTimeUtc": "2019-08-24T14:15:22Z",
          "modifiedDateTimeUtc": "2019-08-24T14:15:22Z"
        }
      ],
      "objectSid": "string",
      "maxRenewAge": 0,
      "maxTicketAge": 0,
      "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177",
      "createdDateTimeUtc": "2019-08-24T14:15:22Z",
      "modifiedDateTimeUtc": "2019-08-24T14:15:22Z"
    }
  ],
  "name": "string",
  "controllers": [
    {
      "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
      "name": "string",
      "activeDirectoryDomain": {
        "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
        "name": "string",
        "domainName": "string",
        "netBiosName": "string",
        "domainController": "string",
        "usnChanged": 0,
        "activeDirectoryDomainConfigurationId": "49888c94-0f98-4f12-afa0-6d4c13cf7f38",
        "activeDirectoryDomainConfiguration": {
          "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
          "activeDirectoryDomain": [
            {}
          ],
          "name": "string",
          "controllers": [],
          "enabled": true,
          "credentialId": "f568fec0-10b6-4b94-9daf-e62c50c9bf3e",
          "useSsl": true,
          "functionalLevel": "string",
          "syncActionQueueId": "52e1c928-ebc8-4a61-b81e-9a896250c15a",
          "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177",
          "createdDateTimeUtc": "2019-08-24T14:15:22Z",
          "modifiedDateTimeUtc": "2019-08-24T14:15:22Z"
        },
        "functionalLevel": "string",
        "activeDirectoryGroup": [
          {
            "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
            "samaccountname": "string",
            "usnchanged": 0,
            "description": "string",
            "distinguishedName": "string",
            "displayName": "string",
            "email": "string",
            "added": "2019-08-24T14:15:22Z",
            "groupToken": "string",
            "activeDirectoryGroupHostUser": [
              {
                "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
                "groupId": "eb54e96e-21b8-4f54-9cd4-80fccbd06f55",
                "memberId": "92983ab9-49c8-444b-85ae-6e40402cf72e",
                "group": {},
                "member": {
                  "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
                  "activeDirectoryObjectId": "c323cc1a-aecb-4eb0-9599-286516de7e9f",
                  "activeDirectoryDomainId": "c9151464-b069-4770-b7ea-a1f6e23f2428",
                  "activeDirectoryDomain": {},
                  "displayName": "string",
                  "enabled": true,
                  "unixId": 0,
                  "unixGroupId": 0,
                  "homeDirectory": "string",
                  "shell": "string",
                  "expirationDate": "2019-08-24T14:15:22Z",
                  "managed": true,
                  "hostId": "70e3fb2d-1cb6-4dbc-ab8d-fa7209aca5dd",
                  "host": {
                    "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
                    "activeDirectoryObjectId": "c323cc1a-aecb-4eb0-9599-286516de7e9f",
                    "name": "string",
                    "distinguishedName": "string",
                    "ipAddress": "string",
                    "os": "string",
                    "version": "string",
                    "lsaLookupCache": "string",
                    "lastUpdatedDateTimeUtc": "2019-08-24T14:15:22Z",
                    "credentialId": "f568fec0-10b6-4b94-9daf-e62c50c9bf3e",
                    "hasSSH": true,
                    "activeDirectoryDomainId": "c9151464-b069-4770-b7ea-a1f6e23f2428",
                    "activeDirectoryDomain": {},
                    "dnsHostName": "string",
                    "netBiosName": "string",
                    "users": [],
                    "groups": [],
                    "features": [],
                    "services": [],
                    "scheduledTasks": [],
                    "databases": [],
                    "databaseDbs": [],
                    "databaseRoles": [],
                    "samaccountname": "string",
                    "isDomainController": true,
                    "isGlobalCatalog": true,
                    "usnChanged": 0,
                    "objectSid": "string",
                    "added": "2019-08-24T14:15:22Z",
                    "deleted": true,
                    "isVirtual": true,
                    "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177",
                    "createdDateTimeUtc": "2019-08-24T14:15:22Z",
                    "modifiedDateTimeUtc": "2019-08-24T14:15:22Z"
                  },
                  "primaryGroupTokenId": 0,
                  "primaryGroupToken": "string",
                  "managerSamaccountname": "string",
                  "title": "string",
                  "samaccountname": "string",
                  "userPrincipalName": "string",
                  "distinguishedName": "string",
                  "department": "string",
                  "email": "string",
                  "lastLogonTimestamp": "2019-08-24T14:15:22Z",
                  "name": "string",
                  "sid": "string",
                  "firstName": "string",
                  "lastName": "string",
                  "passwordHash": "string",
                  "passwordChangedDateTimeUtc": "2019-08-24T14:15:22Z",
                  "passwordExpirationDateTimeUtc": "2019-08-24T14:15:22Z",
                  "forcePasswordReset": true,
                  "privilege": "NotSet",
                  "hostUserGroupJoin": [
                    {}
                  ],
                  "hostDatabaseDbs": [
                    {}
                  ],
                  "hostDatabaseRoles": [
                    {}
                  ],
                  "deleted": true,
                  "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177",
                  "createdDateTimeUtc": "2019-08-24T14:15:22Z",
                  "modifiedDateTimeUtc": "2019-08-24T14:15:22Z"
                },
                "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177",
                "createdDateTimeUtc": "2019-08-24T14:15:22Z",
                "modifiedDateTimeUtc": "2019-08-24T14:15:22Z"
              }
            ],
            "activeDirectoryGroupGroupGroup": [
              {
                "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
                "memberId": "92983ab9-49c8-444b-85ae-6e40402cf72e",
                "group": {},
                "member": {},
                "groupId": "eb54e96e-21b8-4f54-9cd4-80fccbd06f55",
                "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177",
                "createdDateTimeUtc": "2019-08-24T14:15:22Z",
                "modifiedDateTimeUtc": "2019-08-24T14:15:22Z"
              }
            ],
            "activeDirectoryGroupGroupMember": [
              {
                "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
                "memberId": "92983ab9-49c8-444b-85ae-6e40402cf72e",
                "group": {},
                "member": {},
                "groupId": "eb54e96e-21b8-4f54-9cd4-80fccbd06f55",
                "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177",
                "createdDateTimeUtc": "2019-08-24T14:15:22Z",
                "modifiedDateTimeUtc": "2019-08-24T14:15:22Z"
              }
            ],
            "activeDirectoryDomainId": "c9151464-b069-4770-b7ea-a1f6e23f2428",
            "activeDirectoryDomain": {},
            "groupTokenId": 0,
            "name": "string",
            "sid": "string",
            "hostGroupGroupJoins": [
              {
                "hostGroupId": "16b77703-e101-4cf4-94d3-1264fcec3596",
                "hostGroup": {
                  "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
                  "name": "string",
                  "sid": "string",
                  "unixId": 0,
                  "hostId": "70e3fb2d-1cb6-4dbc-ab8d-fa7209aca5dd",
                  "host": {
                    "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
                    "activeDirectoryObjectId": "c323cc1a-aecb-4eb0-9599-286516de7e9f",
                    "name": "string",
                    "distinguishedName": "string",
                    "ipAddress": "string",
                    "os": "string",
                    "version": "string",
                    "lsaLookupCache": "string",
                    "lastUpdatedDateTimeUtc": "2019-08-24T14:15:22Z",
                    "credentialId": "f568fec0-10b6-4b94-9daf-e62c50c9bf3e",
                    "hasSSH": true,
                    "activeDirectoryDomainId": "c9151464-b069-4770-b7ea-a1f6e23f2428",
                    "activeDirectoryDomain": {},
                    "dnsHostName": "string",
                    "netBiosName": "string",
                    "users": [],
                    "groups": [],
                    "features": [],
                    "services": [],
                    "scheduledTasks": [],
                    "databases": [],
                    "databaseDbs": [],
                    "databaseRoles": [],
                    "samaccountname": "string",
                    "isDomainController": true,
                    "isGlobalCatalog": true,
                    "usnChanged": 0,
                    "objectSid": "string",
                    "added": "2019-08-24T14:15:22Z",
                    "deleted": true,
                    "isVirtual": true,
                    "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177",
                    "createdDateTimeUtc": "2019-08-24T14:15:22Z",
                    "modifiedDateTimeUtc": "2019-08-24T14:15:22Z"
                  },
                  "hostUserGroupJoin": [
                    {}
                  ],
                  "hostGroupGroupJoins": [
                    {}
                  ],
                  "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177",
                  "createdDateTimeUtc": "2019-08-24T14:15:22Z",
                  "modifiedDateTimeUtc": "2019-08-24T14:15:22Z"
                },
                "domainGroupMemberId": "8308c9e0-575d-45d1-8ff0-a4708ed268d5",
                "domainGroupMember": {}
              }
            ],
            "deleted": true,
            "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177",
            "createdDateTimeUtc": "2019-08-24T14:15:22Z",
            "modifiedDateTimeUtc": "2019-08-24T14:15:22Z"
          }
        ],
        "objectSid": "string",
        "maxRenewAge": 0,
        "maxTicketAge": 0,
        "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177",
        "createdDateTimeUtc": "2019-08-24T14:15:22Z",
        "modifiedDateTimeUtc": "2019-08-24T14:15:22Z"
      },
      "activeDirectoryDomainConfigurationId": "49888c94-0f98-4f12-afa0-6d4c13cf7f38",
      "activeDirectoryDomainConfiguration": {
        "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
        "activeDirectoryDomain": [
          {
            "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
            "name": "string",
            "domainName": "string",
            "netBiosName": "string",
            "domainController": "string",
            "usnChanged": 0,
            "activeDirectoryDomainConfigurationId": "49888c94-0f98-4f12-afa0-6d4c13cf7f38",
            "activeDirectoryDomainConfiguration": {},
            "functionalLevel": "string",
            "activeDirectoryGroup": [
              {
                "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
                "samaccountname": "string",
                "usnchanged": 0,
                "description": "string",
                "distinguishedName": "string",
                "displayName": "string",
                "email": "string",
                "added": "2019-08-24T14:15:22Z",
                "groupToken": "string",
                "activeDirectoryGroupHostUser": [
                  {
                    "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
                    "groupId": "eb54e96e-21b8-4f54-9cd4-80fccbd06f55",
                    "memberId": "92983ab9-49c8-444b-85ae-6e40402cf72e",
                    "group": {},
                    "member": {},
                    "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177",
                    "createdDateTimeUtc": "2019-08-24T14:15:22Z",
                    "modifiedDateTimeUtc": "2019-08-24T14:15:22Z"
                  }
                ],
                "activeDirectoryGroupGroupGroup": [
                  {
                    "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
                    "memberId": "92983ab9-49c8-444b-85ae-6e40402cf72e",
                    "group": {},
                    "member": {},
                    "groupId": "eb54e96e-21b8-4f54-9cd4-80fccbd06f55",
                    "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177",
                    "createdDateTimeUtc": "2019-08-24T14:15:22Z",
                    "modifiedDateTimeUtc": "2019-08-24T14:15:22Z"
                  }
                ],
                "activeDirectoryGroupGroupMember": [
                  {
                    "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
                    "memberId": "92983ab9-49c8-444b-85ae-6e40402cf72e",
                    "group": {},
                    "member": {},
                    "groupId": "eb54e96e-21b8-4f54-9cd4-80fccbd06f55",
                    "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177",
                    "createdDateTimeUtc": "2019-08-24T14:15:22Z",
                    "modifiedDateTimeUtc": "2019-08-24T14:15:22Z"
                  }
                ],
                "activeDirectoryDomainId": "c9151464-b069-4770-b7ea-a1f6e23f2428",
                "activeDirectoryDomain": {},
                "groupTokenId": 0,
                "name": "string",
                "sid": "string",
                "hostGroupGroupJoins": [
                  {
                    "hostGroupId": "16b77703-e101-4cf4-94d3-1264fcec3596",
                    "hostGroup": {},
                    "domainGroupMemberId": "8308c9e0-575d-45d1-8ff0-a4708ed268d5",
                    "domainGroupMember": {}
                  }
                ],
                "deleted": true,
                "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177",
                "createdDateTimeUtc": "2019-08-24T14:15:22Z",
                "modifiedDateTimeUtc": "2019-08-24T14:15:22Z"
              }
            ],
            "objectSid": "string",
            "maxRenewAge": 0,
            "maxTicketAge": 0,
            "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177",
            "createdDateTimeUtc": "2019-08-24T14:15:22Z",
            "modifiedDateTimeUtc": "2019-08-24T14:15:22Z"
          }
        ],
        "name": "string",
        "controllers": [],
        "enabled": true,
        "credentialId": "f568fec0-10b6-4b94-9daf-e62c50c9bf3e",
        "useSsl": true,
        "functionalLevel": "string",
        "syncActionQueueId": "52e1c928-ebc8-4a61-b81e-9a896250c15a",
        "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177",
        "createdDateTimeUtc": "2019-08-24T14:15:22Z",
        "modifiedDateTimeUtc": "2019-08-24T14:15:22Z"
      },
      "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177",
      "createdDateTimeUtc": "2019-08-24T14:15:22Z",
      "modifiedDateTimeUtc": "2019-08-24T14:15:22Z"
    }
  ],
  "enabled": true,
  "credentialId": "f568fec0-10b6-4b94-9daf-e62c50c9bf3e",
  "useSsl": true,
  "functionalLevel": "string",
  "syncActionQueueId": "52e1c928-ebc8-4a61-b81e-9a896250c15a",
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
|activeDirectoryDomain|[[SbPAM.ActiveDirectory.Models.ActiveDirectoryDomain](../Models/sbpam.activedirectory.models.activedirectorydomain.md)]¦null|false|read-only|none|
|name|string¦null|false|none|none|
|controllers|[[SbPAM.ActiveDirectory.Models.ActiveDirectoryController](../Models/sbpam.activedirectory.models.activedirectorycontroller.md)]¦null|false|read-only|none|
|enabled|boolean|false|none|none|
|credentialId|string(uuid)¦null|false|none|none|
|useSsl|boolean|false|none|none|
|functionalLevel|string¦null|false|none|none|
|syncActionQueueId|string(uuid)¦null|false|none|none|
|nodeId|string(uuid)|false|none|none|
|createdDateTimeUtc|string(date-time)|false|none|none|
|modifiedDateTimeUtc|string(date-time)|false|none|none|


