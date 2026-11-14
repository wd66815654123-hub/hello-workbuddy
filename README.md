# hello-workbuddy

WorkBuddy × GitHub 连接验证仓库。

用于确认本机到 GitHub 的 Git 认证链路（SSH）已经完整打通，包括读取、提交与推送。

## 环境

| 项目 | 值 |
|---|---|
| 系统 | Windows |
| Git | 2.55.0.windows.3 |
| 认证方式 | SSH（ed25519） |
| 默认分支 | main |

## 验证记录

- `ssh -T git@github.com` → `Hi wd66815654123-hub! You've successfully authenticated`
- `git ls-remote` 读取公开仓库 → 正常返回 refs
- 首次推送 → 成功

## 日常用法

```bash
# 克隆（SSH，无需输入密码）
git clone git@github.com:wd66815654123-hub/hello-workbuddy.git

# 提交
git add .
git commit -m "feat: something"
git push
```

> 注：若在其他机器上使用，需要把该机器的公钥添加到 https://github.com/settings/keys 。
