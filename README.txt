Xu Lab 官网 · 全新上线包（2026-11-11 更新）
================================================

这一套是「打开就能看」的纯网页：所有文字直接写在 HTML 里，
没有模板、没有数据文件、没有隐藏文件、不需要 Jekyll 构建。

【先验收内容】
  双击 index.html，用浏览器看四个页面：
    index.html          首页（研究方向 / News 动态 / Join Us）
    people.html         成员（PI 履历 + Lab Alumni 毕业生板块）
    publications.html   论文 38 篇，按年份分组，每条带 DOI 链接，页内有年份跳转
    contact.html        联系方式
  content-checklist.txt 用记事本打开，可逐条核对 38 篇论文。

【本包包含的文件】
  index.html / people.html / publications.html / contact.html / 404.html
  assets/css/style.css        全站样式（只此一个文件）
  sitemap.xml / robots.txt    搜索引擎收录用
  content-checklist.txt       内容核对清单（PI 自查用）

【邮箱防爬虫说明】
  全站邮箱一律显示为 xuchliang (at) mail.sysu.edu.cn，页面上没有可直接
  被机器抓取的完整邮箱。访客发信时把 (at) 换成 @ 即可，这是国际学界
  通行的防垃圾邮件做法。

【上传到 GitHub（首次启用，详见交接包 10.11）】
  推荐：本文件夹已是 git 仓库并关联了远程仓库，用父目录的「部署网站.bat」
  一键推送（首次需修正仓库名为连字符版 + 输入一次 Personal Access Token）。
  手动方式（备选）：
  1. 解压本压缩包，得到上面这些文件（根目录直接就是网页，没有外层文件夹）。
  2. 在仓库页点 Add file -> Upload files。
  3. 把解压出的【全部文件】拖进上传框；不要拖文件夹外壳。
  4. Commit message 填 Fresh launch，选 Commit directly to the main branch。
  5. 仓库 Settings -> Pages -> Source 选 Deploy from a branch，
     Branch 选 main / (root)，Save。
  6. 等 1-2 分钟，访问 https://xulab-plasmacell.github.io

【这套包刻意去掉了什么】
  - 没有 _config.yml、_data/、_layouts/（旧版 Jekyll 遗留，会干扰构建）
  - 没有 .pages.yml、.gitignore 等点文件（以前最容易漏传）
  - 没有需要「覆盖 / 替换」判断的同名旧文件
  所以 uploads 一次就是干净的一套，不会新旧混杂。

【以后改内容：三种方式，按你的情况选】
  详细图文步骤见《WorkBuddy桌面版_接手交接包.md》第 10 节，这里是要点：

  方式一：自己动手（适合改一句话、错别字）
    1. 打开仓库 github.com/xulab-plasmacell/xulab-plasmacell.github.io
    2. 点开要改的文件（改论文 publications.html、改动态 index.html、
       改成员 people.html）→ 点右上角铅笔图标
    3. Ctrl+F 找到那句话，只改文字；<li> <h2> class="..." 这类符号原样不动
    4. 底部 Commit message 写一句说明 -> Commit changes
    5. 等 1-2 分钟，Ctrl+Shift+R 强刷验收
    改坏了不怕：Commits 里点旧提交 ... -> Revert 一键还原。

  方式二：发给管理员/AI 代改（推荐：加论文、加成员、改多处）
    1. 把新资料发给 AI（如：论文标题、作者、期刊、年份、DOI）
    2. AI 返回改好的单个文件（例如 publications.html）
    3. 仓库里点开同名文件 -> 铅笔图标 -> Ctrl+A 全选删除 -> 粘贴新内容
       -> Commit changes
    4. 强刷验收
    优点：编号、年份计数、总篇数这些易错点由 AI 一次算对。

  方式三：升级可视化后台（后期可选，无需碰文件）
    如果以后学生也要参与维护、希望像填表格一样改内容，可以迁移到
    「数据文件 + 可视化 CMS」版本（如 Pages CMS）：内容存成表格文件，
    编辑者在网页表单里填内容、点保存即自动发布，完全不用接触 HTML。
    迁移需一次性改造（半天内完成），启用前需要 PI 本人在 GitHub 授权。
    是否迁移、何时迁移，等站点稳定运行后再决定即可。

内容与 2026-11-11 核实的公开资料一致（Crossref / PubMed / 中山大学官方主页）。
正式对外宣传前请 PI 核对成员名单与全部论文清单。
