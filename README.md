# 包山包海 - 酒店管理系统

一个基于 Flutter 开发的跨平台酒店管理系统，提供完整的酒店运营管理功能。

## 项目简介

包山包海是一个现代化的酒店管理后台系统，支持多平台部署（Web、iOS、Android、macOS、Windows、Linux），为酒店运营者提供实时数据监控、订单管理、房源管理等核心功能。

## 功能特性

### 已实现功能

- **数据统计面板**
  - 今日访问量统计
  - 待处理订单数量
  - 视频管理统计
  - 本周分润展示

- **业务指标监控**
  - 今日营业额及涨跌趋势
  - 总佣金统计
  - 分享人数统计
  - 店铺访问量分析

- **快捷操作中心**
  - 新增房源
  - 视频管理
  - 订单处理
  - 结算管理
  - 消息中心
  - 酒店信息管理

- **数据可视化**
  - 店铺访问趋势图
  - 月度对比分析

### 计划功能

- [ ] 用户登录/注册
- [ ] 房源详细管理
- [ ] 订单详情页面
- [ ] 财务报表
- [ ] 客户管理
- [ ] 员工管理

## 技术栈

- **框架**: Flutter 3.38.9
- **语言**: Dart 3.10.8
- **UI**: Material Design 3
- **状态管理**: StatelessWidget / StatefulWidget
- **图表**: CustomPainter 自定义绘制

## 环境要求

- Flutter SDK: 3.38.9 或更高版本
- Dart SDK: 3.10.8 或更高版本
- 开发工具:
  - VS Code / Android Studio / IntelliJ IDEA
  - Chrome 浏览器（用于 Web 调试）
  - Xcode（用于 iOS/macOS 开发）
  - Android SDK（用于 Android 开发）

## 安装步骤

### 1. 克隆项目

```bash
git clone https://github.com/pikecode/hotel_project.git
cd hotel_project
```

### 2. 安装 Flutter（如果尚未安装）

**macOS/Linux:**
```bash
git clone https://github.com/flutter/flutter.git -b stable ~/flutter
export PATH="$PATH:$HOME/flutter/bin"
```

**中国大陆用户推荐使用镜像:**
```bash
git clone https://gitee.com/mirrors/Flutter.git -b stable ~/flutter --depth 1
export PATH="$PATH:$HOME/flutter/bin"
export PUB_HOSTED_URL=https://pub.flutter-io.cn
export FLUTTER_STORAGE_BASE_URL=https://storage.flutter-io.cn
```

### 3. 配置环境变量（永久生效）

将以下内容添加到 `~/.zshrc` 或 `~/.bash_profile`:

```bash
export PATH="$PATH:$HOME/flutter/bin"
export PUB_HOSTED_URL=https://pub.flutter-io.cn
export FLUTTER_STORAGE_BASE_URL=https://storage.flutter-io.cn
```

然后执行:
```bash
source ~/.zshrc  # 或 source ~/.bash_profile
```

### 4. 检查环境

```bash
flutter doctor
```

### 5. 安装依赖

```bash
flutter pub get
```

## 运行项目

### Web 平台（推荐用于快速预览）

```bash
flutter run -d chrome
```

### macOS 桌面

```bash
flutter run -d macos
```

### iOS 模拟器

```bash
# 先启动模拟器
open -a Simulator
# 运行项目
flutter run -d ios
```

### Android 模拟器

```bash
# 确保 Android 模拟器已启动
flutter run -d android
```

### 查看可用设备

```bash
flutter devices
```

## 项目结构

```
hotel_project/
├── lib/
│   └── main.dart                 # 应用主入口，包含首页实现
├── android/                      # Android 平台配置
├── ios/                          # iOS 平台配置
├── web/                          # Web 平台配置
├── macos/                        # macOS 平台配置
├── linux/                        # Linux 平台配置
├── windows/                      # Windows 平台配置
├── test/                         # 测试文件
├── pubspec.yaml                  # 项目依赖配置
└── README.md                     # 项目说明文档
```

## 开发指南

### 热重载

在应用运行时，修改代码后按 `r` 键可以热重载：

```bash
r - 热重载（保留应用状态）
R - 热重启（清除应用状态）
```

### 代码规范

- 遵循 Flutter 官方代码风格
- 使用 `flutter analyze` 检查代码质量
- 使用 `flutter format` 格式化代码

### 构建发布版本

**Web:**
```bash
flutter build web
```

**Android APK:**
```bash
flutter build apk
```

**iOS:**
```bash
flutter build ios
```

**macOS:**
```bash
flutter build macos
```

## 调试工具

应用运行时可以访问 Flutter DevTools 进行调试：

1. 运行应用后，终端会显示 DevTools URL
2. 在浏览器中打开该 URL
3. 可以查看性能、内存、网络等信息

## 常见问题

### Q: 运行时出现网络错误？

A: 如果在中国大陆，请确保配置了镜像源：
```bash
export PUB_HOSTED_URL=https://pub.flutter-io.cn
export FLUTTER_STORAGE_BASE_URL=https://storage.flutter-io.cn
```

### Q: 如何清理构建缓存？

A: 执行以下命令：
```bash
flutter clean
flutter pub get
```

### Q: Web 版本运行缓慢？

A: 在开发模式下 Web 版本性能较低是正常的，使用 `flutter build web` 构建发布版本后性能会显著提升。

## 贡献指南

欢迎提交 Issue 和 Pull Request！

1. Fork 本仓库
2. 创建特性分支 (`git checkout -b feature/AmazingFeature`)
3. 提交更改 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 开启 Pull Request

## 许可证

本项目采用 MIT 许可证。详见 [LICENSE](LICENSE) 文件。

## 联系方式

- 项目地址: https://github.com/pikecode/hotel_project
- 问题反馈: https://github.com/pikecode/hotel_project/issues

## 更新日志

### v0.1.0 (2026-02-13)

- ✨ 初始版本发布
- ✨ 实现首页数据统计面板
- ✨ 实现业务指标监控
- ✨ 实现快捷操作中心
- ✨ 实现访问趋势图表
- ✨ 支持多平台部署

---

使用 ❤️ 和 Flutter 构建
