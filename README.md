# 📱 istea 微信小程序项目结构总结

## 🎯 项目概述

- **项目类型**: 微信小程序
- **开发语言**: TypeScript
- **项目名称**: istea（茶饮小程序）
- **AppID**: wx7ac3b25e2b5694d1
- **项目描述**: 一个茶饮相关的微信小程序应用

## 🏗️ 项目结构

### 根目录配置文件

```
├── package.json              # 项目依赖管理
├── project.config.json       # 微信开发者工具配置
├── project.private.config.json # 私有配置文件
├── tsconfig.json            # TypeScript 配置
└── sitemap.json             # 小程序搜索优化配置
```

### 小程序主体 (miniprogram/)

```
miniprogram/
├── app.json                 # 小程序全局配置
├── app.ts                   # 小程序入口文件
├── app.wxss                 # 全局样式
├── sitemap.json             # 搜索配置
├── images/                  # 图片资源目录
│   ├── 首页.png             # 首页图标
│   ├── 首页-选中.png        # 首页选中状态图标
│   ├── 点单.png             # 点单图标
│   ├── 点单-选中.png        # 点单选中状态图标
│   ├── 订单.png             # 订单图标
│   ├── 订单-选中.png        # 订单选中状态图标
│   ├── 我的.png             # 我的图标
│   └── 我的-选中.png        # 我的选中状态图标
├── pages/                   # 页面目录
│   ├── index/               # 首页
│   ├── buy/                 # 点单页面
│   ├── order/               # 订单页面
│   ├── my/                  # 我的页面
│   ├── logs/                # 日志页面
│   ├── jump/                # 跳转页面
│   └── template/            # 模板页面
├── utils/                   # 工具函数目录
│   ├── util.ts              # 通用工具函数
│   ├── qqmap-wx-jssdk.min.js # 腾讯地图SDK
│   └── qqmap-wx-jssdk1.2/   # 腾讯地图SDK v1.2
└── typings/                 # TypeScript 类型定义
    ├── index.d.ts
    └── types/
        ├── index.d.ts
        └── wx/               # 微信API类型定义
            ├── index.d.ts
            ├── lib.wx.api.d.ts
            ├── lib.wx.app.d.ts
            ├── lib.wx.behavior.d.ts
            ├── lib.wx.cloud.d.ts
            ├── lib.wx.component.d.ts
            ├── lib.wx.event.d.ts
            └── lib.wx.page.d.ts
```

## 📄 页面结构

### 主要功能页面

| 页面名称 | 路径 | 功能描述 |
|---------|------|----------|
| **首页** | `pages/index/` | 应用入口页面，包含用户信息获取 |
| **点单** | `pages/buy/` | 商品购买页面 |
| **订单** | `pages/order/` | 订单管理页面 |
| **我的** | `pages/my/` | 个人中心页面 |

### 辅助页面

| 页面名称 | 路径 | 功能描述 |
|---------|------|----------|
| **日志** | `pages/logs/` | 调试日志页面 |
| **跳转** | `pages/jump/` | 页面跳转测试 |
| **模板** | `pages/template/` | 页面模板 |

## 🧭 底部导航栏 (TabBar)

配置了4个主要功能模块：

```json
{
  "tabBar": {
    "color": "#bfbfbf",
    "selectedColor": "#2c2c2c",
    "list": [
      {
        "pagePath": "pages/index/index",
        "text": "首页",
        "iconPath": "/images/首页.png",
        "selectedIconPath": "/images/首页-选中.png"
      },
      {
        "pagePath": "pages/buy/buy",
        "text": "点单",
        "iconPath": "/images/点单.png",
        "selectedIconPath": "/images/点单-选中.png"
      },
      {
        "pagePath": "pages/order/order",
        "text": "订单",
        "iconPath": "/images/订单.png",
        "selectedIconPath": "/images/订单-选中.png"
      },
      {
        "pagePath": "pages/my/my",
        "text": "我的",
        "iconPath": "/images/我的.png",
        "selectedIconPath": "/images/我的-选中.png"
      }
    ]
  }
}
```

## 🛠️ 技术特点

### 开发环境
- **TypeScript**: 完整的类型支持
- **微信小程序**: 标准小程序开发模式
- **开发者工具**: 支持 TypeScript 编译

### 功能特性
- ✅ **多页面应用**: 采用微信小程序标准页面结构
- ✅ **底部导航**: 4个主要功能模块的快速切换
- ✅ **用户系统**: 包含用户信息获取和登录功能
- ✅ **页面跳转**: 支持页面间的导航和跳转
- ✅ **地图集成**: 集成腾讯地图SDK
- ✅ **类型安全**: 完整的TypeScript类型定义

## 📝 开发状态

**当前状态**: 基础框架项目

- 🔄 **首页**: 基础用户信息获取功能
- 🔄 **点单页面**: 待完善商品展示和购买逻辑
- 🔄 **订单页面**: 待完善订单管理功能
- 🔄 **我的页面**: 待完善个人中心功能

## 🚀 项目优势

1. **标准化结构**: 遵循微信小程序最佳实践
2. **类型安全**: TypeScript提供完整的类型检查
3. **模块化设计**: 清晰的页面和功能分离
4. **扩展性强**: 为后续功能开发提供良好基础
5. **开发体验**: 完整的开发工具链支持
