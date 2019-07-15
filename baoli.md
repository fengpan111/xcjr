## 开票信息
#### 1.查询开票信息
###### Request URL: /invoiceInfo
###### Request Method : GET
###### parameters : 
        

name | type |is null | explain
---|--- | ---|---
onlyFirst | boolean| yes | 1:只查第1条地址
type|String | yes | 0:增值税普通发票,1:增值税专用发票,不传为全部

###### Rseponse


#### 2.新增开票信息
###### Request URL: /invoiceInfo
###### Request Method : POST
###### parameters : 
        

name | type |is null | explain
---|--- | ---|---
type|String | no | 0:增值税普通发票,1:增值税专用发票
taxpayerIdentityNumber |String | no | 纳税人识别号
registerAddr | String | no | 注册地址
registerTel | String | no | 注册电话
openingBank | String | no | 开户行
openingBankBranch | String | no | 开户支行
openingBankAccount | String | no | 开户行账号
companyName | String | no | 单位名称
orderBy | String | yes | 0:设为默认开票信息

#### 3.修改开票信息
###### Request URL: /invoiceInfo
###### Request Method : PUT
###### parameters : 
        

name | type |is null | explain
---|--- | ---|---
refcode| number | no | 开票信息编号 
type|String | no | 0:增值税普通发票,1:增值税专用发票
taxpayerIdentityNumber |String | no |纳税人识别号
registerAddr | String | no | 注册地址
registerTel | String | no | 注册电话
openingBank | String | no | 开户行
openingBankBranch | String | no | 开户支行
openingBankAccount | String | no | 开户行账号
companyName | String | no | 单位名称
orderBy | String | yes |0:设为默认开票信息


#### 4.删除开票信息
###### Request URL: /invoiceInfo
###### Request Method : DELETE
###### parameters : 
        

name | type |is null | explain
---|--- | ---|---
refcode| number | no | 开票信息编号


---


## 收款信息
#### 1.查询收款信息
###### Request URL: /receiptInfo
###### Request Method : GET
###### parameters : 
        

name | type |is null | explain
---|--- | ---|---
onlyFirst | boolean| yes | 1:只查第1条信息
contacts | String | yes | 联系人模糊查询

###### Rseponse


#### 2.新增收款信息
###### Request URL: /receiptInfo
###### Request Method : POST
###### parameters : 
        

name | type |is null | explain
---|--- | ---|---
contacts|String | no | 联系人
tel |String | no | 联系电话
serviceAddr | String | no | 制定送达地址
accountName | String | no | 账户名称
provinceOfAccount | String | no | 账户所在省
cityOfAccount | String | no | 账户所在市
accountNumber | String | no | 账号
openingBank | String | no | 开户行
openingBankBranch | String | no | 开户支行
cnapsNumber | String | no | 联行号
fax | String | no | 传真号
orderBy | String | yes | 0:设为默认开票信息

#### 3.修改收款票信息
###### Request URL: /receiptInfo
###### Request Method : PUT
###### parameters : 
        

name | type |is null | explain
---|--- | ---|---
refcode| number | no | 开票信息编号 
contacts|String | no | 联系人
tel |String | no | 联系电话
serviceAddr | String | no | 制定送达地址
accountName | String | no | 账户名称
provinceOfAccount | String | no | 账户所在省
cityOfAccount | String | no | 账户所在市
accountNumber | String | no | 账号
openingBank | String | no | 开户行
openingBankBranch | String | no | 开户支行
cnapsNumber | String | no | 联行号
fax | String | no | 传真号
orderBy | String | yes | 0:设为默认开票信息


#### 4.删除收款信息
###### Request URL: /receiptInfo
###### Request Method : DELETE
###### parameters : 
        

name | type |is null | explain
---|--- | ---|---
refcode| number | no | 收款信息编号



---
 ## 获取区域信息
###### Request URL: /receiptInfo/administrativeDivision
###### Request Method : GET
###### parameters : 
name | type |is null | explain
---|--- | ---|---
areaLevel| String | no | 1:省,2: 市
provinceName | String|yes|  省名称

---
### 更新资金计划信息
###### Request URL :services/member/updateUdmBudgetPlan
###### Request Method : POST
###### parameters :
###### 原有参数不再赘述,下表只展示本次改动
name | type |is null | explain
---|--- | ---|---
openingBankBranch| String | yes | 开户支行
provinceOfAccount | String|yes|  账户所在省
cityOfAccount | String|yes|  账户所在城市
invoiceType | String|yes|  开票类型: 0:增值税普通发票,1:增值税专用发票
invoiceTxIdentityNumber | String|yes|  开票纳税人识别号
invoiceRegisterAddr | String|yes|  开票注册地址
invoiceRegisterTel | String|yes|  开票注册电话
invoiceOpeningBank | String|yes|  开票开户行
invoiceOpeningBankAccount | String|yes|  开票开户行账号
invoiceOpeningBankBranch | String|yes|  开票开户支行
invoiceCompanyName | String|yes|  开票单位名称

