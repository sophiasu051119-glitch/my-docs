# API 参考

下面的接口只用于练习 API 文档的结构和代码块展示，不提供真实后端服务。

## 查询文档列表

- 请求方法：`GET`
- 请求路径：`/api/docs`
- 功能：返回当前可查看的文档条目列表。
- 认证：无（示例接口）

### 请求示例

```bash
curl https://example.com/api/docs
```

### 成功响应

状态码：`200 OK`

```json
{
  "items": [
    {"id": 1, "title": "关于本项目", "path": "/about/"},
    {"id": 2, "title": "使用指南", "path": "/guide/"}
  ],
  "count": 2
}
```

### 字段说明

| 字段 | 类型 | 说明 |
| --- | --- | --- |
| `items` | array | 文档条目数组 |
| `id` | integer | 条目编号 |
| `title` | string | 页面标题 |
| `path` | string | 页面相对路径 |
| `count` | integer | 返回的条目数量 |

如果以后真的实现该接口，还需要补充错误响应、分页参数和认证方式；本次只验证文档页面的表达和渲染效果。

[返回首页](index.md) · [查看项目说明](about.md)

