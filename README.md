# P-Momentum

> **p = mv** — 动量是质量与速度的乘积；微小的积累，终将带来巨大的改变。

## 理念

P-Momentum 是一个以**嵌入式开发**为核心的工具集合。如同物理学中的动量——每一个工具都是一份微小的质量（*m*），每一次迭代都赋予它速度（*v*），当积累足够多时，即便是最轻量的工具，也能以极小的代价撬动巨大的效能。

我们相信：

- **积少成多** — 单个工具或许简单，但集合的力量是指数级的。
- **持续迭代** — 每次提交都是一次"加速"，让工具集不断进化。
- **最小代价，最大产出** — 好的工具应当以最少的配置完成最多的事情。

## 工具集

### 维护优先级说明

| 标记 | 含义 |
|------|------|
| 🟢 P0 | 核心工具，积极维护 |
| 🟡 P1 | 常用工具，定期维护 |
| 🟠 P2 | 低频使用，按需修复 |
| 🔴 P3 | 基本不维护，仅保留参考 |

### 仓库列表

| 项目 | 说明 | 语言 | 维护状态 | 优先级 |
|------|------|------|----------|--------|
| [P-STM32Cubedts](https://github.com/moment-NEW/P-STM32Cubedts) | STM32CubeMX `.ioc` → Zephyr Board DTS 转换器 | Python | 🟢 活跃开发 | P0 |
| [P-RTLog](https://github.com/moment-NEW/P-RTLog) | RTT 日志采集与分析工具 | — | 🟢 活跃开发 | P0 |
| [RTTView-Ciallo](https://github.com/moment-NEW/RTTView-Ciallo) | 更好用的 SEGGER-RTT Client，支持 J-Link 和 DAPLink | — | 🟡 仅维护 | P1 |
| [P-POCR](https://github.com/moment-NEW/P-POCR) | 嵌入式平台 OCR / 文字识别工具 | — | 🟡 维护中 | P1 |
| ARM-CLANG-EX | ARM Clang 编译器扩展与辅助工具 | — | 🔒 私有仓库 | P3 |

> 优先级不代表工具价值，仅反映当前维护意愿。欢迎提 Issue 或 PR 推动任何项目。

## 快速开始

```bash
# P0 — 活跃开发
git clone https://github.com/moment-NEW/P-STM32Cubedts.git
git clone https://github.com/moment-NEW/P-RTLog.git

# P1 — 仅维护
git clone https://github.com/moment-NEW/RTTView-Ciallo.git
git clone https://github.com/moment-NEW/P-POCR.git
```

各工具独立使用，详见各自仓库的 README。`ARM-CLANG-EX` 为私有仓库，暂不公开。

## 项目结构

```
P-Momentum/
├── README.md            # 本文件 — 工具集合总览
├── LICENSE              # MIT License
│
├── P-STM32Cubedts/      # 🟢 P0：STM32CubeMX → Zephyr DTS
├── P-RTLog/             # 🟢 P0：RTT 日志采集与分析
├── RTTView-Ciallo/      # 🟡 P1：SEGGER-RTT Client（仅维护）
├── P-POCR/              # 🟡 P1：嵌入式 OCR 工具
├── ARM-CLANG-EX/        # 🔒 P3：ARM Clang 编译器扩展（私有）
└── P-xxx/               # 🔜 未来子项目以 P- 前缀命名
```

## 设计原则

1. **开箱即用** — 工具应当自动探测环境，而非要求用户手动配置路径。
2. **渐进式复杂度** — 默认参数覆盖 80% 场景，高级选项按需暴露。
3. **日志可追溯** — 所有操作均有输出记录，便于复现和排查。
4. **跨平台优先** — 核心逻辑不绑定特定操作系统。

## 未来计划

以下方向已有初步想法，待时机成熟时会以独立仓库形式纳入本集合：

| 方向 | 说明 | 预期前缀 |
|------|------|----------|
| USB 协议栈工具 | USB 描述符解析、枚举调试、类驱动辅助 | `P-` |
| 静态初始化工具 | 编译期配置生成、链接脚本自动填充、静态资源管理 | `P-` |

> 具体仓库名称和内容确定后会更新此表。

## 声明

- 本集合中所有工具均为个人项目，**不代表任何公司或组织的官方立场**。
- 工具以实用为导向，代码质量随个人精力波动，不提供任何明示或暗示的保证。
- 欢迎 Issue / PR / 讨论，但请理解维护时间有限，响应可能不及时。
- 部分仓库（如 `ARM-CLANG-EX`）为私有仓库，不在公开范围内。

## 许可证

[MIT License](LICENSE) © 2026 Just Chen
