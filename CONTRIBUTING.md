# 🤝 Contributing to Ethereum Multi-DEX Course

感谢您对以太坊多DEX课程项目的关注！我们欢迎所有形式的贡献，包括但不限于：

- 🐛 报告Bug或问题
- 📖 改进文档和翻译
- 💻 提交代码改进
- 🎨 设计资源（图表、幻灯片）
- 📝 分享学习笔记和案例
- 💡 提出新功能建议

---

## 📋 贡献指南目录

1. [行为准则](#行为准则)
2. [如何开始](#如何开始)
3. [提交Issue](#提交issue)
4. [提交Pull Request](#提交pull-request)
5. [开发规范](#开发规范)
6. [文档规范](#文档规范)
7. [社区互动](#社区互动)

---

## 行为准则

本项目采用 [Contributor Covenant](https://www.contributor-covenant.org/) 行为准则。

### 我们的承诺

- 使用友好和包容的语言
- 尊重不同的观点和经验
- 优雅地接受建设性批评
- 关注对社区最有利的事情
- 对其他社区成员表示同理心

### 不可接受的行为

- 使用性别歧视、种族歧视或排他性语言
- 骚扰、侮辱或贬低他人
- 发布暴力或威胁性内容
- 未经许可发布他人私人信息
- 其他不道德或不专业的行为

**违规处理**：项目维护者有权删除、编辑或拒绝不符合本行为准则的评论、提交、代码、wiki编辑、问题和其他贡献。

---

## 如何开始

### 首次贡献者

如果您是第一次参与开源项目，建议从以下任务开始：

1. **文档改进**：修复拼写错误、改进表述、添加翻译
2. **示例代码**：为现有概念添加更清晰的代码示例
3. **测试用例**：补充缺失的单元测试
4. **问题解答**：在Discussions中帮助其他学习者

### 环境设置

```bash
# 1. Fork本仓库
# 点击页面右上角的Fork按钮

# 2. 克隆您的Fork
git clone https://github.com/YOUR_USERNAME/ethereum-multi-dex-course.git
cd ethereum-multi-dex-course

# 3. 添加上游仓库
git remote add upstream https://github.com/original-owner/ethereum-multi-dex-course.git

# 4. 安装依赖
npm install

# 5. 创建分支
git checkout -b feature/your-feature-name

# 6. 开始开发！
```

---

## 提交Issue

### 报告Bug

在提交Bug报告前，请先：
- [ ] 搜索现有Issue，避免重复
- [ ] 确认Bug在最新版本中仍然存在
- [ ] 尝试隔离问题，提供最小复现步骤

**Bug报告模板**：

```markdown
**描述**
清晰简洁地描述Bug是什么。

**复现步骤**
1. 进入 '...'
2. 点击 '...'
3. 滚动到 '...'
4. 看到错误

**期望行为**
清晰描述您期望发生什么。

**截图**
如果适用，添加截图帮助解释问题。

**环境信息**
- OS: [e.g. macOS, Windows]
- Node版本: [e.g. 18.12.0]
- Hardhat版本: [e.g. 2.19.0]
- 浏览器: [e.g. Chrome, Safari]

**附加信息**
任何其他相关信息。
```

### 功能建议

**功能建议模板**：

```markdown
**功能描述**
清晰描述您想要的功能。

**动机**
解释为什么这个功能对课程有价值。

**实现方案**
如果您有实现思路，请描述。

**替代方案**
您考虑过的其他解决方案。

**附加信息**
任何截图、原型或参考资料。
```

### 内容改进

针对课程内容的问题（如概念错误、过时信息）：

```markdown
**位置**
文件路径或视频链接。

**当前内容**
描述当前存在的问题。

**建议改进**
您的改进建议。

**参考来源**
支持您建议的权威资料链接。
```

---

## 提交Pull Request

### PR流程

1. **更新您的Fork**
   ```bash
   git fetch upstream
   git rebase upstream/main
   ```

2. **创建功能分支**
   ```bash
   git checkout -b feature/description
   # 或
   git checkout -b fix/description
   ```

3. **提交更改**
   - 遵循[开发规范](#开发规范)
   - 编写清晰的提交信息
   - 确保测试通过

4. **推送并创建PR**
   ```bash
   git push origin feature/description
   ```
   然后在GitHub上创建Pull Request。

### PR模板

```markdown
## 描述
简要描述这个PR做了什么。

## 类型
- [ ] Bug修复
- [ ] 新功能
- [ ] 文档改进
- [ ] 代码重构
- [ ] 性能优化
- [ ] 测试补充

## 检查清单
- [ ] 代码遵循项目规范
- [ ] 测试通过
- [ ] 文档已更新
- [ ] 提交信息清晰

## 相关Issue
Fixes #(issue编号)

## 截图（如适用）
```

### 代码审查

- 所有PR都需要至少1个审查者批准
- 审查者会检查：代码质量、安全性、文档、测试覆盖
- 请积极响应审查意见

---

## 开发规范

### Solidity代码规范

遵循 [Solidity Style Guide](https://docs.soliditylang.org/en/latest/style-guide.html) 和以下附加规则：

```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.19;

import "@openzeppelin/contracts/token/ERC20/IERC20.sol";

/**
 * @title 合约标题
 * @notice 合约功能简要说明
 * @dev 实现细节说明
 */
contract ExampleContract {
    // 状态变量
    uint256 public constant MAX_SUPPLY = 1000000;
    mapping(address => uint256) public balances;
    
    // 事件
    event Transfer(address indexed from, address indexed to, uint256 value);
    
    // 错误
    error InsufficientBalance(uint256 available, uint256 required);
    
    /**
     * @notice 函数功能说明
     * @param _to 接收地址
     * @param _amount 转账金额
     * @return success 是否成功
     */
    function transfer(address _to, uint256 _amount) external returns (bool success) {
        if (balances[msg.sender] < _amount) {
            revert InsufficientBalance(balances[msg.sender], _amount);
        }
        
        balances[msg.sender] -= _amount;
        balances[_to] += _amount;
        
        emit Transfer(msg.sender, _to, _amount);
        return true;
    }
}
```

**规范要点**：
- 使用 `^0.8.19` 或更高版本
- 所有函数必须有NatSpec注释
- 使用自定义错误替代require字符串
- 事件参数使用 `indexed` 优化查询
- 遵循检查-生效-交互模式
- 使用OpenZeppelin库处理标准功能

### JavaScript/TypeScript规范

- 使用ESLint + Prettier配置
- 优先使用TypeScript
- 异步操作使用async/await
- 错误处理使用try/catch

### 提交信息规范

遵循 [Conventional Commits](https://www.conventionalcommits.org/)：

```
<type>(<scope>): <description>

[optional body]

[optional footer]
```

**类型**：
- `feat`: 新功能
- `fix`: Bug修复
- `docs`: 文档更新
- `style`: 代码格式（不影响功能）
- `refactor`: 代码重构
- `test`: 测试相关
- `chore`: 构建/工具更新

**示例**：
```
feat(contracts): 添加多跳交换功能

实现支持多流动性池路径的代币交换，
优化Gas成本和滑点保护。

Closes #123
```

---

## 文档规范

### Markdown格式

- 使用ATX风格的标题（#）
- 代码块指定语言
- 表格对齐使用冒号
- 图片添加替代文本

### 内容标准

- **准确性**：所有技术概念必须准确，引用权威来源
- **清晰性**：使用简洁语言，避免冗长
- **完整性**：提供足够的上下文和示例
- **时效性**：定期更新过时内容

### 翻译贡献

我们欢迎多语言翻译：

1. 在 `docs/i18n/` 创建语言目录（如 `zh-CN/`, `en/`）
2. 保持原文结构
3. 技术术语保留英文并添加解释
4. 提交PR时标注翻译语言

---

## 社区互动

### Discord频道

- `#general` - 一般讨论
- `#questions` - 学习问题求助
- `#showcase` - 项目展示
- `#dev-chat` - 开发技术讨论
- `#i18n` - 翻译协作

### 成为维护者

长期贡献者可以申请成为项目维护者：

1. 持续贡献代码/文档 ≥3个月
2. 帮助审查其他PR
3. 积极参与社区讨论
4. 联系现有维护者申请

---

## 奖励与认可

### 贡献者等级

- 🌱 **Newcomer**: 首次合并PR
- 🌿 **Contributor**: 合并5+ PR
- 🌳 **Active Contributor**: 合并20+ PR
- ⭐ **Core Contributor**: 持续贡献并帮助社区
- 🏆 **Maintainer**: 项目维护权限

### 特别感谢

- 文档翻译贡献者将在对应语言README中致谢
- 重大功能贡献者将在Release Notes中特别提及
- 优秀学习者项目将在社区展示

---

## 常见问题

**Q: 我没有编程经验，可以贡献吗？**  
A: 当然可以！您可以帮助改进文档、翻译内容、测试课程或分享学习反馈。

**Q: 我的PR为什么还没有被审查？**  
A: 维护者都是志愿者，通常会在7天内响应。如果紧急，可以在PR中@维护者。

**Q: 我可以为课程添加新的模块吗？**  
A: 欢迎建议！请先开Issue讨论新模块的内容和结构，避免重复工作。

**Q: 发现课程内容有错误怎么办？**  
A: 直接提交Issue或PR修复。对于重大概念错误，我们会快速响应。

---

## 联系我们

- 📧 Email: xcai02716@gmail.com
- 💬 社区: [加入秀才web3大师之路社区](https://xiucai-web3-develop-guide.vercel.app/login)
- 🐦 微信: [@GreenPoint8888](https://xiucai-web3-develop-guide.vercel.app/login)

再次感谢您的贡献！🙏

---

**最后更新**: 2026-03-02

