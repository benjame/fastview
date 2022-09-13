# 接口文档

## 1. 接口通用包装

```json
{
  "code": "200",
  "msg": "成功",
  "data": null
}
```

如果是分页数据，数据包装在 `data`中，需要展开：

```json
{
  "code": "200",
  "msg": "成功",
  "data": {
    "total": 1,
    "list": [
      {
        "id": 1,
        "createTime": null,
        "updateTime": null,
        "createBy": null,
        "updateBy": null,
        "status": null,
        "remark": null,
        "blackListId": 2,
        "blackList": null,
        "version": "1.0-SNAPSHOT",
        "locked":false
      }
    ],
    "pageNum": 0,
    "pageSize": 0,
    "size": 1,
    "startRow": 1，
    "endRow": 1,
    "pages": 0,
    "prePage": 0,
    "nextPage": 0,
    "isFirstPage": false,
    "isLastPage": true,
    "hasPreviousPage": false,
    "hasNextPage": false,
    "navigatePages": 8,
    "navigatePageNums": [],
    "navigateFirstPage": 0,
    "navigateLastPage": 0,
    "lastPage": 0,
    "firstPage": 0
  }
}
```

| 字段  |  类型  |      描述      |
| :---: | :----: | :------------: |
| total | number | 所有记录的数量 |
| list  | object | 分页列表的数据 |

## 2.接口列表

### 2.1 黑名单

### 2.2 准入系统

### 2.3 定时任务

### 2.4 字典

#### 2.4.1 字典(查询、修改、新增、删除)

##### 2.4.1.1 通用查询(queryParams:字典名称、字典编码)

**根据字典名称、字典编码查询(联合查询、单查询、空查询)**

URL: http://localhost:8080/dict

method: get

requestParams:

| 字段 |  类型  |   描述   |
| :--: | :----: | :------: |
| name | string | 字典名称 |
| code | string | 字典编码 |

responseBody:

|    字段    |  类型  |   说明   |
| :--------: | :----: | :------: |
|     id     | number |          |
|  createBy  | string |          |
|  updateBy  | string |          |
| createTime |  date  |          |
| updateTime |  date  |          |
|   remark   | string |          |
|    name    | string | 字典名称 |
|    code    | string | 字典编码 |

**根据 id 查询**

URL: http://localhost:8080/dict/info

method: get

requestParam:

| 字段 |  类型  | 说明 |
| :--: | :----: | :--: |
|  id  | number | 主键 |

responseBody: data

|    字段    |  类型  | 说明 |
| :--------: | :----: | :--: |
|     id     | number |      |
|  createBy  | string |      |
|  updateBy  | string |      |
| createTime |  date  |      |
| updateTime |  date  |      |
|   remark   | string |      |
|    name    | string |      |
|    code    | string |      |



##### 2.4.1.2 新增、修改、删除

**新增**

URL: http://localhost:8080/dict

method: POST

requestBody:

| 字段 |  类型  | 说明 |
| :--: | :----: | :--: |
| name | string |      |
| code | string |      |



**修改**

URL: http://localhost:8080/dict

method: PUT

**删除**

URL: http://localhost:8080/dict

method: DELETE





#### 2.4.2 字典详情(查询、修改、新增、删除)



### 2.5 发送队列



### 2.6 货币管理

