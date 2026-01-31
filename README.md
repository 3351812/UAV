# SR·U-FLEET 无人集群仿真验证平台（前端）

面向“地下水环境监测”场景的无人集群仿真验证前端原型。项目聚焦任务生成、通信网络、节点行为、三维态势与安全审计等模块，用于方案展示与交互联动演示。

## 主要功能
- 指挥控制中心：KPI 指标、视频回传墙、任务态势联动地图、系统日志
- 任务生成：任务建议、规则集、算法库、多阶段审批流与动态分配
- 通信网络：分层时延、链路质量与自组网健壮性展示
- 节点行为：协同决策与队形库管理
- 三维态势：Three.js 目标生成、轨迹与指标联动
- 标准与能力：统一数据标准、目标识别与实飞测试配置
- 安全与日志：用户权限、审计留痕与系统日志管理

## 技术栈
- Vue 3 + Vite
- Vue Router 4
- Pinia
- Three.js

## 快速开始
> 建议使用较新的 Node.js 版本（与 Vite 5 兼容）

```bash
npm install
npm run dev
```

构建与预览：

```bash
npm run build
npm run preview
```

默认开发端口为 `5173`（Vite 默认）。

## 内置账号（演示用）
- 管理员：admin / admin123
- 运维：ops / ops123
- 审计：audit / audit123

## 路由结构（主要页面）
- `/auth/login` 登录
- `/app/command` 指挥控制中心
- `/app/mission/task` 任务建议与动态分配
- `/app/mission/planner` 智能航迹规划
- `/app/mission/loop` 决策闭环实验
- `/app/network/monitor` 网络状态监测
- `/app/network/resilience` 自组网健壮性
- `/app/nodes/behavior` 节点协同决策
- `/app/nodes/formations` 队形库
- `/app/viz/3d` 三维态势
- `/app/standards/unified` 统一数据标准
- `/app/flighttest/scenario` 实飞测试配置
- `/app/recognition/targets` 目标识别
- `/app/security/users` 用户权限
- `/app/security/audit` 审计留痕
- `/app/logs/system` 系统日志

## 项目结构
```
public/              静态资源
src/
  assets/            图片与静态素材
  components/        可复用组件
  layouts/           页面布局（主框架/空白页）
  mock/              演示用假数据
  pages/             业务页面
  router/            路由配置与守卫
  store/             Pinia 状态（认证、日志、仿真）
  styles/            主题与全局样式
  utils/             工具函数
```

## 数据与状态说明
- 项目为纯前端演示，无后端依赖。
- 认证、日志、仿真态势等数据来自 `src/mock/` 与 `src/store/`。
- 日志默认写入浏览器 `localStorage`（键名：`sys_logs_v1`，最多保存 2000 条）。

## 设计与样式
- 主题与视觉系统集中在 `src/styles/`，包括全局样式、科幻风格与动画。
- 主布局在 `src/layouts/MainLayout.vue`，侧边栏包含各模块导航。

## 注意事项
- 这是展示型原型，功能交互基于本地 mock 数据。
- 若出现中文乱码，请确认编辑器编码为 UTF-8。

---
如果需要补充真实接口、权限策略或数据协议，请告知具体需求。
