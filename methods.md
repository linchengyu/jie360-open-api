# 1.接口说明（闪电周转提供）
生成订单时，“借360”向闪电周转推送订单，包括订单基本信息，产品政策对应信息、抓取信息等，接口采用post方式，数据组织采用json传递。
# 2.参数说明：
orderInfo 订单的基本信息， applyDetail 产品政策对应信息， addInfo 抓取信息如运营商、网银、信用卡账单等。

| 参数 | 名称 | 值类型 | 是否必须 | 备注 |
| :----: | :----: | :----: | :----: | :---- |
| orderInfo | 订单基本信息 | OrderInfo | 是 | OrderInfo字段说明 |
| applyDetail | 产品政策对应信息 | ApplyDetail | 是 | ApplyDetail字段说明 |
| addInfo | 订单抓取信息 | AddInfo | 是 | AddInfo字段说明 |

### OrderInfo字段说明：
| 参数 | 名称 | 值类型 | 是否必须 | 备注 |
| :----: | :----: | :----: | :----: | :---- |
| orderNo | 订单编号 | String | 是 |  |
| userName | 用户名 | String | 是 |  |
| userMobile | 用户手机号码 | String | 是 |  |
| applicationAmount | 申请金额 | Float | 是 |  |
| applicationTerm | 申请期限（日） | Int | 是 |  |
| orderTime | 订单创建时间 | Timestamp | 是 |  |

### ApplyDetail字段说明：
| 参数 | 名称 | 值类型 | 是否必须 | 备注 |
| :----: | :----: | :----: | :----: | :---- |
| applicationAmount | 申请金额	 | Float | 是 |  |
| applicationTerm | 申请期限（日） | Int | 是 |  |
| career | 职业 | Int | 是 | 1 - 程序员/设计师/产品经理<br>2 - 学生<br>3 - 教师<br>4 - 服务员<br>5 - 司机<br>6 - 厨师<br>7 - 理发师<br>8 - 教练<br>9 - 文员<br>10 - 销售经理<br>11 - 客服专员<br>12 - 采购员<br>13 - 营业员<br>14 - 网店店长<br>15 - 维修工<br>16 - 快递员<br>17 - 律师<br>18 - 翻译<br>19 - 编辑<br>20 - 会计<br>21 - 医生<br>22 - 工程师<br>23 - 其他 |
| workPeriod | 在职时长 | Int | 是 | 1 - 6个月以下<br>2 - 6-12个月<br>4 - 1-3年<br>5 - 3年以上 |
| userEducation | 教育程度 | Int | 是 | 1 - 小学<br>2 - 初中<br>3 - 高中/职高/技校<br>4 - 大专<br>5 - 本科<br>6 - 硕士<br>7 - 博士 |
| incomeRange | 月收入 | Int | 是 | 1 - 小于1000元<br>2 - 1000~2000元<br>3 - 2000~4000元<br>4 - 4000~6000元<br>5 - 6000~10000元<br>6 - 10000元以上 |
| idNumber | 本人身份证号码 | String | 是 |  |
| realName | 本人身份证号码 | String | 是 |  |
| gpsLocation | GPS信息 | String | 是 | 经纬度以“,”分隔 |

### AddInfo字段说明：

#### addInfo.zhima：
| 参数 | 名称 | 值类型 | 是否必须 | 备注 |
| :----: | :----: | :----: | :----: | :---- |
| aliTrustScore | 芝麻信用分 | String | 是 |  |

#### addInfo.contacts：
| 参数 | 名称 | 值类型 | 是否必须 | 备注 |
| :----: | :----: | :----: | :----: | :---- |
| phoneList | 手机通讯录信息 | PhoneList | 是 | PhoneList字段说明 |
| callLog | 手机通话记录信息 | String | 是 | CallLog字段说明 |

##### PhoneList字段说明：
| 参数 | 名称 | 值类型 | 是否必须 | 备注 |
| :----: | :----: | :----: | :----: | :---- |
| name | 通讯录姓名 | String | 是 |  |
| phone | 通讯录手机号 | String | 是 |  |

##### CallLog字段说明：
| 参数 | 名称 | 值类型 | 是否必须 | 备注 |
| :----: | :----: | :----: | :----: | :---- |
| phone | 通话记录手机号 | String | 是 |  |
| date | 通话时间戳 | Int | 是 |  |
| duration | 通话时长秒数 | Int | 是 |  |
| type | 通话类型 | Int | 是 |  |

#### addInfo.carrier：(运营商爬取数据)
