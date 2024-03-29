
<h2 id="tocS_SbPAM.Models.DataTable[System.String]">SbPAM.Models.DataTable[System.String]</h2>

<a id="schemasbpam.models.datatable[system.string]"></a>
<a id="schema_SbPAM.Models.DataTable[System.String]"></a>
<a id="tocSsbpam.models.datatable[system.string]"></a>
<a id="tocssbpam.models.datatable[system.string]"></a>

```json
{
  "data": [
    "string"
  ],
  "recordsTotal": 0
}

```

Generic container for the output of some API endpoints and .Search() 
methods in some actors that return paged subsets of filtered search results

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|data|[string]¦null|false|none|A subset of the filtered, sorted, and paged (e.g., rows 30 - 39 of <br>589 found) search results|
|recordsTotal|integer(int32)|false|none|What is the total count of search results that .DataRows may only <br>be a paged subset of (e.g., rows 30 - 39 of 589 found)|

