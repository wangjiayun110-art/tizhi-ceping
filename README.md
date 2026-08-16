# 中医体质自测 · tizhi-ceping

基于《中医体质分类与判定》国家标准（GB/T 46939—2025）的**九种体质自测网站**，副业项目。

## 功能

- 62 题标准量表自测（题目随机顺序，避免被标签暗示而答偏）
- 标准计分算法：原始分 → 转化分（含平和质 6 道反向计分题）→ 判定
- 九种体质得分可视化 + 主体质 / 兼夹体质 / 倾向判定
- 调养建议（饮食 / 穴位 / 起居）
- 报告分享（保存长图 PNG + 复制分享文案）

## 目录结构

```
tizhi-ceping/
├── index.html              # 测试入口（62题+标准计分+报告分享）
├── constitutions/          # 九种体质详解内容页（SEO 长尾）
│   ├── index.html          # 九种体质总览 / 导航 hub
│   ├── pinghe.html         # 平和质
│   ├── qixu.html           # 气虚质
│   ├── yangxu.html         # 阳虚质
│   ├── yinxu.html          # 阴虚质
│   ├── tanshi.html         # 痰湿质
│   ├── shire.html          # 湿热质
│   ├── xueyu.html          # 血瘀质
│   ├── qiyu.html           # 气郁质
│   └── tebing.html         # 特禀质
├── sitemap.xml             # 搜索引擎抓取索引
├── README.md
└── .gitignore
```

## 技术

纯前端静态站，**零依赖、可离线运行**。直接双击 `index.html` 即可使用，或静态托管上线。
内容页由 `build_site.py`（上级目录）统一生成，修改体质文案后重跑即可。

## 部署

- 静态托管即可：Vercel / Netlify / Cloudflare Pages / GitHub Pages / CloudStudio
- 无需服务器、无需数据库、无需后端
- sitemap.xml 上线后把里面的 `https://tizhi.example.com` 替换为正式域名

## 合规

结果仅供参考，**不构成医疗诊断**。体质调理请咨询专业中医师。页面已内置显著免责声明。

## 路线图

- [x] 测试内核（62 题 + 标准计分）
- [x] 报告页（得分图 + 分享）
- [x] 9 种体质完整内容页 + sitemap + 内链
- [ ] 变现层（广告 / 带货 / 会员）
- [ ] 27 题短版适配新国标

## 本地预览

直接用浏览器打开 `index.html` 即可；内容页在 `constitutions/` 目录下。
