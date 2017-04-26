# 1.接口说明（闪电周转提供）
生成订单时，“借360”向闪电周转推送订单，包括订单基本信息，产品政策对应信息、抓取信息等，接口采用post方式，数据组织采用json传递。
# 2.参数说明：
orderInfo 订单的基本信息， applyDetail 产品政策对应信息， addInfo 抓取信息如运营商、网银、信用卡账单等。
### orderInfo字段说明：
| 参数 | 名称 | 值类型 | 是否必须 |
| :----: | :----: | :---- | :----: |
| orderNo | 订单编号 | String | 是 |
| userName | 用户名 | String | 是 |
| userMobile | 用户手机号码 | String | 是 |
| applicationAmount | 申请金额 | Float | 是 |
| applicationTerm | 申请期限（日） | Int | 是 |
| orderTime | 订单创建时间 | Timestamp | 是 |

### applyDetail字段说明：










# Defining Methods

Methods allow you to smoothly display code examples in different languages.

{% method %}
## My first method

My first method exposes how to print a message in JavaScript and Go.

{% sample lang="js" %}
Here is how to print a message to `stdout` using JavaScript.

```js
console.log('My first method');
```

{% sample lang="go" %}
Here is how to print a message to `stdout` using Go.

```go
fmt.Println("My first method")
```

{% common %}
Whatever language you are using, the result will be the same.

```bash
$ My first method
```
{% endmethod %}
