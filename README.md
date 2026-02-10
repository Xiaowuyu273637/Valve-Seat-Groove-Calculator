# 阀座槽计算器

## 项目简介

阀座槽计算器是一个基于Web的CNC（数控机床）加工程序生成工具，专门用于阀座槽加工计算与程序生成。该工具提供直观的图形界面，允许用户通过参数化设置自动生成相应的CNC加工程序。

## 主要功能

### 1. 图形化布局设计
- 实时显示阀座槽布局图
- 支持大圆(R1)、小圆(R2)、平行槽、C槽、Q槽等几何元素的绘制
- 自适应缩放和居中显示
- 支持深色/浅色主题切换

### 2. 参数化配置
- **主圆参数**：R1、R2的坐标和直径
- **平行槽参数**：槽间距（自动计算一半）
- **C槽参数**：直径和位置配置
- **Q槽参数**：可选Q槽的直径和偏移
- **加工参数**：切削深度、进给速度
- **坐标参数**：起点坐标、旋转中心坐标

### 3. 增量编程支持
- 支持绝对编程和增量编程模式
- 智能增量编程：后续C槽可基于前一个槽进行增量计算
- 一键切换所有C槽为增量/绝对编程

### 4. 图形旋转功能
- 支持0°、90°、180°、270°等预设旋转角度
- 支持自定义旋转角度
- 起点坐标保持固定不旋转

### 5. CNC程序生成
- 自动生成直径编程格式的CNC程序
- 支持两套程序格式（$1 和 $1+$2）
- 程序代码实时预览
- 支持程序导出为文本文件

### 6. 数据可视化
- 旋转加工数据表格显示
- 参考信息汇总
- 连接线数据和角度计算

## 技术特点

### 前端技术
- 纯HTML/CSS/JavaScript实现，无需后端依赖
- 响应式设计，支持桌面端和移动端
- Canvas 2D绘图，高性能图形渲染
- CSS Grid和Flexbox布局
- 深色模式支持（跟随系统主题）

### 交互特性
- 实时参数更新和图形重绘
- 拖拽缩放和视角调整（通过画布交互）
- 加载状态提示
- 模态框和表单验证

### 数据管理
- 参数本地存储（通过URL参数或本地存储）
- 增量编程数据模型
- 旋转计算和几何变换

## 使用说明

### 快速开始
1. 打开 `index.html` 文件或部署到Web服务器
2. 在左侧控制面板中输入或调整参数
3. 图形区域将实时更新显示布局
4. 查看底部生成的CNC程序代码
5. 点击"导出"按钮保存程序文件

### 参数配置说明
- **R1坐标**：大圆的圆心位置
- **R2坐标**：小圆的圆心位置
- **槽间距**：平行槽之间的距离
- **C槽**：圆形槽，可添加多个，支持增量编程
- **Q槽**：额外的圆形槽，可自由添加
- **起点坐标**：加工起点位置（不参与图形旋转）
- **旋转中心**：加工旋转中心点

### 编程模式
- **绝对编程**：基于R1圆的绝对位置
- **增量编程**：基于前一个槽的相对位置
- 点击"切换所有为增量编程"可批量修改模式

### 图形旋转
- 选择预设角度或自定义角度
- 点击"应用旋转"生效
- 注意：起点坐标保持固定，其他元素绕旋转中心旋转

### 程序导出
1. 选择需要导出的程序版本（第一套或第二套）
2. 点击"导出"按钮
3. 输入文件名（输入名称自带TXT格式）
4. 确认后自动下载文件

## 开发信息

### 开发者
- **主要开发者**：鱼
- **AI协作**：DeepSeek
- **开发时间**：2026年2月

### 技术栈
- 原生JavaScript（ES6+）
- HTML5 Canvas API
- CSS3（Grid、Flexbox、CSS变量）
- 响应式Web设计
- 现代浏览器API（ResizeObserver等）

### 项目特点
1. **无依赖**：不依赖任何外部库或框架
2. **离线使用**：所有功能在浏览器本地运行
3. **跨平台**：支持桌面和移动设备
4. **易部署**：单HTML文件即可运行

## 注意事项

1. **单位系统**：所有尺寸单位为毫米（mm），角度单位为度（°）
2. **坐标系**：Y轴向上为正，符合机械加工习惯
3. **程序格式**：生成的是直径编程格式的CNC程序
4. **精度**：计算精度为两位小数
5. **性能**：图形重绘时可能会有短暂加载状态

## 更新日志

### v1.0 (2026-02-10)
- 初始版本发布
- 基础参数设置和图形绘制
- CNC程序生成和导出功能
- 增量编程支持
- 图形旋转功能
- 响应式设计

## 贡献指南

欢迎提交Issue和Pull Request来改进这个项目。

## 许可证

本项目遵循MIT许可证。详细信息请查看LICENSE文件（如有）。

---


**使用提示**：在实际加工前，请务必在仿真软件中验证生成的程序，确保加工安全。
---
# Valve Seat Groove Calculator

## Project Introduction

The Valve Seat Groove Calculator is a web-based CNC (Computer Numerical Control) machining program generation tool, specifically designed for calculating and generating machining programs for valve seat grooves. The tool provides an intuitive graphical interface, allowing users to automatically generate corresponding CNC machining programs through parametric settings.

## Main Features

### 1. Graphical Layout Design
- Real-time display of the valve seat groove layout diagram
- Supports drawing of geometric elements such as large circle (R1), small circle (R2), parallel grooves, C-grooves, Q-grooves, etc.
- Adaptive zoom and center-aligned display
- Supports dark/light theme switching

### 2. Parametric Configuration
- **Main Circle Parameters**: Coordinates and diameters of R1, R2
- **Parallel Groove Parameters**: Groove spacing (automatically calculates half)
- **C-Groove Parameters**: Diameter and position configuration
- **Q-Groove Parameters**: Optional Q-groove diameter and offset
- **Machining Parameters**: Cutting depth, feed rate
- **Coordinate Parameters**: Start point coordinates, rotation center coordinates

### 3. Incremental Programming Support
- Supports absolute and incremental programming modes
- Smart incremental programming: Subsequent C-grooves can be calculated incrementally based on the previous groove
- One-click switching of all C-grooves to incremental/absolute programming

### 4. Graphic Rotation Function
- Supports preset rotation angles: 0°, 90°, 180°, 270°
- Supports custom rotation angles
- Start point coordinates remain fixed and do not rotate

### 5. CNC Program Generation
- Automatically generates CNC programs in diameter programming format
- Supports two program formats ($1 and $1+$2)
- Real-time preview of program code
- Supports exporting programs as text files

### 6. Data Visualization
- Tabular display of rotation machining data
- Summary of reference information
- Connection line data and angle calculation

## Technical Features

### Frontend Technology
- Pure HTML/CSS/JavaScript implementation, no backend dependencies
- Responsive design, supports desktop and mobile
- Canvas 2D drawing, high-performance graphics rendering
- CSS Grid and Flexbox layout
- Dark mode support (follows system theme)

### Interactive Features
- Real-time parameter updates and graphic redrawing
- Drag-to-zoom and view adjustment (via canvas interaction)
- Loading status prompts
- Modal dialogs and form validation

### Data Management
- Parameter local storage (via URL parameters or local storage)
- Incremental programming data model
- Rotation calculations and geometric transformations

## Usage Instructions

### Quick Start
1. Open the `index.html` file or deploy to a web server
2. Enter or adjust parameters in the left control panel
3. The graphic area will update in real-time to display the layout
4. View the generated CNC program code at the bottom
5. Click the "Export" button to save the program file

### Parameter Configuration Notes
- **R1 Coordinates**: Position of the large circle's center
- **R2 Coordinates**: Position of the small circle's center
- **Groove Spacing**: Distance between parallel grooves
- **C-Groove**: Circular groove, multiple can be added, supports incremental programming
- **Q-Groove**: Additional circular groove, can be freely added
- **Start Point Coordinates**: Machining start position (does not participate in graphic rotation)
- **Rotation Center**: Machining rotation center point

### Programming Modes
- **Absolute Programming**: Based on the absolute position relative to the R1 circle
- **Incremental Programming**: Based on the relative position to the previous groove
- Click "Switch All to Incremental Programming" to batch modify modes

### Graphic Rotation
- Select a preset angle or a custom angle
- Click "Apply Rotation" to take effect
- Note: Start point coordinates remain fixed, other elements rotate around the rotation center

### Program Export
1. Select the desired program version to export (first set or second set)
2. Click the "Export" button
3. Enter the filename (name input includes .TXT format by default)
4. Confirm to automatically download the file

## Development Information

### Developer
- **Main Developer**: Yu (Fish)
- **AI Collaboration**: DeepSeek
- **Development Date**: February 2026

### Technology Stack
- Native JavaScript (ES6+)
- HTML5 Canvas API
- CSS3 (Grid, Flexbox, CSS Variables)
- Responsive Web Design
- Modern Browser APIs (ResizeObserver, etc.)

### Project Highlights
1. **No Dependencies**: Does not rely on any external libraries or frameworks
2. **Offline Use**: All functions run locally in the browser
3. **Cross-Platform**: Supports desktop and mobile devices
4. **Easy Deployment**: Runs with a single HTML file

## Important Notes

1. **Unit System**: All dimensional units are millimeters (mm), angle units are degrees (°)
2. **Coordinate System**: Y-axis is positive upward, conforming to machining conventions
3. **Program Format**: Generates CNC programs in diameter programming format
4. **Precision**: Calculation precision is to two decimal places
5. **Performance**: There may be a brief loading state during graphic redrawing

## Update Log

### v1.0 (2026-02-10)
- Initial version release
- Basic parameter settings and graphic drawing
- CNC program generation and export functionality
- Incremental programming support
- Graphic rotation function
- Responsive design

## Contribution Guidelines

Issues and Pull Requests to improve this project are welcome.

## License

This project follows the MIT License. Please see the LICENSE file for details (if present).

---

**Usage Tip**: Before actual machining, always verify the generated program in simulation software to ensure machining safety.
