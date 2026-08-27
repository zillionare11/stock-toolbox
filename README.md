# 投资工具箱 - GitHub Pages 部署

## 文件说明

| 文件 | 说明 |
|------|------|
| `index.html` | 主页面（标签页导航） |
| `scoring.html` | A股买入评分系统 |
| `briefing.html` | 盘后情报 |
| `.nojekyll` | 禁用 Jekyll 处理 |

## 部署步骤

### 方法一：直接上传

1. 在 GitHub 创建新仓库（如 `stock-toolbox`）
2. 将本目录所有文件上传到仓库根目录
3. 进入仓库 Settings → Pages
4. Source 选择 `Deploy from a branch`，分支选 `main`，目录选 `/ (root)`
5. 保存后等待 1-2 分钟，访问 `https://<用户名>.github.io/stock-toolbox/`

### 方法二：Git 命令行

```bash
cd github-pages
git init
git add .
git commit -m "投资工具箱部署"
git branch -M main
git remote add origin https://github.com/<用户名>/stock-toolbox.git
git push -u origin main
```

然后在仓库 Settings → Pages 中开启 Pages。

## 功能说明

- **A股买入评分**：49 只沪深热门股扫描评分，四维模型（技术+趋势+基本面+情绪）
- **科技×金融早报**：9 大指数实时行情 + 7×24 快讯（利好/利空标签）
- **盘后情报**：持仓股分析（K线/技术指标/资金流向）+ 黄金行情

所有数据通过 JSONP 从公开行情接口获取，无需后端服务。
