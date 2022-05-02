
## API地址

v1: `https://api.tail.icu/api/v1/ill`

## 获取全部名单列表

`GET` `/getAll`

### 请求体

无

### 响应体

[根对象](../respData/#_2)

data 对象

| 字段 | 类型   | 内容     | 备注          |
| ---- | ------ | -------- | ------------- |
| list | array  | 名单列表 | 内容为 number |
| time | number | 时间戳   | 10位UNIX时间  |

## 查询指定QQ

`GET` `/checkQQ`

### 请求体

| 字段 | 必选 | 内容     | 备注 |
| ---- | ---- | -------- | ---- |
| qq   | 是   | 欲查询QQ |      |

### 响应体

[根对象](../respData/#_2)

| 状态码 | 原因             |
| ------ | ---------------- |
| 200    | 在黑名单内       |
| 400    | QQ号输入错误     |
| 404    | 黑名单内未查询到 |

data 对象 （在黑名单内时返回）

| 字段   | 类型   | 内容       | 备注         |
| ------ | ------ | ---------- | ------------ |
| target | object | 被查询对象 |              |
| time   | number | 时间戳     | 10位UNIX时间 |

data -> target 对象

| 字段     | 类型   | 内容     | 备注 |
| -------- | ------ | -------- | ---- |
| id       | number | 记录id   |      |
| qq       | string | 记录qq   |      |
| level    | number | 记录等级 |      |
| comment  | string | 记录原因 |      |
| active   | number | 是否生效 |      |
| operator | string | 操作员id |      |

