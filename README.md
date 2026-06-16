# Claude Desktop MSIX 获取器

利用 GitHub Actions 在境外服务器下载 Claude Desktop MSIX 安装包，然后通过 GitHub 加速取回本地。

## 使用方法

### 1. 将此仓库推送到你的 GitHub

```bash
# 在 GitHub 网页上创建一个新仓库（比如叫 claude-msix-fetcher），不要勾选任何初始化选项

cd C:\Users\Gqx\Desktop\claude-msix-fetcher
git init
git add .
git commit -m "init"
git remote add origin https://github.com/你的用户名/claude-msix-fetcher.git
git push -u origin main
```

### 2. 触发 Workflow

1. 打开你的 GitHub 仓库页面
2. 点击 **Actions** 标签
3. 左侧选 **获取 Claude Desktop MSIX**
4. 点击 **Run workflow** → **Run workflow**
5. 等待约 2-3 分钟完成

### 3. 下载 MSIX

Workflow 完成后：
- 进入 **Releases** 页面（右侧栏）
- 下载 `Claude.msix`

### 4. 安装

以**管理员身份**打开 PowerShell：
```powershell
Add-AppxPackage -Path "C:\Users\Gqx\Downloads\Claude.msix"
```

若报错需开发者模式：**设置 → 系统 → 开发者选项 → 开启"开发人员模式"**。

---

## 备用方案：百度网盘

如果不想折腾 GitHub Actions，直接从百度网盘下载：
```
https://pan.baidu.com/s/1FDVMR0n5bb5BuFUNMAojyQ?pwd=9d8a
提取码: 9d8a
版本: v1.9255.0
```
