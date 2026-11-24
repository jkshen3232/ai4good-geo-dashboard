# AI4GOOD GEO 调查报告

公开预览：[htmlpreview 链接](https://htmlpreview.github.io/?https://github.com/jkshen3232/ai4good-geo-dashboard/blob/main/index.html)

启用 GitHub Pages（Settings → Pages → Deploy from branch `main` / `(root)`）后，地址为 https://jkshen3232.github.io/ai4good-geo-dashboard/ 。

## 文件

- `index.html` — 报告正文、热力图、指标切换、每周趋势、Prompt 库。
- `prompts.json` — 已发布的测试 prompt 集（含 `version`、`updated_at`、`changelog`）。每周复测以该文件为最新题库，默认跑其中 `core` 为 true 的条目（见 `core_prompt_ids`）。

## 如何把页面上的编辑变成已发布版本

1. 在「Prompt 库」中新增、修改、删除、调整顺序或打标签。这些修改只保存在当前浏览器的 localStorage，不会自动写入仓库。
2. 点击「导出 JSON」，下载当前题库。
3. 用导出的文件替换本仓库的 `prompts.json` 并提交到 `main`。提交后即成为已发布版本；之后打开页面会加载新文件（若浏览器里还留着旧的本地修改，可用「恢复为已发布版本」清掉）。每周复测请使用仓库里最新的 `prompts.json`。

也可以跳过页面编辑，直接在仓库里改 `prompts.json` 后提交。

`index.html` 内嵌了一份已发布副本。htmlpreview 只渲染这一个 HTML 文件，读不到旁边的 `prompts.json`，因此会自动退回内嵌副本，预览链接仍可用。用 GitHub Pages 或直接打开站点时，页面会优先读取仓库中的 `prompts.json`。

## 注意

- 本仓库是公开的，任何人拿到链接都能看到全部 prompt 原文和报告内容。
- 页面已设置 `noindex`，但仓库里的代码和数据仍可在 GitHub 上被搜到。
