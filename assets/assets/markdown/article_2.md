# Flutter_Demo

本项目利用 https://jsonplaceholder.typicode.com/ 接口模拟社区项目交互，演示 Flutter 工程大致架构。



## 工程结构

root

- android
- ios
- lib
  - config  常量定义、环境参数、路由配置等
  - data
    - repository  Repository 实现类
    - source  数据源（如网络、数据库）
  - domain
    - entity  实体类
    - repository  Repository 抽象类
  - extension  Dart 扩展
  - l10n
    - arb  多语言文件
  - presentation  表现层
    - xxx 模块
      - bloc
      - view  页面类
      - widget  控件类
  - utils  工具类
- plugin  本地插件
- l10n.yaml  国际化配置



## 项目框架

屏幕适配：flutter_screenutil

路由：go_router

状态管理：flutter_bloc

国际化：intl

网络：dio

Toast：oktoast

Loading：flutter_easyloading



## 应用入口

位于 lib/presentation/app/view/app_screen.dart 中的 AppScreen 类



- MultiBlocProvider（注入各种 Repository）
  - OKToast
    - ScreenUtilInit
      - MaterialApp
        - FlutterEasyLoading



## 表现层模块

- app（应用入口）
- home（首页）
- login（登录页）
- post（首页 - 动态 Tab）
- post_detail（动态详情页）
- sample（首页 - 示例 Tab）
- search（首页顶部 - 搜索页）
- setting（设置页）
- user（首页 - 用户 Tab、用户页）
- user_album（用户页 - 相册 Tab）
- user_post（用户页 - 动态 Tab）
- welcome（欢迎页）
