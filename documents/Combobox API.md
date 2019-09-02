# Combobox Interfaces

## 1.년도 [select] year

#### 1.1 url

/api/GetEasyUIComboboxData

#### 1.2 method

get

#### 1.3 Params

| Param Name   | Param Type | Required | Value                       |
| ------------ | ---------- | -------- | --------------------------- |
| comboboxName | String     | True     | ContractDataComboboxService |

#### 1.4 Return Results Example

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
    				id:'2018',
    				text;'2018'
				}
			],
	errrorMessage:''
}
```

## 2.거래처명  (select) [contrctCustomer]

#### 2.1 url

/api/GetEasyUIComboboxData

#### 2.2 method

get

#### 2.3 Params

| Param Name   | Param Type | Required | Value                       |
| ------------ | ---------- | -------- | --------------------------- |
| comboboxName | String     | True     | ContractDataComboboxService |
| year         | String     | True     | The value of selectedYear   |

#### 2.4 Return Results Example

```json
{
    status:false,
	errrorMessage:'System is updating'
}
or
{
    status:true,
    results:[
    			{
    				id:'1',
    				text;'Hana Bank'
				}
			],
}
```

## 3.시즌  (select) [season]

#### 3.1 url

/api/GetEasyUIComboboxData

#### 3.2 method

get

#### 3.3 Params

| Param Name   | Param Type | Required | Value                                 |
| ------------ | ---------- | -------- | ------------------------------------- |
| comboboxName | String     | True     | ContractDataComboboxService           |
| year         | String     | True     | The value of selectedYear             |
| contractName | String     | True     | The value of selectedContractCustomer |

#### 3.4 Return Results Example

```json
{
    status:false,
	errrorMessage:'System is updating'
}
or
{
    status:true,
    results:[
    			{
    				id:'3',
    				text;'Spring'
				}
			],
}
```

## 4.부서명  (select) [departmentName]

#### 4.1 url

/api/GetEasyUIComboboxData

#### 4.2 method

get

#### 4.3 Params

| Param Name   | Param Type | Required | Value                                        |
| ------------ | ---------- | -------- | -------------------------------------------- |
| comboboxName | String     | True     | CustomerAddressDepartmentNameComboboxService |
| contractID   | String     | True     | The 'id' value of selectedSeason             |

#### 4.4 Return Results Example

```json
{
    status:false,
	errrorMessage:'System is updating'
}
or
{
    status:true,
    results:[
    			{
    				valueField:'3',
    				textField;'Adminstrator Derpartment'
				}
			],
}
```

## 5.소속명  (select) [teamName]

#### 5.1 url

/api/GetEasyUIComboboxData

#### 5.2 method

get

#### 5.3 Params

| Param Name     | Param Type | Required | Value                                           |
| -------------- | ---------- | -------- | ----------------------------------------------- |
| comboboxName   | String     | True     | CustomerAddressTeamNameComboboxService          |
| contractID     | String     | True     | The 'id' value of selectedSeason                |
| departmentName | String     | True     | the 'textField' value of selectedDepartmentName |

#### 5.4 Return Results Example

```json
{
    status:false,
	errrorMessage:'System is updating'
}
or
{
    status:true,
    results:[
    			{
    				valueField:'3',
    				textField;'Adminstrator Team'
				}
			],
}
```

## 6.아이템명(select) [ItemName]

#### 6.1 url

/api/GetEasyUIComboboxData

#### 6.2 method

get

#### 6.3 Params

| Param Name   | Param Type | Required | Value                                                        |
| ------------ | ---------- | -------- | ------------------------------------------------------------ |
| comboboxName | String     | True     | CurrentInventoryManagementPage_CurrentInventoryDataGrid_Toolbar_Combobox_ItemName |
| contractID   | String     | True     | The 'id' value of selectedSeason                             |

#### 6.4 Return Results Example

```json
{
    status:false,
	errrorMessage:'This Item is not existed'
}
or
{
    status:true,
    results:[
    			{
    				contractID:'8',
    				id;'72',
                    itemName:'jacket
				}
			],
}
```

