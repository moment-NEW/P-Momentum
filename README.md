# P-Momentum

> **p = mv** — 动量是质量与速度的乘积；微小的积累，终将带来巨大的改变。

## 理念

P-Momentum 是一个以**嵌入式开发**为核心的工具集合。如同物理学中的动量——每一个工具都是一份微小的质量（*m*），每一次迭代都赋予它速度（*v*），当积累足够多时，即便是最轻量的工具，也能以极小的代价撬动巨大的效能。

我们相信：

- **积少成多** — 单个工具或许简单，但集合的力量是指数级的。
- **持续迭代** — 每次提交都是一次"加速"，让工具集不断进化。
- **最小代价，最大产出** — 好的工具应当以最少的配置完成最多的事情。

## 工具集

### 已纳入

| 项目 | 说明 | 语言 |
|------|------|------|
| [P-STM32Cubedts](https://github.com/moment-NEW/P-STM32Cubedts) | STM32CubeMX `.ioc` → Zephyr Board DTS 转换器 | Python |

### 规划中

以下工具以 VS Code Skill 形式存在，后续计划以独立 `P-` 仓库整合进本集合：

| 领域 | Skill 命令 | 说明 |
|------|-----------|------|
| 🔧 构建 | `/keil` `/gcc` | Keil MDK / GCC CMake 一键编译 |
| 🔌 烧录调试 | `/jlink` `/openocd` `/probe-rs` | 固件下载、在线调试、RTT 日志 |
| 📡 通信调试 | `/serial` `/can` `/net` | 串口、CAN/CAN-FD、网络抓包 |
| 🔄 工作流 | `/workflow` | 自动发现 → 构建 → 烧录 → 调试 → 观测 |

> 每整合一个工具，就为动量增加一份质量。欢迎提 Issue 或 PR。

## 快速开始

```bash
# 已有子项目
git clone https://github.com/moment-NEW/P-STM32Cubedts.git
cd P-STM32Cubedts && python src/ioc2dts.py --help
```

在 VS Code 中，已整合的 Skill 可直接通过命令面板调用（如 `/workflow`、`/jlink` 等）。

## 项目结构

```
P-Momentum/
├── README.md            # 本文件 — 工具集合总览
├── LICENSE              # MIT License
│
├── P-STM32Cubedts/      # ✅ 已纳入：STM32CubeMX → Zephyr DTS
├── P-xxx/               # 🔜 未来子项目以 P- 前缀命名
└── ...
```

## 设计原则

1. **开箱即用** — 工具应当自动探测环境，而非要求用户手动配置路径。
2. **渐进式复杂度** — 默认参数覆盖 80% 场景，高级选项按需暴露。
3. **日志可追溯** — 所有操作均有输出记录，便于复现和排查。
4. **跨平台优先** — 核心逻辑不绑定特定操作系统。

## 许可证

[MIT License](LICENSE) © 2026 Just Chen
