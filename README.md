# py-fullstack

一个最小可用的静态页面示例：HTML 结构与样式分离，不依赖任何构建工具或第三方库。

## 目录结构

```
py-fullstack/
├── index.html    # 页面结构
├── style.css     # 页面样式
└── README.md     # 项目说明
```

## 快速开始

直接用浏览器打开 `index.html` 即可预览。

如需通过本地服务器访问（推荐，便于后续接入接口或模块化脚本）：

```bash
# 任选其一
python -m http.server 8000
npx serve .
```

然后访问 <http://localhost:8000>。

## 文件说明

- **index.html** — 包含 `doctype`、`charset` 与 `viewport` 声明，通过 `<link rel="stylesheet" href="style.css" />` 引入样式，页面主体是一个居中显示的标题。
- **style.css** — 用 `:root` 定义 `--bg`、`--fg` 两个颜色变量；`body` 采用 `grid` + `place-items: center` 实现垂直水平居中；`*` 统一 `box-sizing: border-box`。

## 自定义

改主题色只需调整 `style.css` 顶部的变量：

```css
:root {
  --bg: #0d1117;
  --fg: #e6edf3;
}
```

新增页面时，复制 `index.html` 并复用同一份 `style.css` 即可保持一致的外观。

## 备注

仓库中的 `.gitignore/` 目录当前包含 `serverkey.pem`，属本地私密文件，不应提交到版本库。
