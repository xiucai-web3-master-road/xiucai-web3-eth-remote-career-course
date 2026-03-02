# 📚 Ethereum Multi-DEX Course Syllabus

> **以太坊多DEX开发与实战 - 完整课程大纲**  
> 版本：v1.0.0 | 最后更新：2026-03

---

## 课程概览

| 属性 | 详情 |
|------|------|
| **课程名称** | 以太坊多DEX开发与实战 |
| **英文名称** | Ethereum Multi-DEX Development Masterclass |
| **课程时长** | 72课时（约60小时） |
| **授课方式** | 远程视频 + 在线实操 + 社区答疑 |
| **难度等级** | 中级 → 高级 |
| **目标学员** | 区块链开发者、DeFi从业者、Web3创业者 |

---

## 前置要求

### 必备技能
- [ ] 至少1年编程经验（JavaScript/Python/Solidity）
- [ ] 理解区块链基础概念（区块、交易、Gas）
- [ ] 熟悉Git版本控制
- [ ] 具备命令行操作能力

### 推荐预备知识
- 基础密码学概念（哈希、签名）
- HTTP/WebSocket协议基础
- 前端开发基础（HTML/CSS/React）

### 开发环境
- Node.js ≥ 18.0
- Git
- VS Code + Solidity插件
- MetaMask钱包

---

## 模块详情

### 模块一：DeFi与DEX基础理论 (8课时)

**学习目标**：建立DeFi生态全局认知，理解DEX核心机制

| 课时 | 主题 | 内容要点 | 资料 |
|:---:|------|---------|------|
| 1.1 | DeFi生态全景 | TVL概念、主要赛道（DEX/借贷/衍生品）、生态图谱 | [幻灯片](./resources/slides/module-01/defi-landscape.pdf) |
| 1.2 | 传统金融vs去中心化金融 | CeFi与DeFi对比、无托管优势、智能合约风险 | [对比表](./resources/cheatsheets/cefi-vs-defi.md) |
| 1.3 | DEX发展历程 | CEX→DEX演进、订单簿vs AMM、主要里程碑 | [时间线](./resources/diagrams/dex-evolution.png) |
| 1.4 | 自动做市商(AMM)机制 | 恒定乘积公式、价格曲线、滑点计算、无常损失 | [公式推导](./docs/module-01/amm-math.md) |
| 1.5 | 流动性池(LP)原理 | LP代币、份额计算、手续费分配、再投资机制 | [交互演示](https://example.com/amm-sim) |
| 1.6 | 多DEX聚合器原理 | 1inch/Paraswap架构、路由算法、MEV保护 | [架构图](./resources/diagrams/aggregator-arch.png) |
| 1.7 | **实操演示**：主流DEX平台 | Uniswap/Curve/Balancer操作演示、对比分析 | [录屏视频](https://youtube.com/xxx) |
| 1.8 | 模块测试与讨论 | 概念测验、案例分析：典型DEX失败案例 | [测试题](./test/module-01-quiz.md) |

**实战作业**：
- 在Uniswap Sepolia测试网完成3笔交换交易
- 分析一笔大额交易的滑点与价格影响
- 撰写学习笔记：对比Uniswap V2与V3的差异

---

### 模块二：Solidity智能合约基础 (10课时)

**学习目标**：掌握Solidity编程，能独立开发ERC20代币与基础合约

| 课时 | 主题 | 内容要点 | 代码 |
|:---:|------|---------|------|
| 2.1 | 以太坊架构深度解析 | EVM原理、Gas机制、存储布局、事件日志 | [笔记](./docs/module-02/evm-deep-dive.md) |
| 2.2 | Solidity编程入门 | 数据类型、函数修饰器、事件、错误处理 | [示例代码](./contracts/examples/Basics.sol) |
| 2.3 | ERC20代币标准实现 | 标准接口详解、转账逻辑、授权机制、安全考虑 | [ERC20合约](./contracts/examples/MyToken.sol) |
| 2.4 | Hardhat开发环境 | 项目初始化、网络配置、插件使用、调试技巧 | [配置模板](./hardhat.config.js) |
| 2.5 | 智能合约安全基础 | 重入攻击、整数溢出、访问控制、检查-生效-交互 | [安全清单](./docs/security-checklist.md) |
| 2.6 | **演示**：Solidity开发(上) | 编写完整ERC20合约、单元测试编写 | [录屏视频](https://youtube.com/xxx) |
| 2.7 | **演示**：Solidity开发(下) | 调试技巧、Gas优化、部署脚本 | [录屏视频](https://youtube.com/xxx) |
| 2.8 | 多DEX合约交互原理 | 跨合约调用、接口设计、事件监听、回调机制 | [交互示例](./contracts/examples/ContractInteraction.sol) |
| 2.9 | **实操**：部署测试代币 | Sepolia测试网部署、验证、水龙头获取 | [操作指南](./docs/module-02/deploy-guide.md) |
| 2.10 | 模块考核 | 智能合约编写测试、代码审查 | [考核题目](./test/module-02-exam.md) |

**实战项目**：
- 开发一个功能完整的ERC20代币合约
- 实现额外的功能：销毁、暂停、黑名单
- 部署到Sepolia测试网并验证源码

---

### 模块三：AMM与流动性池深入 (10课时)

**学习目标**：深入理解AMM数学模型，能分析复杂流动性策略

| 课时 | 主题 | 内容要点 | 资源 |
|:---:|------|---------|------|
| 3.1 | AMM数学模型详解 | x*y=k曲线、价格影响公式、流动性深度 | [数学推导](./docs/module-03/amm-math-deep.md) |
| 3.2 | Uniswap V2架构剖析 | Factory-Router模式、Pair合约结构、事件系统 | [源码分析](./docs/module-03/uniswap-v2-arch.md) |
| 3.3 | Uniswap V3集中流动性 | Tick系统、仓位NFT、多费率层级、Oracle功能 | [V3白皮书](https://uniswap.org/whitepaper-v3.pdf) |
| 3.4 | Curve稳定币交换 | StableSwap算法、低滑点设计、多代币池 | [Curve文档](https://curve.readthedocs.io/) |
| 3.5 | Balancer加权池 | 多代币池、自定义权重、投资池模式 | [Balancer文档](https://docs.balancer.fi/) |
| 3.6 | 多DEX流动性聚合 | 跨协议流动性整合、最优报价算法、Gas优化 | [聚合算法](./docs/module-03/aggregation-algo.md) |
| 3.7 | **演示**：Uniswap V2源码分析 | 核心函数解读、状态流转、安全机制 | [录屏视频](https://youtube.com/xxx) |
| 3.8 | **演示**：流动性池操作 | 添加/移除流动性、仓位管理、收益追踪 | [录屏视频](https://youtube.com/xxx) |
| 3.9 | 无常损失计算与对冲 | 数学建模、对冲策略、期权保护 | [计算工具](./resources/cheatsheets/il-calculator.md) |
| 3.10 | **实操**：AMM模拟器 | 参数调整、收益分析、策略回测 | [在线工具](https://example.com/amm-sim) |

**实战作业**：
- 使用Python实现AMM价格计算模拟器
- 分析Uniswap V3不同费率层级的适用场景
- 计算并提供流动性策略的无常损失预期

---

### 模块四：DEX智能合约开发实战 (12课时)

**学习目标**：从零构建完整DEX合约，通过安全测试

| 课时 | 主题 | 内容要点 | 代码 |
|:---:|------|---------|------|
| 4.1 | DEX架构设计 | Factory模式、Router设计、状态管理、升级策略 | [架构图](./resources/diagrams/dex-arch.png) |
| 4.2 | 流动性池工厂合约 | 动态创建Pair、CREATE2地址计算、事件发射 | [Factory.sol](./contracts/core/Factory.sol) |
| 4.3 | 路由合约实现 | 路径查找、多跳交换、ETH包装、滑点保护 | [Router.sol](./contracts/core/Router.sol) |
| 4.4 | 核心交换逻辑 | 代币互换、价格计算、K值恒定验证、重入防护 | [Pair.sol](./contracts/core/Pair.sol) |
| 4.5 | 手续费机制设计 | 协议费、LP奖励、动态费率、FeeTo设置 | [Fee机制](./docs/module-04/fee-design.md) |
| 4.6 | **演示**：Hardhat项目搭建 | 工程化配置、多网络支持、任务定制 | [录屏视频](https://youtube.com/xxx) |
| 4.7 | **演示**：Arbitrum L2集成 | 二层网络部署、成本对比、桥接使用 | [录屏视频](https://youtube.com/xxx) |
| 4.8 | 安全考虑与攻击防护 | 闪电贷防护、价格操纵防御、重入锁 | [安全合约](./contracts/core/SecureDEX.sol) |
| 4.9 | 合约测试策略 | 单元测试、集成测试、覆盖率要求、模糊测试 | [测试套件](./test/unit/DEX.test.js) |
| 4.10 | **演示**：完整测试流程 | Foundry/Hardhat测试框架、Gas快照 | [录屏视频](https://youtube.com/xxx) |
| 4.11 | 多DEX兼容性设计 | 通用接口标准、适配器模式、代理合约 | [适配器](./contracts/core/DEXAdapter.sol) |
| 4.12 | 项目提交与代码审查 | 导师点评、优化建议、最佳实践 | [审查清单](./docs/code-review-checklist.md) |

**实战项目**：简易DEX合约
- 实现Factory创建交易对
- 实现Router支持多跳交换
- 完整测试覆盖（≥90%）
- 部署到Sepolia并验证

---

### 模块五：高级DEX功能开发 (12课时)

**学习目标**：实现高级交易功能，构建多DEX聚合器

| 课时 | 主题 | 内容要点 | 代码 |
|:---:|------|---------|------|
| 5.1 | 限价单与订单簿 | 链下订单簿、链上结算、撮合逻辑、订单生命周期 | [OrderBook.sol](./contracts/advanced/OrderBook.sol) |
| 5.2 | 闪电贷功能实现 | 无抵押借贷、原子性操作、套利应用、回调安全 | [FlashLoan.sol](./contracts/advanced/FlashLoan.sol) |
| 5.3 | 多代币路由优化 | Dijkstra算法、最优路径计算、Gas成本模型 | [RouterV2.sol](./contracts/advanced/RouterV2.sol) |
| 5.4 | TWAP价格预言机 | 时间加权平均价格、操纵抵抗、价格偏差处理 | [Oracle.sol](./contracts/advanced/TWAPOracle.sol) |
| 5.5 | 治理代币与DAO | 投票机制、协议参数治理、收益分配、委托投票 | [Governance.sol](./contracts/advanced/Governance.sol) |
| 5.6 | **演示**：工厂高级功能 | 自定义费率、权限管理、暂停机制 | [录屏视频](https://youtube.com/xxx) |
| 5.7 | **演示**：多DEX聚合器架构 | 报价聚合、路由分发、执行优化 | [录屏视频](https://youtube.com/xxx) |
| 5.8 | 跨链DEX架构 | 桥接协议、消息传递、状态同步、流动性分割 | [跨链设计](./docs/module-05/cross-chain.md) |
| 5.9 | MEV保护与隐私 | 防三明治攻击、隐私交易、Flashbots集成 | [MEV防护](./docs/module-05/mev-protection.md) |
| 5.10 | 形式化验证与安全审计 | 数学证明、符号执行、审计工具、报告解读 | [验证示例](./test/formal-verification/) |
| 5.11 | **演示**：安全测试流程 | Slither、Mythril、Echidna实战 | [录屏视频](https://youtube.com/xxx) |
| 5.12 | 高级项目答辩 | 功能演示、技术答辩、优化建议 | [评分标准](./docs/module-05/grading-rubric.md) |

**实战项目**：多DEX聚合器
- 集成Uniswap V2/V3、Curve报价
- 实现最优路径算法
- 支持大额交易拆分
- 完整安全测试与审计报告

---

### 模块六：前端与Web3应用开发 (12课时)

**学习目标**：构建生产级DApp前端，实现完整用户交互

| 课时 | 主题 | 内容要点 | 代码 |
|:---:|------|---------|------|
| 6.1 | React + Web3项目架构 | 项目结构、状态管理、性能优化、错误边界 | [架构指南](./frontend/docs/architecture.md) |
| 6.2 | Ethers.js深度使用 | Provider/Signer、合约交互、事件监听、批量请求 | [工具库](./frontend/src/utils/ethers.ts) |
| 6.3 | 钱包连接与多链支持 | MetaMask、WalletConnect、网络切换、账户监听 | [连接组件](./frontend/src/components/WalletConnect.tsx) |
| 6.4 | 代币列表与价格展示 | Token列表管理、价格获取、缓存策略、实时更新 | [价格钩子](./frontend/src/hooks/usePrices.ts) |
| 6.5 | 交换界面设计与实现 | 输入验证、滑点设置、交易预览、确认流程 | [交换组件](./frontend/src/components/Swap.tsx) |
| 6.6 | 流动性管理界面 | 添加/移除LP、仓位展示、收益计算、历史记录 | [流动性组件](./frontend/src/components/Liquidity.tsx) |
| 6.7 | **演示**：React项目初始化 | 组件设计、路由配置、样式系统、主题切换 | [录屏视频](https://youtube.com/xxx) |
| 6.8 | **演示**：合约前端集成 | 读写操作、交易状态、通知系统、错误处理 | [录屏视频](https://youtube.com/xxx) |
| 6.9 | **演示**：交换功能完整实现 | 代币选择、报价获取、交易执行、状态追踪 | [录屏视频](https://youtube.com/xxx) |
| 6.10 | 多DEX聚合界面 | 报价对比、最优路径展示、一键交换、Gas估算 | [聚合组件](./frontend/src/components/Aggregator.tsx) |
| 6.11 | 安全测试与UX优化 | 防钓鱼、交易确认、加载状态、空状态处理 | [UX检查清单](./frontend/docs/ux-checklist.md) |
| 6.12 | 完整DApp部署 | Vercel部署、性能监控、分析集成、SEO优化 | [部署指南](./frontend/docs/deployment.md) |

**实战项目**：完整DApp界面
- 实现代币交换全流程
- 流动性添加/移除界面
- 交易历史与状态追踪
- 响应式设计，支持移动端

---

### 模块七：生产部署与优化 (8课时)

**学习目标**：掌握生产环境部署、监控与优化

| 课时 | 主题 | 内容要点 | 资源 |
|:---:|------|---------|------|
| 7.1 | 多DEX聚合器完整开发 | 整合所有模块、端到端测试、性能基准 | [完整代码](./contracts/examples/CompleteDEX.sol) |
| 7.2 | **实战**：构建个人DEX平台 | 从0到1完整项目开发、需求分析、架构设计 | [项目模板](./templates/final-project/) |
| 7.3 | Gas优化与Layer2部署 | Arbitrum/Optimism部署、成本对比、桥接指南 | [优化技巧](./docs/module-07/gas-optimization.md) |
| 7.4 | 生产环境安全清单 | 部署前检查、密钥管理、监控设置、应急预案 | [生产清单](./docs/module-07/production-checklist.md) |
| 7.5 | DeFi协议经济模型 | Tokenomics设计、激励相容、可持续性分析、风险评估 | [模型模板](./docs/module-07/tokenomics-template.md) |
| 7.6 | 行业案例深度分析 | Uniswap/Curve/SushiSwap成功与失败案例复盘 | [案例分析](./docs/module-07/case-studies.md) |
| 7.7 | 职业发展指导 | 求职技巧、作品集准备、面试题库、行业资源 | [职业指南](./docs/module-07/career-guide.md) |
| 7.8 | 结业考试与项目展示 | 理论考试（50%）+ 实战项目答辩（50%） | [考试大纲](./docs/module-07/final-exam.md) |

**毕业项目**：生产级DEX平台
- 完整功能：交换+流动性+聚合
- 部署到Arbitrum测试网
- 通过安全审计（使用自动化工具）
- 前端部署并可公开访问
- 撰写技术文档与白皮书

---

## 课程资源

### 开发工具
- [Hardhat](https://hardhat.org/) - 以太坊开发环境
- [Foundry](https://book.getfoundry.sh/) - 快速Rust开发工具包
- [OpenZeppelin](https://docs.openzeppelin.com/) - 安全合约库
- [Tenderly](https://tenderly.co/) - 交易模拟与调试

### 学习资源
- [Ethereum文档](https://ethereum.org/developers)
- [Solidity官方文档](https://docs.soliditylang.org/)
- [Uniswap文档](https://docs.uniswap.org/)
- [Curve文档](https://curve.readthedocs.io/)

### 社区支持
- [课程Discord](https://discord.gg/your-invite)
- [GitHub Discussions](https://github.com/yourusername/ethereum-multi-dex-course/discussions)
- [Stack Exchange Ethereum](https://ethereum.stackexchange.com/)

---

## 评估与认证

### 评分标准
| 组成部分 | 权重 | 说明 |
|---------|:---:|:---|
| 模块作业 | 30% | 7个模块的实战作业 |
| 项目作品 | 40% | 4个渐进式项目 |
| 结业考试 | 20% | 理论+实操综合测试 |
| 社区贡献 | 10% | 文档改进、代码贡献、答疑 |

### 认证等级
- 🥉 **初级开发者**：完成模块01-04，通过基础考试
- 🥈 **中级开发者**：完成所有模块，通过完整考试
- 🥇 **高级开发者**：完成毕业项目，获得社区认可

---

## 更新日志

- **v1.0.0** (2024-01-15) - 初始版本发布
- 模块01-07完整大纲
- 基础代码框架
- 文档与资源整理

---

**本课程持续更新中，欢迎提交Issue建议改进内容！**

[⬆ 返回顶部](#ethereum-multi-dex-course-syllabus)

