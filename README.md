# 桌面日历 (DeskTodo)

![Platform](https://img.shields.io/badge/platform-Windows-7d9979?style=flat-square)
![Electron](https://img.shields.io/badge/built%20with-Electron-7d9979?style=flat-square)
![License](https://img.shields.io/badge/license-MIT-7d9979?style=flat-square)

会提醒、会规划、会写周报的 Windows 桌面效率助手。

它把待办清单、日历排程、四象限、倒计时纪念日、系统提醒和 AI 助手放在同一个桌面窗口里，适合学生、上班族、项目管理和日常计划。

适合想找"好用的桌面日历""Windows 桌面日历提醒软件""电脑桌面日程管理工具"或"开源 Electron 桌面小组件项目"的用户:免费、开源、本地保存数据,也适合拿来学习 Electron 桌面应用开发。

## 下载

Windows 用户可以直接下载运行版(从 Releases 下载对应版本压缩包),解压后双击 `桌面日历.exe` 运行,不需要安装 Node.js。

## 核心亮点

- **桌面常驻**:透明无边框窗口,支持置顶、托盘、靠边自动隐藏。
- **待办清单**:多清单管理、状态筛选、快速添加、完成、删除、恢复。
- **日历排程**:月视图、周视图、日视图,支持农历、节气、节假日和调休标记。
- **时间提醒**:支持日期、时间、全天、重复事项和系统通知。
- **四象限管理**:按重要和紧急组织任务,适合每日优先级规划。
- **倒计时纪念日**:支持公历、农历和每年重复。
- **AI 助手**:可配置 DeepSeek API Key,用于对话、写待办、生成周报。
- **本地数据**:数据保存在本机,支持自定义数据目录和备份导入导出。

## 本地开发

```bash
npm install
npm run dev      # 开发态启动(已开启热重载:app/ 下文件改动自动刷新)
npm start        # 普通启动
```

Windows 用户也可以双击 `start.bat` 启动开发版(首次会自动安装依赖)。

### 热重载说明

启动 `npm run dev` 后:

- `app/` 下任何文件(`index.html`、`style.css`、`app.js`、`lunar.js`、`holidays.js`、`almanac.js`)被修改后,窗口会在约 120ms 后自动刷新页面,无需重启。
- `main.js` 或 `preload.js` 改动会自动重启整个应用。
- 通过设置环境变量 `DESK_TODO_HOTRELOAD=0` 可临时关闭热重载。
- 打包后的应用(`app.isPackaged === true`)中自动关闭热重载。

## 数据与隐私

应用数据默认保存在本机用户数据目录,可在设置中更改保存位置。AI 功能需要用户自行配置 DeepSeek API Key;未配置时,日历、待办、提醒、倒计时等核心功能仍可正常使用。