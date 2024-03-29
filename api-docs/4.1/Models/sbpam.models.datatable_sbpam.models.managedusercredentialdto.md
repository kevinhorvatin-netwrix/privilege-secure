
<h2 id="tocS_SbPAM.Models.DataTable[SbPAM.Models.ManagedUserCredentialDto]">SbPAM.Models.DataTable[SbPAM.Models.ManagedUserCredentialDto]</h2>

<a id="schemasbpam.models.datatable[sbpam.models.managedusercredentialdto]"></a>
<a id="schema_SbPAM.Models.DataTable[SbPAM.Models.ManagedUserCredentialDto]"></a>
<a id="tocSsbpam.models.datatable[sbpam.models.managedusercredentialdto]"></a>
<a id="tocssbpam.models.datatable[sbpam.models.managedusercredentialdto]"></a>

```json
{
  "data": [
    {
      "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
      "credentialId": "f568fec0-10b6-4b94-9daf-e62c50c9bf3e",
      "managedResourceId": "43aaf5a7-e929-49e6-870e-49d47d9cdc2f",
      "name": "string",
      "username": "string",
      "password": "string",
      "managedType": "NotManaged",
      "createdDateTimeUtc": "2019-08-24T14:15:22Z"
    }
  ],
  "recordsTotal": 0
}

```

Generic container for the output of some API endpoints and .Search() 
methods in some actors that return paged subsets of filtered search results

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|data|[[SbPAM.Models.ManagedUserCredentialDto](../Models/sbpam.models.managedusercredentialdto.md)]¦null|false|none|A subset of the filtered, sorted, and paged (e.g., rows 30 - 39 of <br>589 found) search results|
|recordsTotal|integer(int32)|false|none|What is the total count of search results that .DataRows may only <br>be a paged subset of (e.g., rows 30 - 39 of 589 found)|

