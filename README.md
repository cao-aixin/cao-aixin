# cao-aixin

软件工程在读，求职方向：**AI 产品经理 / AI 测试**。

关注 AI 能力在真实业务里的完整链路：场景选择 → 提示词与 Tool 设计 → 权限与降级 → 效果验证。

## 项目一览

### [智团星台 · 校园社团智能协同系统](https://github.com/cao-aixin/zhituan-xingtai)

毕业设计。Spring Boot 3 + Vue3 + Sa-Token + Spring AI。

- 8 个 AI 技能场景：活动方案/总结、运营分析、个性化推荐、风险巡检、通知润色、联合方案、活动问答
- Tool Call 前置权限校验：越权请求不进模型，直接 403，避免「模型替权限做主」
- api-key 为空或调用失败时自动降级本地模板，业务不中断，返回带 source 标注

### [CoBot-v2 · 企业微信协作机器人](https://github.com/cao-aixin/CoBot-v2)

Spring AI 双模式 Agent：LLM Tool Calling 与本地 Skill（无 Key 可跑）。

- 团队洞察/周报：数字全部来自库内真实统计，AI 只负责叙述——AI 输出可核验
- 会议纪要拆任务、AI 生成 PPT（Apache POI 渲染真实 .pptx 文件）

### [新农e家 · 农产品尾货转化助农平台](https://github.com/cao-aixin/xinnong-ejia)

大学生创新创业项目。Vue3 + Express + MySQL。

- 农户入驻、商品上架、购物下单的完整业务闭环
- JWT 认证 + BCrypt 密码哈希

## 测试实践

- 每个项目附带可重复执行的闭环测试脚本（curl / Python），测试证据落文件可回溯
- AI 功能测试覆盖三条路径：真实大模型调用、降级路径、越权 403 与参数校验
