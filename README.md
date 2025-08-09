# Guide Audio du Louvre

语音讲解卢浮宫重要藏品｜Explorez les Trésors du Louvre, Écoutez les Secrets de l'Art

> 一个极简的静态网页，组织并呈现卢浮宫重点藏品的语音讲解。配合页面内的作品清单与音频目录，您可以在浏览器中直接播放讲解音频。
> 体验地址：https://mizukisheena.github.io/Guide-Audio-du-Louvre/

## 功能概述
- 浏览器直接播放音频文件（无需后端）
- 目录式组织：按城市/博物馆/藏品分层管理音频
- 纯静态 HTML，支持 GitHub Pages 等静态托管

## 目录结构
```
Guide-Audio-du-Louvre/
├─ index.html                      # 主页（入口）
└─ Paris/卢浮宫/卢浮宫藏品/audio/      # 音频目录（可放置 .mp3/.wav 等）
```

- 您可以在 `Paris/卢浮宫/卢浮宫藏品/audio/` 目录中添加音频文件，例如：
  - `01-胜利女神.mp3`
  - `02-蒙娜丽莎.mp3`
  - `03-米洛的维纳斯.mp3`
- 建议文件名包含序号与作品名，便于排序与识别。

## 本地预览
1. 直接用浏览器打开仓库根目录下的 `index.html`
2. 确保音频文件已放到上述 `audio/` 目录中

> 提示：如果浏览器的本地文件安全策略限制了音频加载，可改用任意本地服务器（如 VS Code Live Server、`python -m http.server` 等）在项目根目录下启动后再访问 `index.html`。

## 部署到 GitHub Pages（可选）
1. 在仓库设置（Settings → Pages）中，将 Source 设为 `Deploy from a branch`，并选择 `master` 分支与根目录
2. 保存后等待几分钟，GitHub Pages 会生成一个访问链接
3. 若有自定义域名，将 DNS CNAME 指向 Pages 提供的域名即可

## 如何添加/更新音频
- 将新的音频文件放入 `Paris/卢浮宫/卢浮宫藏品/audio/`
- 在 `index.html` 中添加相应的列表项与播放控件（若页面已自动遍历目录则可省略）
- 提交并推送后，静态托管站点会自动提供这些音频

## 建议命名规范
- 文件名：`序号-作品名.扩展名`，示例：`01-蒙娜丽莎.mp3`
- 文本编码：UTF-8（仓库内路径已包含中文，推荐使用 UTF-8 以避免乱码）

## 贡献
欢迎提交 PR：
- 新增/优化音频清单与元数据
- 改进 `index.html` 的样式与播放器交互
- 提供更丰富的语言版本与文案修订

## 许可
当前未明确开源许可。若需二次开发或公开传播，请先在 Issue 中讨论或添加合适的许可证（如 MIT）。

---

如需参考、反馈或讨论，请在本仓库提交 Issue。
