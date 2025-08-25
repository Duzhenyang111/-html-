# Excel 数据标注工具

一个基于浏览器的轻量级工具，用于标注Excel文件中两列文本数据的相关性。支持键盘快捷键操作，提高标注效率。

![示例界面](https://img.shields.io/badge/界面-友好-brightgreen) ![无需后端](https://img.shields.io/badge/架构-纯前端-blue) ![开源](https://img.shields.io/badge/许可证-MIT-green)

## 功能特点

- 📊 直接读取Excel文件（.xlsx, .xls）
- ⌨️ 支持键盘快捷键操作（左右箭头键）
- 📈 实时进度显示与进度条
- 💾 随时导出标注结果
- 🎨 简洁直观的用户界面
- 🌐 纯前端实现，无需服务器

## 使用说明

### 基本流程

1. 上传包含两列文本数据的Excel文件
2. 系统逐行显示文本内容
3. 判断两句话是否相关：
   - 点击"相关"按钮 或 按键盘 **左箭头键** (←)
   - 点击"不相关"按钮 或 按键盘 **右箭头键** (→)
4. 随时导出当前标注结果

### Excel文件格式要求

Excel文件应包含至少两列文本数据，第一行可以是标题行（会自动识别）。

示例格式：

| 句子A | 句子B |
|-------|-------|
| 这是一段文本 | 这是另一段文本 |
| 今天天气很好 | 我喜欢吃苹果 |

### 标注结果

工具会在原始Excel文件中添加第三列"标签"，标注结果为：
- `1` 表示相关
- `0` 表示不相关

## 在线使用

直接访问 [GitHub Pages 页面](https://[你的用户名].github.io/excel-data-annotation-tool/) 即可使用。

或下载HTML文件后在浏览器中打开。

## 本地开发

```bash
# 克隆仓库
git clone https://github.com/[你的用户名]/excel-data-annotation-tool.git

# 进入目录
cd excel-data-annotation-tool

# 无需安装依赖，直接打开index.html即可使用
```

## 项目结构

```
excel-data-annotation-tool/
├── index.html          # 主页面
├── README.md           # 说明文档
├── LICENSE             # 开源许可证
└── assets/
    ├── screenshot.png  # 项目截图
    └── demo.xlsx       # 示例数据文件
```

## 技术栈

- 原生JavaScript
- [SheetJS/xlsx](https://github.com/SheetJS/sheetjs) - Excel文件处理库
- 纯CSS样式，无额外框架

## 常见问题

### 支持哪些Excel格式？
支持.xlsx和.xls格式的文件。

### 数据会上传到服务器吗？
不会。所有处理都在浏览器本地完成，保障数据安全。

### 最多支持多少行数据？
取决于浏览器性能，通常可处理数万行数据。

### 可以中途保存进度吗？
可以随时导出当前标注结果，下次可继续从上次停止的地方开始。

## 贡献

欢迎提交Issue和Pull Request来改进这个工具。

## 许可证

本项目采用 MIT 许可证 - 详见 [LICENSE](LICENSE) 文件。
