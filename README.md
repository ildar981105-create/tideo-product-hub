# tideo-product-hub

产品知识库聚合器：PRD + 产品简介 + 体验框架 + API 调试台，可配置化适用于任何产品团队。

## 文件结构

```
assets/
├── hub.html                  # Hub 导航页（入口）
├── prd.html                  # PRD 页面（模板，替换内容即用）
├── product-brief.html        # 产品简介（模板，替换内容即用）
├── experience-framework.html # 体验框架方法论（通用，内容不敏感）
├── api.html                  # API 调试台（配置化）
└── api-console-config.js     # API Console 端点配置

references/
└── (预留扩展目录)
```

## 快速使用

### Hub 导航页

直接打开 `hub.html`，四个入口卡片分别链接到四个子页面。

### PRD / 产品简介

复制 `prd.html` 或 `product-brief.html`，替换其中的产品特定内容为你的内容。

### API 调试台

```html
<script src="api-console-config.js"></script>
<script>
  window.API_CONSOLE_CONFIG.baseUrl = 'https://api.yourproduct.com';
  window.API_CONSOLE_CONFIG.groups = [
    {
      name: '用户模块',
      apis: [
        {
          method: 'POST',
          path: '/users',
          desc: '创建用户',
          params: [
            { name:'name', type:'text', required:true, placeholder:'姓名' },
            { name:'email', type:'text', required:true, placeholder:'邮箱' }
          ]
        }
      ]
    }
  ];
</script>
<script src="api.html"></script>
```

### 体验框架

`experience-framework.html` 包含完整的四维体验验证方法论（Trust / Control / Find / Resonance）及 SUS / SAM / EV / NPS 量表，可直接作为产品体验评估的内部工具使用。

## API Console 配置字段

| 字段 | 类型 | 说明 |
|------|------|------|
| `baseUrl` | string | API 基础地址 |
| `groups` | array | 分组列表 |
| `groups[].name` | string | 分组名称 |
| `groups[].apis` | array | 端点列表 |
| `groups[].apis[].method` | string | HTTP 方法 |
| `groups[].apis[].path` | string | 路径 |
| `groups[].apis[].desc` | string | 描述 |
| `groups[].apis[].params` | array | 参数列表 |
| `groups[].apis[].params[].name` | string | 参数名 |
| `groups[].apis[].params[].type` | string | `text` / `select` / `path` |
| `groups[].apis[].params[].options` | array | select 类型的选项（仅 select） |
| `groups[].apis[].params[].required` | boolean | 是否必填 |
| `groups[].apis[].params[].placeholder` | string | 占位文字 |
| `theme` | string | `blue` / `purple` / `green` / `orange` |
| `stats` | object | 初始统计值 |
