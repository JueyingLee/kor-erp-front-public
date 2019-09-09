# NotificationManagementPage API 

### 1. NotificationManagementPage NotificationDataGrid Annotation Explanation Korean -> Chinese

공지사황: notification

날짜: date

공지 기간: Notification Period

### 2. NotificationManagementPage_NotificationAddEditorData Interfaecs

#### 2.1 url

/api/notificationManagement/addEditorData/

#### 2.2 method

post

#### 2.3 Params

| Param Name      | Param Type | Required | Value                |
| --------------- | ---------- | -------- | -------------------- |
| createdby       | String     | True     | name of login person |
| title           | String     | True     | edited title         |
| content         | String     | True     | edited content       |
| noticestart     | Date       | True     | chosen date          |
| noticeend       | Date       | True     | chosen date          |
| createddatetime | Date       | True     | system time          |

#### 2.4 Return Results Example

```json
{
    status:false,
	message:'The format of title is not correct'
}
or
{
    status:true,
    message:'Successfully submit'
}
```

### 3. NotificationManagementPage_NotificationQueryDataList Interfaecs

#### 3.1 url

/api/notificationManagement/queryDataList/

#### 3.2 method

get

#### 3.3 Params

| Param Name | Param Type | Required | Value |
| ---------- | ---------- | -------- | ----- |
|            |            |          |       |

#### 3.4 Return Results Example

