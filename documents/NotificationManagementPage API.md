# NotificationManagementPage API 

### 1. NotificationManagementPage NotificationDataGrid Annotation Explanation Korean -> Chinese

공지사황: notification

날짜: date

폼목: itemName

### 2. NotificationManagementPage_NotificationDataGrid Interfaecs

#### 2.1 url

/api/GetEasyUIDataGridListData

#### 2.2 method

get

#### 2.3 Params

| Param Name   | Param Type | Required | Value                                           |
| ------------ | ---------- | -------- | ----------------------------------------------- |
| datagridName | String     | True     | NotificationManagementPage_NotificationDataGrid |

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
    				id:'1'
                    title:'Company Meeting Date',
    				createdDate:'2019-10-10',
                    content:'........'
				}
			],
	errrorMessage:''
}
```