# Tideo Product Hub

> PRD + 产品简介 + 体验框架 + API 调试台，四合一产品知识聚合器

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![GitHub stars](https://img.shields.io/github/stars/ildar981105-create/tideo-product-hub)](https://github.com/ildar981105-create/tideo-product-hub/stargazers)
[![GitHub topics](https://img.shields.io/github/topics/codebuddy-skill)](https://github.com/topics/codebuddy-skill)

## 🎯 5 分钟上手

### API Console（最快）

```html
<script src="api-console-config.js"></script>
<script>
  window.API_CONSOLE_CONFIG = {
    productName: '我的产品',
    baseUrl:     'https://api.my-product.com',
    groups: [
      {
        name: '用户',
        apis: [
          { method: 'POST', path: '/users', desc: '创建用户',
            params: [
              { name:'name',  type:'text', required:true, placeholder:'姓名' },
              { name:'email', type:'text', required:true, placeholder:'邮箱' }
            ]
          }
        ]
      }
    ]
  };
</script>
<script src="api.html"></script>
```

### 其他页面

| 页面 | 定制方式 |
|------|---------|
| **PRD** | 复制 `prd.html`，替换章节内容 |
| **产品简介** | 复制 `product-brief.html`，替换内容 |
| **体验框架** | 复制 `experience-framework.html`，替换四维模型 |
| **Hub 导航** | 复制 `hub.html`，修改四个入口链接 |

## 核心模块

| 页面 | 功能 |
|------|------|
| **prd.html** | 功能规格说明书，含目录/Callout/流程图 |
| **product-brief.html** | 面向投资人的轻量简介，含 flow 图 + 状态表 |
| **experience-framework.html** | AI 产品体验验证方法论，四维模型 + SUS/SAM/EV/NPS 量表 |
| **api.html** | API 调试台，支持请求构造/响应查看/历史记录 |
| **hub.html** | 四页面导航入口，统一暗色主题 |

## 完整功能说明

详见 [SKILL.md](SKILL.md)

## License

MIT © Tideo
