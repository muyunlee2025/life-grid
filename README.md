# ⏳ Life Grid (人生进度条)

> "种一棵树最好的时间是十年前，其次是现在。"

## 📖 简介 (Introduction)
Life Grid 是一个极简主义的人生可视化工具。灵感来源于 "Your Life in Weeks"。
作为一个程序员爸爸，我希望用这种直观的方式，记录儿子 Louie 的成长，以及提醒自己珍惜当下。

🌐 **Live Demo:** [https://muyunlee2025.github.io/life-grid/]

## ✨ 特性 (Features)
- **极简视觉：** 纯 CSS 实现的 4000+ 周格子，移动端极致适配（无光标、无误触）。
- **云端同步：** 基于 Supabase Auth (Magic Link) 实现数据多端漫游。
- **分享海报：** 一键生成精美的人生进度分享卡片 (html2canvas)。
- **隐私优先：** 数据仅存储于 Supabase，无第三方追踪。

## 🛠️ 技术栈 (Tech Stack)
本项目坚持 **"Less is More"** 的独立开发原则：
- **Frontend:** Vanilla JS (原生 JavaScript), HTML5, CSS3 (No Frameworks)
- **Backend:** Supabase (PostgreSQL, Auth, RLS)
- **Tools:** html2canvas
- **Deploy:** Vercel / Netlify

## 🚀 快速开始 (Setup)

1. 克隆仓库:
   ```bash
   git clone [https://github.com/muyunlee2025/life-grid.git](https://github.com/muyunlee2025/life-grid.git)

```

2. 替换 `index.html` 中的 Supabase 配置 (URL & Key)。
3. 在 Supabase 后台创建表结构:
```sql
create table test_milestones (
  user_id uuid references auth.users not null,
  week_index int not null,
  content text,
  primary key (user_id, week_index)
);

```


4. 启动本地服务器 (Live Server) 即可。

## 👨‍💻 作者 (Author)

**牧云 (Muyun)**

* Indie Dev & Dad.
* Follow my journey: [x（twitter）: https://x.com/muyun_dev] (公众号名称：牧云和Louie一起长大)

## 📝 License

MIT
