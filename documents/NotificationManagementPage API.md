# CurrentInventoryManagementPage API 

### 1. CurrentInventoryManagementPage TableDataTitle Annotation Explanation Korean -> Chinese

사이즈: size

재고: inventory amount

폼목: itemName

### 2. CurrentInventoryManagementPage Interfaecs

#### 2.1 url

/api/GetEasyUIDataGridListData

#### 2.2 method

get

#### 2.3 Params

| Param Name   | Param Type | Required | Value                                                   |
| ------------ | ---------- | -------- | ------------------------------------------------------- |
| datagridName | String     | True     | CurrentInventoryManagementPage_CurrentInventoryDataGrid |
| contractID   | String     | True     | The 'id' value of selectedSeason                        |
| itemName     | String     | True     | The 'itemName' value of selectedItemName                |

#### 2.4 Return Results Example

```json
{
    status:false,
    results:[],
	errrorMessage:'System is updating'
}
or
{
    status:true,
    results:[
    			{
    				사이즈:'77L',
    				재고:'209',
                    폼목:'jacket'
				}
			],
	errrorMessage:''
}
```