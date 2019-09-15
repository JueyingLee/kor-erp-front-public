# 数据库表分类

### 1.管理员相关表



|      |      |      |      |      |      |
| ---- | ---- | ---- | ---- | ---- | ---- |
|      |      |      |      |      |      |
|      |      |      |      |      |      |
|      |      |      |      |      |      |

### 2.客户公司相关表

#### 2.1 Contract

##### Table: ContractInfo

| id   | contractName | season | year | image | CompanyDepartment_TeamName |
| ---- | ------------ | ------ | ---- | ----- | -------------------------- |
|      |              |        |      |       |                            |

##### Table: ContractDistinction_Address

| contractInfo_Id | departmentName | teamName | address | personInCharge | personInChargeTel | personInChargeMobile |
| --------------- | -------------- | -------- | ------- | -------------- | ----------------- | -------------------- |
|                 |                |          |         |                |                   |                      |



#### 2.2  ContractDistinction_Customer

##### Table: contractDistinction_Customer_Info

| id   | number | name | telephone | contractDistinction_Address_contractInfo_id | contractDistinction_Address_departmentName | contractDistinction_Address_TeamName | sex  | AS  Degree | privatePostAddress | privatePostAddressapply |
| ---- | ------ | ---- | --------- | ------------------------------------------- | ------------------------------------------ | ------------------------------------ | ---- | ---------- | ------------------ | ----------------------- |
|      |        |      |           |                                             |                                            |                                      |      |            |                    |                         |

##### Table: contractDistinction_CustomerDistinction_Exchange_Info

| id   | exchangeApplyDate | exchangeInputWriter | ASInfo_id | exchangeComment | exchangeMessage | exchangePackageDate | exchangeVariety | exchangeBackToFactoryNumber | exchangeBackToDate |
| ---- | ----------------- | ------------------- | --------- | --------------- | --------------- | ------------------- | --------------- | --------------------------- | ------------------ |
|      |                   |                     |           |                 |                 |                     |                 |                             |                    |

##### Table: contractDistinction_CustomerDistinction_Clip_Info

| id   | applyPerson | applyDate | clipPerson | clipReceiptDate | clipCompleteDate | clipStatus | comment | contractInfo_id | contractDistinction_Customer_Info_id | ASInformation_id |
| ---- | ----------- | --------- | ---------- | --------------- | ---------------- | ---------- | ------- | --------------- | ------------------------------------ | ---------------- |
|      |             |           |            |                 |                  |            |         |                 |                                      |                  |

##### Table: contractDistinction_CustomerDistinction_New_Info

| id   | boxPackageTurn | packageTurn | putIntoProductDATE | newOrderYear | newOrderDate | newPackageDate | newSendToFactoryDate | newSendToFactoryNum | newInputPerson | contractDistinction_Customer_Info_id | comment | newMessage |
| ---- | -------------- | ----------- | ------------------ | ------------ | ------------ | -------------- | -------------------- | ------------------- | -------------- | ------------------------------------ | ------- | ---------- |
|      |                |             |                    |              |              |                |                      |                     |                |                                      |         |            |

##### Table: contractDistinction_CustomerDistinction_Degree_Info

记录客户公司内的职员来申请AS的次数

| id   | degreeApplyDate | degreeApplyInputEmployee | ASInformation_id | degreeApplyComment |
| ---- | --------------- | ------------------------ | ---------------- | ------------------ |
|      |                 | FK                       |                  |                    |

##### Table: contractDistinction_CustomerDistinction_ItemDistinction_Clip_Info

| id   | contractDistinction_CustomerDistinction_Clip_Info_id | clipOriginalItem_ContractDistinction_ItemDistinction_Size_Info_ContractDistinction_ItemDistinction_Meta_Info_id | clipOriginalItem_ContractDistinction_ItemDistinction_Size_Info_size | clipCompleteItem_ContractDistinction_ItemDistinction_Size_Info_ContractDistinction_ItemDistinction_Meta_Info_id | clipCompleteItem_ContractDistinction_ItemDistinction_Size_Info_size | clipCompleteItemAmount | clipOriginalItemAmount | comment | createdDate | updatedDate |
| ---- | ---------------------------------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ---------------------- | ---------------------- | ------- | ----------- | ----------- |
|      |                                                      |                                                              |                                                              |                                                              |                                                              |                        |                        |         |             |             |

##### Table: factoryInfo

| factoryName | factoryTel | factoryAddress | factoryMobile | businessLicenseNum | representiveName | bank | bankAccount |
| ----------- | ---------- | -------------- | ------------- | ------------------ | ---------------- | ---- | ----------- |
|             |            |                |               |                    |                  |      |             |



#### 2.3  ContractDistinction_ItemDistinction

##### Table: ContractDistinction_ItemDistinction_Meta_Info

| id   | contractInfo_Id | itemName | image | deliveryUnitPrice | productPredictAmount | deliveryPredictDate | totalWarehouseAmount | totalWarehouseAmount | totalOrderAmount | totalClaimAmount | inventoryAmount | actualInventoryAmount | saleProceeds | sexDistinction |
| ---- | --------------- | -------- | ----- | ----------------- | -------------------- | ------------------- | -------------------- | -------------------- | ---------------- | ---------------- | --------------- | --------------------- | ------------ | -------------- |
|      |                 |          |       |                   |                      |                     |                      |                      |                  |                  | null            | null                  |              |                |

inventoryAmount：程序计算出来的应有的库存量

actualInventoryAmount:人为损坏，天气原因等影响衣物损耗之后剩下的数量

##### Table: ContractDistinction_ItemDistinction_Order_Info

| degree | orderDate | orderAmount | comment | contractDistinction_ItemDistinction_meta_info_id | id   |
| ------ | --------- | ----------- | ------- | ------------------------------------------------ | ---- |
|        |           |             |         |                                                  |      |

##### Table: ContractDistinction_ItemDistinction_Size_Info

| contractDistinction_ItemDistinction_Meta_Info | size | comment |
| --------------------------------------------- | ---- | ------- |
|                                               |      |         |

##### Table: ContractDistinction_ItemDistinction_SizeDistinction_Warehouse_Info

| id   | degree | warehouseDate | warehouseAmount | comment | contractDistinction_ItemDistinction_Size_Info_ContractDistinction_ItemDistinction_Meta_Info_id | contractDistinction_ItemDistinction_SizeDistinction_meta_Size |
| ---- | ------ | ------------- | --------------- | ------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
|      |        |               |                 |         |                                                              |                                                              |

##### Table: ContractDistinction_ItemDistinction_Claim_Info

| degree | claimDate | claimAmount | comment | contractDistinction_ItemDistinction_Meta_Info_id | claimOrNot | depositOrNot |
| ------ | --------- | ----------- | ------- | ------------------------------------------------ | ---------- | ------------ |
|        |           |             |         | fk                                               |            |              |

##### Table: ContractDistinction_ItemDistinction_Exchange_Info

| createdDate | updatedDate | contractDistinction_ItemDistinction_Size_Info_ContractDistinction_ItemDistinction_Meta_Info_id | contractDistinction_ItemDistinction_Size_Info_Size | contractDistinction_CustomerDistinction_Exchange_Info_id | amount | id   |
| ----------- | ----------- | ------------------------------------------------------------ | -------------------------------------------------- | -------------------------------------------------------- | ------ | ---- |
|             |             |                                                              |                                                    |                                                          |        |      |

##### Table: ContractDistinction_ItemDistinction_New_Info

| createdDate | updatedDate | contractDistinction_ItemDistinction_Size_Info_ContractDistinction_ItemDistinction_Meta_Info_id | contractDistinction_ItemDistinction_Size_Info_Size | contractDistinction_CustomerDistinction_Exchange_Info_id | amount | id   |
| ----------- | ----------- | ------------------------------------------------------------ | -------------------------------------------------- | -------------------------------------------------------- | ------ | ---- |
|             |             |                                                              |                                                    |                                                          |        |      |

##### Table: ContractDistinction_ItemDistinction_Count_Info

| createdDate | updatedDate | contractDistinction_ItemDistinction_Size_Info_ContractDistinction_ItemDistinction_Meta_Info_id | contractDistinction_ItemDistinction_Size_Info_Size | contractDistinction_CustomerDistinction_Exchange_Info_id | amount | id   |
| ----------- | ----------- | ------------------------------------------------------------ | -------------------------------------------------- | -------------------------------------------------------- | ------ | ---- |
|             |             |                                                              |                                                    |                                                          |        |      |



#### 

#### 2.4 A/S 

##### Table: ASInformation (A/S 정보)

| id   | contractDistinction_CustomerInformation_id | **conversationDate** | conversationContents | conversationEmployee | ASDegree | Comment |
| ---- | ------------------------------------------ | -------------------- | -------------------- | -------------------- | -------- | ------- |
|      |                                            |                      |                      |                      |          |         |

Table: CustomerQandA

| id   | customerWriterName | customerWriterDate | contract | customerWriterTel | questionContents | answerPerson | processCotents | processStatus | importance | answerDate |
| ---- | ------------------ | ------------------ | -------- | ----------------- | ---------------- | ------------ | -------------- | ------------- | ---------- | ---------- |
|      |                    |                    |          |                   |                  |              |                |               |            |            |

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

| id   | employeeName | createdTime | Token | os   | ip   | device | browser | valid | updatedTime | rememberMe | session |
| ---- | ------------ | ----------- | ----- | ---- | ---- | ------ | ------- | ----- | ----------- | ---------- | ------- |
|      |              |             |       |      |      |        |         |       |             |            |         |

权限管理 （ComponentId）

Table: Team_ComponentACL

| authority | companyTeamsList_TeamName | Component_id |
| --------- | ------------------------- | ------------ |
|           |                           |              |

User_ComponentACL

| Authority | Component_id | employeeName |
| --------- | ------------ | ------------ |
|           |              |              |



AuthenticatedUserIP

| IP   | employeeName |
| ---- | ------------ |
|      |              |



#### 3.2 公司行政业务相关表

Table: Notification

| id   | createdDateTime | updatedDateTime | Content | noticeStart | noticeEnd | createdBy | title | deleted |
| ---- | --------------- | --------------- | ------- | ----------- | --------- | --------- | ----- | ------- |
|      |                 |                 |         |             |           |           |       |         |

##### Table: otherSubsidyCost

| id   | productYear | accountingYear | purchaseDate | contract | item | sumOfMoney | sumOfMoney_VATIncludes | purchasing place | purchaser |
| ---- | ----------- | -------------- | ------------ | -------- | ---- | ---------- | ---------------------- | ---------------- | --------- |
|      |             |                |              |          |      |            |                        |                  |           |

##### Table: unit

| unit |
| ---- |
|      |

##### Table: designActualPurchasedCotents

| id   | productYear | accountingYear | purchaseDate | purchaser | contractInfo_id | contractDistinction_ItemDistinction_Meta_Info_id | jobClassification | item | unitPrice | warehousingAmount | warehousingSumOfMoney | warehousingSumOfMoney_VATIncluding | companyName | comment |
| ---- | ----------- | -------------- | ------------ | --------- | --------------- | ------------------------------------------------ | ----------------- | ---- | --------- | ----------------- | --------------------- | ---------------------------------- | ----------- | ------- |
|      |             |                |              |           |                 |                                                  |                   |      |           |                   |                       |                                    |             |         |

Table: sampleManagement(대장?)



#### 4.文件上传相关表

Table：file

| fileName | fileUploadType | fileSize | fileStorageType | uploadDate | uploadStatus | validDate | validStatus | warehousingDate | warehousingStatus | path | uploadUser |
| -------- | -------------- | -------- | --------------- | ---------- | ------------ | --------- | ----------- | --------------- | ----------------- | ---- | ---------- |
|          |                |          |                 |            |              |           |             |                 |                   |      |            |

