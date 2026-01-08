# Lightning Site

产品官方网站

## 版本检查接口

应用可以通过以下接口获取最新版本信息：

```
GET https://martiny985.github.io/version.json
```

### 响应示例

```json
{
  "version": "0.1.3",
  "releaseDate": "2026-01-08",
  "downloadUrl": "",
  "releaseNotes": "",
  "minVersion": "0.1.0"
}
```

### 字段说明

| 字段 | 说明 |
|------|------|
| version | 最新版本号 |
| releaseDate | 发布日期 |
| downloadUrl | 下载地址 |
| releaseNotes | 更新说明 |
| minVersion | 最低兼容版本 |
