# mac-test-tmp

GitHub Actions workflow 用于在 macOS 上创建临时 SSH 会话。

## 使用方法

1. 推送包含 `start` 关键字的提交信息到 main 分支：
   ```bash
   git commit -m "start a temp mac"
   git commit --allow-empty -m "start a temp mac"
   git push
   ```

2. Workflow 会自动启动 macOS runner 并创建 tmate SSH 会话

3. SSH 命令会在日志中输出

4. 输入 `exit mac` 结束会话

## 功能

- 自动检测架构 (x86_64 / arm64)
- 下载最新的 winload 二进制文件
- 使用 tmate 提供临时 SSH 访问
- 超时时间: 60 分钟
