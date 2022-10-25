# 龍脈•另一種姿態R Mod
* 修改战斗相关功能
* 建议设置100毫秒延迟
* 只能真实机器，模拟器需要框架本身的frida支持了才行

## 基础功能
* 编组可以上同名角色（除支援）
* 战斗必定3星，输了会变成胜利

## 可选功能
* 战斗开场不动直接胜利，在主界面点击“签到奖励查看”按钮开关
* 进了战斗想开可以连点4下“暂停”按钮

## 免root相关
### 黑盒方法：
#### 首次执行：
* 安装JsHook
* 安装黑盒，一般来说安装BlackBox64 https://github.com/FBlackBox/BlackBox/releases
* 打开BlackBox64 -> 右上角三点 -> 软件设置 启动Xposed框架 -> 模块管理 -> 勾选JsHook -> 关闭BlackBox64
* 打开BlackBox64 -> 点+ -> 龍脈R 和 “兔子头” -> “兔子头”登录，点击OPEN -> 进入游戏主界面后关闭
* 打开BlackBox64 -> 打开JsHook -> 框架管理 -> 安装FridaMod
* 打开BlackBox64 -> 打开JsHook -> 仓库 -> 下载脚本
* 打开BlackBox64 -> 打开JsHook -> 应用 -> 龍脈R -> 启动Hook服务 -> 启动配置(脚本配置) -> 延时设置100 -> 选择注入框架“FridaMod” -> 启动下载的脚本 -> 运行游戏
* 之后应该在外部更新游戏就行了？

### 普通方法：
#### 首次执行：
* 安装JsHook
* 打开JsHook -> 应用 -> 龍脈R -> 注入Hook服务 -> 卸载再安装（安装好后不要启动，启动了可以进应用设置里清除全部数据） -> 打开“兔子头”登录，点击OPEN
#### 游戏更新后：
* 下载游戏最新安装包，不要用兔子头更新，官方最新安装包地址 https://habxbit.com/download/launcher/AnotherEidos.apk
* 打开JsHook -> 安装包注入Hook服务 -> 选择下载的安装包 -> 安装 -> 启动
  
## 预览
![image](https://i.imgur.com/yc49Hcz.jpg)
