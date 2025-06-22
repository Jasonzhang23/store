# MenFashion Store - 男士服装电商网站

一个完整的男士服装电商网站项目，用于学习前后端开发概念。

## 项目概述

这是一个前后端分离的电商网站项目，包含完整的用户系统、商品管理、购物车、订单处理等功能。

### 技术栈

- **前端**: HTML5, CSS3, JavaScript (原生)
- **后端**: Node.js, Express.js
- **数据库**: SQLite
- **认证**: JWT (JSON Web Token)
- **样式**: 苹果风格设计

## 功能特性

### 用户功能
- ✅ 用户注册/登录
- ✅ 密码重置
- ✅ 个人信息管理
- ✅ 收藏夹
- ✅ 浏览历史

### 商品功能
- ✅ 商品分类展示
- ✅ 商品搜索筛选
- ✅ 商品详情页
- ✅ 热门商品/新品推荐

### 购物功能
- ✅ 购物车管理
- ✅ 订单创建
- ✅ 模拟支付
- ✅ 订单跟踪
- ✅ 商品评价

### 管理功能
- ✅ 商品管理
- ✅ 订单管理
- ✅ 用户管理
- ✅ 数据统计

## 项目结构

```
menfashion-store/
├── frontend/                 # 前端文件
│   ├── pages/               # 页面文件
│   ├── css/                 # 样式文件
│   ├── js/                  # JavaScript文件
│   └── images/              # 图片资源
├── backend/                  # 后端文件
│   ├── routes/              # 路由文件
│   ├── middleware/          # 中间件
│   ├── config/              # 配置文件
│   └── utils/               # 工具函数
├── database/                 # 数据库文件
└── package.json             # 项目配置
```

## 安装和运行

### 1. 安装依赖

```bash
npm install
```

### 2. 初始化数据库

```bash
npm run init-db
```

### 3. 启动服务器

```bash
# 开发模式（自动重启）
npm run dev

# 生产模式
npm start
```

### 4. 访问网站

- 前端页面: http://localhost:3000
- API接口: http://localhost:3000/api
- 后台管理: http://localhost:3000/admin/login.html

## 默认账号

### 管理员账号
- 邮箱: admin@menfashion.com
- 密码: admin123

### 测试用户账号
- 邮箱: test@example.com
- 密码: 123456

## API接口文档

### 用户相关
- `POST /api/users/register` - 用户注册
- `POST /api/users/login` - 用户登录
- `GET /api/users/profile` - 获取用户信息
- `PUT /api/users/profile` - 更新用户信息

### 商品相关
- `GET /api/products` - 获取商品列表
- `GET /api/products/:id` - 获取商品详情
- `GET /api/products/categories` - 获取商品分类

### 购物车相关
- `GET /api/orders/cart` - 获取购物车
- `POST /api/orders/cart` - 添加到购物车
- `PUT /api/orders/cart/:id` - 更新购物车商品
- `DELETE /api/orders/cart/:id` - 删除购物车商品

### 订单相关
- `POST /api/orders` - 创建订单
- `GET /api/orders` - 获取订单列表
- `GET /api/orders/:id` - 获取订单详情

## 前后端概念说明

### 前端 (Frontend)
前端负责用户界面的展示和用户交互，包括：
- 页面布局和样式
- 用户交互处理
- 数据展示
- 表单验证

### 后端 (Backend)
后端负责业务逻辑处理和数据管理，包括：
- API接口提供
- 数据库操作
- 用户认证
- 业务逻辑处理

### 数据流向
1. 用户在前端进行操作
2. 前端通过API向后端发送请求
3. 后端处理请求并操作数据库
4. 后端返回处理结果给前端
5. 前端更新页面显示

## 学习要点

### 1. 前后端分离
- 前端和后端独立开发
- 通过API进行数据交互
- 前端专注于用户体验
- 后端专注于业务逻辑

### 2. RESTful API
- 使用标准HTTP方法
- 统一的接口设计
- 清晰的数据格式

### 3. 用户认证
- JWT token认证
- 安全的密码存储
- 权限控制

### 4. 数据库设计
- 表结构设计
- 关联关系
- 数据完整性

## 开发建议

1. **先理解整体架构**：了解前后端的分工和交互方式
2. **从简单功能开始**：先实现基础的CRUD操作
3. **逐步添加功能**：在基础功能上添加更复杂的功能
4. **注意安全性**：实现用户认证和权限控制
5. **优化用户体验**：添加加载状态、错误处理等

## 常见问题

### Q: 如何添加新的商品分类？
A: 在数据库的categories表中添加新记录，或通过后台管理系统添加。

### Q: 如何修改支付方式？
A: 在`backend/utils/payment.js`中修改支付逻辑。

### Q: 如何添加新的页面？
A: 在`frontend/pages/`目录下创建新的HTML文件，并在导航中添加链接。

## 贡献

欢迎提交Issue和Pull Request来改进这个项目！

## 许可证

MIT License 
