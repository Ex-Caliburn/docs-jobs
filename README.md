# 接口文档
#### 1.可添加的课程列表 （可调试）
> 可添加的课程列表

**请求地址：**

**前端请求地址：**../IntegralMall/GetIntegralCourseList

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
    "count": 3,
    "list": [
      {
        "course_id": 59311,
        "title": "支付",
        "course_type": 0, //0日历打卡 1作业 2解锁课程
        "permit_type": 4, //打卡限制人员类型：0-不限制 1-密码 2-指定群组(已弃用) 3 微信群 4 支付 5契约金
        "holded_by_user_id": 8266,
        "holded_name": "robot5.2"
      },
      {
        "course_id": 59310,
        "title": "(复制)(复制)125454",
        "course_type": 1,
        "permit_type": 0,
        "holded_by_user_id": 8266,
        "holded_name": "robot5.2"
      },
      {
        "course_id": 59309,
        "title": "(复制)125454",
        "course_type": 1,
        "permit_type": 0,
        "holded_by_user_id": 8266,
        "holded_name": "robot5.2"
      }
    ]
  },
  "err_code": 0,
  "err_msg": "success"
}
