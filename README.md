# 🚀 Ethereum Multi-DEX Course

[![Solidity](https://img.shields.io/badge/Solidity-%5E0.8.19-363636?style=flat&logo=solidity&logoColor=white)](https://soliditylang.org/)
[![Hardhat](https://img.shields.io/badge/Hardhat-2.19.0-F7C52C?style=flat&logo=ethereum&logoColor=black)](https://hardhat.org/)
[![React](https://img.shields.io/badge/React-18.2-61DAFB?style=flat&logo=react&logoColor=black)](https://react.dev/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

> **从0到1构建以太坊多DEX聚合器 | 开源视频课程 + 实战代码**

中文 | [课程官网](https://xiucai-web3-master-road-solana.vercel.app/web3-fullstack) | [视频播放列表](https://xiucai-web3-develop-guide.vercel.app/login)

---

## 📚 课程简介

本课程是一套完整的**开源以太坊多DEX开发课程**，涵盖从DeFi基础理论到生产级DEX聚合器开发的完整路径。通过7大模块、60+课时，带你掌握：

- 🏗️ AMM自动做市商核心机制
- 💻 Solidity智能合约开发
- 🔗 多DEX聚合路由算法
- ⚛️ React + Web3前端开发
- 🛡️ 合约安全与形式化验证
- 🚀 Layer2部署与Gas优化

---

## 🎯 适合人群

- **区块链开发者**：想系统学习DeFi协议开发
- **Web2转Web3**：有前端/后端基础，转向Web3开发
- **DeFi研究员**：深入理解DEX底层机制
- **创业者**：构建自己的DEX或DeFi产品

**前置要求**：
- 基础编程经验（JavaScript/Python/Solidity）
- 了解区块链基础概念
- 具备命令行操作能力

---

## 📋 课程大纲

| 模块 | 主题 | 课时 | 实战项目 | 难度 |
|:---:|------|:---:|:---------|:----:|
| 01 | [DeFi与DEX基础](./docs/module-01-defi-basics.md) | 8 | 主流DEX平台操作 | ⭐ |
| 02 | [Solidity智能合约基础](./docs/module-02-solidity-fundamentals.md) | 10 | ERC20代币部署 | ⭐⭐ |
| 03 | [AMM与流动性池深入](./docs/module-03-amm-deep-dive.md) | 10 | AMM数学建模 | ⭐⭐ |
| 04 | [DEX智能合约开发](./docs/module-04-dex-development.md) | 12 | **简易DEX合约** | ⭐⭐⭐ |
| 05 | [高级DEX功能开发](./docs/module-05-advanced-features.md) | 12 | **多DEX聚合器** | ⭐⭐⭐⭐ |
| 06 | [前端与Web3集成](./docs/module-06-frontend-integration.md) | 12 | **完整DApp界面** | ⭐⭐⭐ |
| 07 | [生产部署与优化](./docs/module-07-production-deployment.md) | 8 | **主网部署** | ⭐⭐⭐⭐ |

**总课时**：72课时（约60小时）  
**实战项目**：4个渐进式项目 + 1个毕业作品

---

## 🛠️ 技术栈

### 智能合约
- **Solidity** ^0.8.19 - 智能合约语言
- **Hardhat** - 开发框架与测试环境
- **Foundry** - 高级测试与Gas优化
- **OpenZeppelin** - 安全合约库
- **Slither/Mythril** - 安全分析工具

### 前端开发
- **React 18** + **TypeScript** - UI框架
- **Ethers.js v6** - 区块链交互
- **Wagmi** + **RainbowKit** - 钱包连接
- **TailwindCSS** - 样式系统
- **Viem** - 现代Web3工具库

### 部署与运维
- **Alchemy/Infura** - 节点服务
- **Vercel** - 前端托管
- **Arbitrum/Optimism** - Layer2部署
- **Tenderly** - 交易模拟与调试

---

## 🚀 快速开始

### 环境准备

```bash
# 克隆仓库
git clone https://github.com/yourusername/ethereum-multi-dex-course.git
cd ethereum-multi-dex-course

# 安装依赖
npm install

# 配置环境变量
cp .env.example .env
# 编辑 .env 文件，添加你的 API keys
```

### 本地开发

```bash
# 启动本地节点
npx hardhat node

# 编译合约
npx hardhat compile

# 运行测试
npx hardhat test

# 部署到本地
npx hardhat run scripts/deploy.js --network localhost
```

### 前端开发

```bash
cd frontend
npm install
npm run dev
```

访问 `http://localhost:3000` 查看DApp界面。

---

## 📁 项目结构

```
ethereum-multi-dex-course/
├── contracts/          # 智能合约源码
│   ├── core/          # 核心DEX合约
│   ├── interfaces/    # 接口定义
│   ├── libraries/     # 工具库
│   └── examples/      # 示例合约
├── frontend/          # React前端应用
│   ├── src/
│   └── public/
├── test/              # 测试套件
│   ├── unit/          # 单元测试
│   ├── integration/   # 集成测试
│   └── fuzzing/       # 模糊测试
├── docs/              # 课程文档
├── scripts/           # 部署与工具脚本
└── resources/         # 课件与资源
```

---

## 🎓 学习路径建议

### 路径A：完整系统学习（推荐）
按模块顺序学习，完成所有实战项目，预计8-10周。

### 路径B：快速上手开发
1. 模块01-02（基础）
2. 模块04（简易DEX）
3. 模块06（前端集成）
4. 直接参考 `examples/` 代码

### 路径C：高级开发者进阶
跳过基础模块，直接学习：
- 模块03（AMM深入）
- 模块05（高级功能）
- 模块07（生产部署）
- 研究 `MultiDEXAggregator.sol` 源码

---

## 📝 实战项目

### 项目1：简易DEX合约
构建基础的代币交换合约，支持：
- ERC20代币互换
- 流动性添加/移除
- 恒定乘积做市

**代码位置**：`contracts/examples/SimpleDEX.sol`

### 项目2：多DEX聚合器
实现跨Uniswap V2/V3、Curve的最优路径交换：
- 多源报价聚合
- 最优路由算法
- Gas成本优化

**代码位置**：`contracts/examples/MultiDEXAggregator.sol`

### 项目3：完整DApp界面
React前端实现：
- 钱包连接
- 代币交换界面
- 流动性管理
- 实时价格图表

**代码位置**：`frontend/src/`

### 毕业项目：生产级DEX平台
整合所有模块，部署到测试网/主网。

---

## 🔗 重要资源

### 文档
- [课程完整大纲](./COURSE_SYLLABUS.md)
- [贡献指南](./CONTRIBUTING.md)
- [安全审计清单](./docs/security-checklist.md)
- [常见问题FAQ](./docs/FAQ.md)

### 外部资源
- [Uniswap V3白皮书](https://uniswap.org/whitepaper-v3.pdf)
- [Ethereum文档](https://ethereum.org/developers)
- [OpenZeppelin合约库](https://docs.openzeppelin.com/)
- [DeFi Llama](https://defillama.com/) - TVL数据

### 社区
- [Discord学习群](https://discord.gg/your-invite)
- [论坛讨论区](https://github.com/yourusername/ethereum-multi-dex-course/discussions)
- [Twitter更新](https://twitter.com/yourhandle)

---

## 🤝 贡献指南

欢迎贡献！请阅读 [CONTRIBUTING.md](./CONTRIBUTING.md) 了解如何：
- 提交Issue报告问题
- 提交PR改进代码
- 完善课程文档
- 分享学习笔记

### 贡献者
感谢所有贡献者！

<a href="https://github.com/yourusername/ethereum-multi-dex-course/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=yourusername/ethereum-multi-dex-course" />
</a>

---

## 📜 许可证

本课程采用 [MIT License](./LICENSE) 开源协议。

- ✅ 允许商业使用
- ✅ 允许修改和分发
- ✅ 允许私人使用
- ⚠️ 不提供担保

**免责声明**：本课程仅供教育目的，代码未经正式审计，不建议直接用于生产环境。

---

## 🌟 Star History

[![Star History Chart](https://api.star-history.com/svg?repos=yourusername/ethereum-multi-dex-course&type=Date)](https://star-history.com/#yourusername/ethereum-multi-dex-course&Date)

---

## 📞 联系我们

- 📧 Email: xcai02716@gmail.com
- 🐦 官网: [@秀才web3大师之路官网](https://xiucai-web3-master-road-solana.vercel.app/web3-fullstack)
- 💬 社区: [加入秀才web3大师之路社区](https://xiucai-web3-develop-guide.vercel.app/login)

---

**如果这个项目对你有帮助，请给个 ⭐ Star 支持一下！**
扫描二维码,开启您的以太坊web3远程职业之旅！
1. 微信号 | WeChat
   - ![微信二维码](./微信号.jpg)
   - 账号 | Account：GreenPoint8888
   - 说明 | Description：一对一答疑，技术指导 | One-on-one Q&A, technical guidance
