# Personal Website · V2.0

独立制作的学术与工程主页原型；视觉设计参考现代学术作品集，不直接复制他人网站源码。

## 本地运行

在本目录执行：

```bash
python3 -m http.server 8000
```

浏览器打开 `http://localhost:8000`。本压缩包没有多余的外层文件夹。

## 内容维护

编辑 `content.json`：

- `profile`：姓名、简介、GitHub、可选照片路径（如 `assets/photo.jpg`）
- `interests`：仅学术研究兴趣
- `research`：可公开的进行中研究
- `publications`：真实论文信息；没有成果时保留 `[]`
- `projects`：项目卡片，必须有唯一 `slug`
- `project_details`：按对应的 `slug` 编写项目独立详情页内容；支持多节标题和正文段落
- `experience` / `education`：经历与教育；示例 Experience 默认隐藏

主页项目卡片会链接到 `project.html?id=项目slug`。不需要修改网页代码就可以继续添加项目。内容是 JSON，不是 Markdown，第一版以可验证的低依赖实现为主；后续若需要大规模技术笔记可再引入 Markdown 构建流程。

注意：内容中的部分条目仍是标注过的示例和占位信息，公开部署前务必替换或删除。论文状态、学校、项目成果、测试指标都应以真实可验证的信息为准。

## 本次升级

- Research 移出 Linux / Embedded，区分研究兴趣、正在进行的工作与论文。
- Publications 空状态，不虚构论文。
- 项目新增独立详情页面。
- 无真实 Experience 时自动隐藏对应导航和板块。
- 调整首页背景层次、图片占位、卡片详情链接。
