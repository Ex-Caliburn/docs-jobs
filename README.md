# 接口文档

获取用get，操作修改数据用post

#### 1.兼职列表

>

**请求地址：**

**前端请求地址：**../enterprise/info

**请求方式：**GET

**参数：**

| 参数 | 必选 | 类型 | 参数说明 |
| ---- | ---- | ---- | -------- |
| offset         | 否   | int    | 分页偏移     |
| limit          | 否   | int    | 分页大小     |

**返回：**

```json
{
  "data": {
    "name": '', // 名字
    "phone": '', // 手机
    "info": '', // 企业信息
    "hasAuth": '', // 是否认证
  },
  "err_code": 0,
  "err_msg": "success"
}
```

#### 2.修改手机号

>

**请求地址：**

**前端请求地址：**../enterprise/updatePhone

**请求方式：**post

**参数：**

| 参数 | 必选 | 类型 | 参数说明 |
| ---- | ---- | ---- | -------- |
| phone         | 否   | int    | 新手机号     |

**返回：**

```json
{
  "data": "",
  "err_code": 0,
  "err_msg": "success"
}

#### 3.更改密码

>

**请求地址：**

**前端请求地址：**../enterprise/updatePassword

**请求方式：**post

**参数：**

| 参数 | 必选 | 类型 | 参数说明 |
| ---- | ---- | ---- | -------- |
| password         | 否   | str    | 新密码     |

**返回：**

```json
{
  "data": "",
  "err_code": 0,
  "err_msg": "success"
}

#### 4.账号和设置

>

**请求地址：**

**前端请求地址：**../enterprise/accountAndSetting

**请求方式：**get

**参数：**

| 参数 | 必选 | 类型 | 参数说明 |
| ---- | ---- | ---- | -------- |

**返回：**

```json
{
  "data": {
    autoPassAudit: 1, // 1 是， 0 否
    ...
  },
  "err_code": 0,
  "err_msg": "success"
}

#### 5.账号和设置统一开关

> 方便拓展

**请求地址：**

**前端请求地址：**../enterprise/switch

**请求方式：**post

**参数：**

| 参数 | 必选 | 类型 | 参数说明 |
| ---- | ---- | ---- | -------- |
| type         | 是   | int    |  开关类型 1 自动通过审核    |
| status       | 是   | int    |  开关状态 1 开 0关    |

**返回：**

```json
{
  "data": "",
  "err_code": 0,
  "err_msg": "success"
}

#### 6.待发布兼职

> 方便拓展

**请求地址：**

**前端请求地址：**../enterprise/jobs/preRelease

**请求方式：**get

**参数：**

| 参数 | 必选 | 类型 | 参数说明 |
| ---- | ---- | ---- | -------- |
| key   | 否  | str    |  带发布搜索内容    |

**返回：**

```json
{
  "data": {
    list: [{
      name: '',
      address: '',
      salary: '',
      status: '',
    }],
    count: 1,
  },
  "err_code": 0,
  "err_msg": "success"
}

#### 7.获取兼职类型

>

**请求地址：**

**前端请求地址：**../enterprise/jobs/allType

**请求方式：**get

**参数：**

| 参数 | 必选 | 类型 | 参数说明 |
| ---- | ---- | ---- | -------- |

**返回：**

```json
{
  "data": [{
      name: '小时工',
      id: 1,
    },{
      name: '长期兼职',
      id: 2,
    },{
      name: '按天计酬',
      id: 3,
    }],
  "err_code": 0,
  "err_msg": "success"
}
