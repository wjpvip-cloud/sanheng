# 三衡生活 · 文献库站点

> 大医派紫尘阁 · 项目战略文献库

## 文件说明

```
sanheng-site/
├── index.html              首页（文献入口）
├── docs/
│   ├── community.html      01 · 共同体战略
│   ├── structure.html      02 · 双主体整合
│   └── roadmap.html        03 · 完整落地计划
└── README.md               本说明
```

## 部署到 GitHub Pages（5 分钟）

### 步骤 1：在 GitHub 新建仓库

1. 打开 https://github.com/new
2. **Repository name** 填：`sanheng`（或你想要的名字）
3. **Public**（必须公开，Pages 才能免费用）
4. 不勾选 "Add a README file"（已经有了）
5. 点 **Create repository**

### 步骤 2：上传文件（最简单的方式）

新仓库页面会有一行字 **"uploading an existing file"**，点它。

把整个 `sanheng-site` 文件夹里的 **所有内容**（注意是里面的内容，不是文件夹本身）拖进去：
- `index.html`
- `docs` 文件夹（连同里面三个 html）
- `README.md`

下面有个绿色按钮 **Commit changes** ，点它。

### 步骤 3：开启 GitHub Pages

1. 进入仓库 → 上方点 **Settings**
2. 左侧菜单 → **Pages**
3. **Source** 选 `Deploy from a branch`
4. **Branch** 选 `main` ，文件夹选 `/ (root)` ，点 **Save**
5. 等 1-2 分钟，刷新这个页面

### 步骤 4：拿到网址

页面顶部会出现：

```
✓ Your site is live at https://wjpvip-cloud.github.io/sanheng/
```

这就是公开网址，全球任何人都能访问。

---

## 后续怎么继续加文档？

### 方法 A · 网页直接传（适合偶尔加文件）

1. 进入仓库
2. 点 **Add file** → **Upload files**
3. 拖新文件进去 → Commit
4. 大约 1 分钟后网址自动更新

### 方法 B · 装 GitHub Desktop（推荐长期用）

下载：https://desktop.github.com

装好后把仓库 clone 到本地某个文件夹，以后改文件就在本地改，改完点 Commit + Push 即可，比网页快得多。

---

## 加新文档时怎么办？

每加一份新的 HTML 文档，需要做两件事：

1. **把新文档放进 `docs/` 文件夹**，文件名用英文（避免 URL 编码问题），比如 `compliance.html`
2. **在 `index.html` 里加一个入口**，复制下面这段，改成对应内容：

```html
<a class="doc" href="docs/compliance.html">
  <div class="doc-num">04</div>
  <div class="doc-body">
    <div class="doc-cat">COMPLIANCE · 合规框架</div>
    <div class="doc-title">三衡生活合规框架与高端咨询</div>
    <div class="doc-desc">法律边界 · 名称替换 · 高端咨询产品 · 价格体系 · 合同模板</div>
  </div>
  <div class="doc-arrow">→</div>
</a>
```

放在 `</section>` 之前，序号 `01 02 03` 后面接 `04`，依此类推。

---

## 以后想换成自己的域名？

如果以后买了域名（比如 `sanheng.life`），步骤：

1. 在域名服务商处加一条 CNAME 记录指向 `wjpvip-cloud.github.io`
2. 仓库 Settings → Pages → Custom domain 填上你的域名 → Save
3. 等 DNS 生效（最长 24 小时），完成

GitHub Pages 免费提供 HTTPS 证书。

---

## 常见问题

**Q：上传后 Pages 没出现网址怎么办？**
A：检查 Settings → Pages 里 Source 有没有选对 branch（main）。如果还不行，检查 Actions 标签页有没有报错。

**Q：访问网址显示 404？**
A：等 2-3 分钟，第一次部署有延迟。还不行就检查根目录有没有 `index.html`（必须叫这个名字）。

**Q：内部用，不想全网公开怎么办？**
A：免费 GitHub Pages 必须公开仓库。要私密，方案有：
   - 升级 GitHub Pro（$4/月），可以让 Pages 仅协作者访问
   - 或换用 Vercel/Netlify，免费版也支持密码保护

**Q：站点速度慢？**
A：GitHub Pages 在国内访问可能略慢。后续要面向中国用户优化，可以考虑：
   - 配置自定义域名 + Cloudflare CDN（免费）
   - 或部署到国内服务（如腾讯云静态托管）
