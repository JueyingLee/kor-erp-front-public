# 数据库表分类

### 1.管理员相关表



|      |      |      |      |      |      |
| ---- | ---- | ---- | ---- | ---- | ---- |
|      |      |      |      |      |      |
|      |      |      |      |      |      |
|      |      |      |      |      |      |

### 2.客户相关表



### 3.公司相关表

#### 3.1 职员表

Table : Employee

| name | mobile | outsideCall | interCall | companyOutIP | companyInterIP | teamName | position | password | workStatus | Department |
| ---- | ------ | ----------- | --------- | ------------ | -------------- | -------- | -------- | -------- | ---------- | ---------- |
|      |        |             |           |              |                |          |          |          |            |            |

Table : CompanyDepartment

| teamName | departName |
| -------- | ---------- |
|          |            |

Table : EmployeePositionList

| PositionName |
| ------------ |
|              |

Table : workStatus

| workStatus |
| ---------- |
| serve      |
| retire     |

Table : EmployeeTokenList



| id   | employeeName | CreatedTime | Token | os   | ip   | device | browser | valid | updatedTime | rememberMe | session |
| ---- | ------------ | ----------- | ----- | ---- | ---- | ------ | ------- | ----- | ----------- | ---------- | ------- |
|      |              |             |       |      |      |        |         |       |             |            |         |



Table: Team_ComponentACL

| Authority | 회사구성팀List_팀명 | Component_id |
| --------- | ------------------- | ------------ |
|           |                     |              |

User_ComponentACL

| Authority | Component_id | 직원명 |
| --------- | ------------ | ------ |
|           |              |        |

AuthenticatedUserIP

| IP   | employeeName |
| ---- | ------------ |
|      |              |

#### 3.2 公司行政业务相关表

Table: Notification

| id   | CreatedDateTime | UpdatedDateTime | Content | NoticeStart | NoticeEnd | CreatedBy | Title | Deleted |
| ---- | --------------- | --------------- | ------- | ----------- | --------- | --------- | ----- | ------- |
|      |                 |                 |         |             |           |           |       |         |

#### 4.文件上传相关表