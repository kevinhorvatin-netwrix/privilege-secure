
<h2 id="tocS_SbPAM.Models.Report">SbPAM.Models.Report</h2>

<a id="schemasbpam.models.report"></a>
<a id="schema_SbPAM.Models.Report"></a>
<a id="tocSsbpam.models.report"></a>
<a id="tocssbpam.models.report"></a>

<details><summary>JSON</summary>


```json
{
  "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
  "name": "string",
  "reportFolder": {
    "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
    "name": "string",
    "reportFolderId": "6201f8bf-2ec3-42b7-937c-91082a4a691a",
    "reports": [
      {
        "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
        "name": "string",
        "reportFolder": {},
        "reportFolderId": "6201f8bf-2ec3-42b7-937c-91082a4a691a",
        "source": {
          "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
          "name": "string",
          "dbSet": "string",
          "reportAttributeTemplateJoins": [
            {
              "reportSourceId": "7ac31b1d-ecbf-43a3-aaf9-c77e7f57dfbe",
              "reportSource": {},
              "reportAttributeTemplateId": "f895b642-4c0a-41db-a175-2812933e6f65",
              "reportAttributeTemplate": {
                "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
                "name": "string",
                "displayName": "string",
                "dataType": "Boolean",
                "type": "User",
                "reportAttributeTemplateJoins": [
                  {}
                ],
                "reportOperatorJoins": [
                  {
                    "reportAttributeTemplateId": "f895b642-4c0a-41db-a175-2812933e6f65",
                    "reportAttributeTemplate": {},
                    "reportOperator": "Equals"
                  }
                ],
                "createdDateTimeUtc": "2019-08-24T14:15:22Z",
                "modifiedDateTimeUtc": "2019-08-24T14:15:22Z",
                "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177"
              },
              "attributeName": "string"
            }
          ],
          "columns": [
            {
              "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
              "reportSourceId": "7ac31b1d-ecbf-43a3-aaf9-c77e7f57dfbe",
              "source": {},
              "name": "string",
              "title": "string",
              "columnOrder": 0,
              "dataType": "string",
              "createdDateTimeUtc": "2019-08-24T14:15:22Z",
              "modifiedDateTimeUtc": "2019-08-24T14:15:22Z",
              "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177"
            }
          ],
          "dateColumn": "string",
          "createdDateTimeUtc": "2019-08-24T14:15:22Z",
          "modifiedDateTimeUtc": "2019-08-24T14:15:22Z",
          "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177"
        },
        "sourceId": "797f5a94-3689-4ac8-82fd-d749511ea2b2",
        "reportAttributes": [
          {
            "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
            "reportId": "836df459-dc40-4aa1-972a-6eb0a864dff9",
            "report": {},
            "reportAttributeTemplateId": "f895b642-4c0a-41db-a175-2812933e6f65",
            "reportAttributeTemplate": {
              "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
              "name": "string",
              "displayName": "string",
              "dataType": "Boolean",
              "type": "User",
              "reportAttributeTemplateJoins": [
                {
                  "reportSourceId": "7ac31b1d-ecbf-43a3-aaf9-c77e7f57dfbe",
                  "reportSource": {
                    "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
                    "name": "string",
                    "dbSet": "string",
                    "reportAttributeTemplateJoins": [],
                    "columns": [],
                    "dateColumn": "string",
                    "createdDateTimeUtc": "2019-08-24T14:15:22Z",
                    "modifiedDateTimeUtc": "2019-08-24T14:15:22Z",
                    "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177"
                  },
                  "reportAttributeTemplateId": "f895b642-4c0a-41db-a175-2812933e6f65",
                  "reportAttributeTemplate": {},
                  "attributeName": "string"
                }
              ],
              "reportOperatorJoins": [
                {
                  "reportAttributeTemplateId": "f895b642-4c0a-41db-a175-2812933e6f65",
                  "reportAttributeTemplate": {},
                  "reportOperator": "Equals"
                }
              ],
              "createdDateTimeUtc": "2019-08-24T14:15:22Z",
              "modifiedDateTimeUtc": "2019-08-24T14:15:22Z",
              "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177"
            },
            "value": "string",
            "operator": "Equals",
            "createdDateTimeUtc": "2019-08-24T14:15:22Z",
            "modifiedDateTimeUtc": "2019-08-24T14:15:22Z",
            "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177"
          }
        ],
        "createdBy": "25a02396-1048-48f9-bf93-102d2fb7895e",
        "reportFavorites": [
          {
            "reportId": "836df459-dc40-4aa1-972a-6eb0a864dff9",
            "report": {},
            "userId": "2c4a230c-5085-4924-a3e1-25fb4fc5965b"
          }
        ],
        "durationType": "LastHour",
        "startDateTimeUtc": "2019-08-24T14:15:22Z",
        "endDateTimeUtc": "2019-08-24T14:15:22Z",
        "createdDateTimeUtc": "2019-08-24T14:15:22Z",
        "modifiedDateTimeUtc": "2019-08-24T14:15:22Z",
        "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177"
      }
    ],
    "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177",
    "createdDateTimeUtc": "2019-08-24T14:15:22Z",
    "modifiedDateTimeUtc": "2019-08-24T14:15:22Z"
  },
  "reportFolderId": "6201f8bf-2ec3-42b7-937c-91082a4a691a",
  "source": {
    "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
    "name": "string",
    "dbSet": "string",
    "reportAttributeTemplateJoins": [
      {
        "reportSourceId": "7ac31b1d-ecbf-43a3-aaf9-c77e7f57dfbe",
        "reportSource": {},
        "reportAttributeTemplateId": "f895b642-4c0a-41db-a175-2812933e6f65",
        "reportAttributeTemplate": {
          "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
          "name": "string",
          "displayName": "string",
          "dataType": "Boolean",
          "type": "User",
          "reportAttributeTemplateJoins": [
            {}
          ],
          "reportOperatorJoins": [
            {
              "reportAttributeTemplateId": "f895b642-4c0a-41db-a175-2812933e6f65",
              "reportAttributeTemplate": {},
              "reportOperator": "Equals"
            }
          ],
          "createdDateTimeUtc": "2019-08-24T14:15:22Z",
          "modifiedDateTimeUtc": "2019-08-24T14:15:22Z",
          "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177"
        },
        "attributeName": "string"
      }
    ],
    "columns": [
      {
        "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
        "reportSourceId": "7ac31b1d-ecbf-43a3-aaf9-c77e7f57dfbe",
        "source": {},
        "name": "string",
        "title": "string",
        "columnOrder": 0,
        "dataType": "string",
        "createdDateTimeUtc": "2019-08-24T14:15:22Z",
        "modifiedDateTimeUtc": "2019-08-24T14:15:22Z",
        "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177"
      }
    ],
    "dateColumn": "string",
    "createdDateTimeUtc": "2019-08-24T14:15:22Z",
    "modifiedDateTimeUtc": "2019-08-24T14:15:22Z",
    "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177"
  },
  "sourceId": "797f5a94-3689-4ac8-82fd-d749511ea2b2",
  "reportAttributes": [
    {
      "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
      "reportId": "836df459-dc40-4aa1-972a-6eb0a864dff9",
      "report": {
        "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
        "name": "string",
        "reportFolder": {
          "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
          "name": "string",
          "reportFolderId": "6201f8bf-2ec3-42b7-937c-91082a4a691a",
          "reports": [
            {}
          ],
          "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177",
          "createdDateTimeUtc": "2019-08-24T14:15:22Z",
          "modifiedDateTimeUtc": "2019-08-24T14:15:22Z"
        },
        "reportFolderId": "6201f8bf-2ec3-42b7-937c-91082a4a691a",
        "source": {
          "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
          "name": "string",
          "dbSet": "string",
          "reportAttributeTemplateJoins": [
            {
              "reportSourceId": "7ac31b1d-ecbf-43a3-aaf9-c77e7f57dfbe",
              "reportSource": {},
              "reportAttributeTemplateId": "f895b642-4c0a-41db-a175-2812933e6f65",
              "reportAttributeTemplate": {
                "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
                "name": "string",
                "displayName": "string",
                "dataType": "Boolean",
                "type": "User",
                "reportAttributeTemplateJoins": [
                  {}
                ],
                "reportOperatorJoins": [
                  {
                    "reportAttributeTemplateId": "f895b642-4c0a-41db-a175-2812933e6f65",
                    "reportAttributeTemplate": {},
                    "reportOperator": "Equals"
                  }
                ],
                "createdDateTimeUtc": "2019-08-24T14:15:22Z",
                "modifiedDateTimeUtc": "2019-08-24T14:15:22Z",
                "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177"
              },
              "attributeName": "string"
            }
          ],
          "columns": [
            {
              "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
              "reportSourceId": "7ac31b1d-ecbf-43a3-aaf9-c77e7f57dfbe",
              "source": {},
              "name": "string",
              "title": "string",
              "columnOrder": 0,
              "dataType": "string",
              "createdDateTimeUtc": "2019-08-24T14:15:22Z",
              "modifiedDateTimeUtc": "2019-08-24T14:15:22Z",
              "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177"
            }
          ],
          "dateColumn": "string",
          "createdDateTimeUtc": "2019-08-24T14:15:22Z",
          "modifiedDateTimeUtc": "2019-08-24T14:15:22Z",
          "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177"
        },
        "sourceId": "797f5a94-3689-4ac8-82fd-d749511ea2b2",
        "reportAttributes": [],
        "createdBy": "25a02396-1048-48f9-bf93-102d2fb7895e",
        "reportFavorites": [
          {
            "reportId": "836df459-dc40-4aa1-972a-6eb0a864dff9",
            "report": {},
            "userId": "2c4a230c-5085-4924-a3e1-25fb4fc5965b"
          }
        ],
        "durationType": "LastHour",
        "startDateTimeUtc": "2019-08-24T14:15:22Z",
        "endDateTimeUtc": "2019-08-24T14:15:22Z",
        "createdDateTimeUtc": "2019-08-24T14:15:22Z",
        "modifiedDateTimeUtc": "2019-08-24T14:15:22Z",
        "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177"
      },
      "reportAttributeTemplateId": "f895b642-4c0a-41db-a175-2812933e6f65",
      "reportAttributeTemplate": {
        "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
        "name": "string",
        "displayName": "string",
        "dataType": "Boolean",
        "type": "User",
        "reportAttributeTemplateJoins": [
          {
            "reportSourceId": "7ac31b1d-ecbf-43a3-aaf9-c77e7f57dfbe",
            "reportSource": {
              "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
              "name": "string",
              "dbSet": "string",
              "reportAttributeTemplateJoins": [
                {}
              ],
              "columns": [
                {
                  "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
                  "reportSourceId": "7ac31b1d-ecbf-43a3-aaf9-c77e7f57dfbe",
                  "source": {},
                  "name": "string",
                  "title": "string",
                  "columnOrder": 0,
                  "dataType": "string",
                  "createdDateTimeUtc": "2019-08-24T14:15:22Z",
                  "modifiedDateTimeUtc": "2019-08-24T14:15:22Z",
                  "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177"
                }
              ],
              "dateColumn": "string",
              "createdDateTimeUtc": "2019-08-24T14:15:22Z",
              "modifiedDateTimeUtc": "2019-08-24T14:15:22Z",
              "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177"
            },
            "reportAttributeTemplateId": "f895b642-4c0a-41db-a175-2812933e6f65",
            "reportAttributeTemplate": {},
            "attributeName": "string"
          }
        ],
        "reportOperatorJoins": [
          {
            "reportAttributeTemplateId": "f895b642-4c0a-41db-a175-2812933e6f65",
            "reportAttributeTemplate": {},
            "reportOperator": "Equals"
          }
        ],
        "createdDateTimeUtc": "2019-08-24T14:15:22Z",
        "modifiedDateTimeUtc": "2019-08-24T14:15:22Z",
        "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177"
      },
      "value": "string",
      "operator": "Equals",
      "createdDateTimeUtc": "2019-08-24T14:15:22Z",
      "modifiedDateTimeUtc": "2019-08-24T14:15:22Z",
      "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177"
    }
  ],
  "createdBy": "25a02396-1048-48f9-bf93-102d2fb7895e",
  "reportFavorites": [
    {
      "reportId": "836df459-dc40-4aa1-972a-6eb0a864dff9",
      "report": {
        "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
        "name": "string",
        "reportFolder": {
          "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
          "name": "string",
          "reportFolderId": "6201f8bf-2ec3-42b7-937c-91082a4a691a",
          "reports": [
            {}
          ],
          "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177",
          "createdDateTimeUtc": "2019-08-24T14:15:22Z",
          "modifiedDateTimeUtc": "2019-08-24T14:15:22Z"
        },
        "reportFolderId": "6201f8bf-2ec3-42b7-937c-91082a4a691a",
        "source": {
          "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
          "name": "string",
          "dbSet": "string",
          "reportAttributeTemplateJoins": [
            {
              "reportSourceId": "7ac31b1d-ecbf-43a3-aaf9-c77e7f57dfbe",
              "reportSource": {},
              "reportAttributeTemplateId": "f895b642-4c0a-41db-a175-2812933e6f65",
              "reportAttributeTemplate": {
                "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
                "name": "string",
                "displayName": "string",
                "dataType": "Boolean",
                "type": "User",
                "reportAttributeTemplateJoins": [
                  {}
                ],
                "reportOperatorJoins": [
                  {
                    "reportAttributeTemplateId": "f895b642-4c0a-41db-a175-2812933e6f65",
                    "reportAttributeTemplate": {},
                    "reportOperator": "Equals"
                  }
                ],
                "createdDateTimeUtc": "2019-08-24T14:15:22Z",
                "modifiedDateTimeUtc": "2019-08-24T14:15:22Z",
                "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177"
              },
              "attributeName": "string"
            }
          ],
          "columns": [
            {
              "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
              "reportSourceId": "7ac31b1d-ecbf-43a3-aaf9-c77e7f57dfbe",
              "source": {},
              "name": "string",
              "title": "string",
              "columnOrder": 0,
              "dataType": "string",
              "createdDateTimeUtc": "2019-08-24T14:15:22Z",
              "modifiedDateTimeUtc": "2019-08-24T14:15:22Z",
              "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177"
            }
          ],
          "dateColumn": "string",
          "createdDateTimeUtc": "2019-08-24T14:15:22Z",
          "modifiedDateTimeUtc": "2019-08-24T14:15:22Z",
          "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177"
        },
        "sourceId": "797f5a94-3689-4ac8-82fd-d749511ea2b2",
        "reportAttributes": [
          {
            "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
            "reportId": "836df459-dc40-4aa1-972a-6eb0a864dff9",
            "report": {},
            "reportAttributeTemplateId": "f895b642-4c0a-41db-a175-2812933e6f65",
            "reportAttributeTemplate": {
              "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
              "name": "string",
              "displayName": "string",
              "dataType": "Boolean",
              "type": "User",
              "reportAttributeTemplateJoins": [
                {
                  "reportSourceId": "7ac31b1d-ecbf-43a3-aaf9-c77e7f57dfbe",
                  "reportSource": {
                    "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
                    "name": "string",
                    "dbSet": "string",
                    "reportAttributeTemplateJoins": [],
                    "columns": [],
                    "dateColumn": "string",
                    "createdDateTimeUtc": "2019-08-24T14:15:22Z",
                    "modifiedDateTimeUtc": "2019-08-24T14:15:22Z",
                    "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177"
                  },
                  "reportAttributeTemplateId": "f895b642-4c0a-41db-a175-2812933e6f65",
                  "reportAttributeTemplate": {},
                  "attributeName": "string"
                }
              ],
              "reportOperatorJoins": [
                {
                  "reportAttributeTemplateId": "f895b642-4c0a-41db-a175-2812933e6f65",
                  "reportAttributeTemplate": {},
                  "reportOperator": "Equals"
                }
              ],
              "createdDateTimeUtc": "2019-08-24T14:15:22Z",
              "modifiedDateTimeUtc": "2019-08-24T14:15:22Z",
              "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177"
            },
            "value": "string",
            "operator": "Equals",
            "createdDateTimeUtc": "2019-08-24T14:15:22Z",
            "modifiedDateTimeUtc": "2019-08-24T14:15:22Z",
            "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177"
          }
        ],
        "createdBy": "25a02396-1048-48f9-bf93-102d2fb7895e",
        "reportFavorites": [],
        "durationType": "LastHour",
        "startDateTimeUtc": "2019-08-24T14:15:22Z",
        "endDateTimeUtc": "2019-08-24T14:15:22Z",
        "createdDateTimeUtc": "2019-08-24T14:15:22Z",
        "modifiedDateTimeUtc": "2019-08-24T14:15:22Z",
        "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177"
      },
      "userId": "2c4a230c-5085-4924-a3e1-25fb4fc5965b"
    }
  ],
  "durationType": "LastHour",
  "startDateTimeUtc": "2019-08-24T14:15:22Z",
  "endDateTimeUtc": "2019-08-24T14:15:22Z",
  "createdDateTimeUtc": "2019-08-24T14:15:22Z",
  "modifiedDateTimeUtc": "2019-08-24T14:15:22Z",
  "nodeId": "959356e3-6168-4a92-b4a5-b9d462be6177"
}

```


</details>

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|string(uuid)|false|none|none|
|name|string¦null|false|none|none|
|reportFolder|[SbPAM.Models.ReportFolder](../Models/sbpam.models.reportfolder.md)|false|none|none|
|reportFolderId|string(uuid)|false|none|none|
|source|[SbPAM.Models.ReportSource](../Models/sbpam.models.reportsource.md)|false|none|none|
|sourceId|string(uuid)|false|none|none|
|reportAttributes|[[SbPAM.Models.ReportAttribute](../Models/sbpam.models.reportattribute.md)]¦null|false|none|none|
|createdBy|string(uuid)¦null|false|none|none|
|reportFavorites|[[SbPAM.Models.ReportFavorite](../Models/sbpam.models.reportfavorite.md)]¦null|false|none|none|
|durationType|[SbPAM.Models.ReportDurationType](../Models/sbpam.models.reportdurationtype.md)|false|none|none|
|startDateTimeUtc|string(date-time)¦null|false|none|none|
|endDateTimeUtc|string(date-time)¦null|false|none|none|
|createdDateTimeUtc|string(date-time)|false|none|none|
|modifiedDateTimeUtc|string(date-time)|false|none|none|
|nodeId|string(uuid)|false|none|none|


