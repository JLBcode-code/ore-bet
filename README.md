# ⛏️ ORE 挖矿游戏一键下注脚本

## 📝 项目介绍

这是一个用于 ORE 协议挖矿游戏的自动下注脚本。支持批量选择格子进行下注，使用代码混淆技术保护核心功能。

## ⚙️ 配置参数

复制 `config.example.json` 为 `config.json` 并填入以下参数：

```json
{
  "rpcUrl": "https://mainnet.helius-rpc.com/?api-key=YOUR_API_KEY_HERE",
  "secretKeyBase58": "您的Base58格式私钥",
  "amountSol": 0.0001,
  "squares": [1, 2, 3]
}
```

### 参数说明：
- **rpcUrl**: Solana RPC 端点地址（替换YOUR_API_KEY_HERE为您的API密钥）
- **secretKeyBase58**: 您的钱包私钥（Base58格式，推荐）
- **secretKeyHex**: HEX格式私钥（可选，与Base58三选一）
- **secretKeyB64**: Base64格式私钥（可选，与Base58三选一）
- **amountSol**: 每个格子下注的SOL数量
- **squares**: 要下注的格子号数组（1-32）

## 🚀 运行方法

```bash
# 1. 安装依赖
npm install

# 2. 编辑 config.json 填入您的配置

# 3. 运行脚本(下注成功后Ctrl + C结束)
node place-bet-secure.min.js
```

## ⚠️ 注意事项

1. 请妥善保管配置文件中的私钥信息
2. 首次使用建议小额测试
3. 确保钱包有足够的 SOL 余额
4. 下注成功后Ctrl + C结束