# 龍脈•另一種姿態R Mod
* 修改战斗相关功能
* rhino不能设置延迟，frida建议设置100毫秒延迟
* 模拟器使用rhino，实机rhino和frida都行

## 基础功能
* 编组可以上同名角色（除支援）
* 战斗必定3星，输了会变成胜利
* 插画4无需道具解锁（不用担心错过活动了）

## 可选功能
* 战斗开场不动直接胜利，在主界面点击`签到奖励查看`按钮开关
* 进了战斗想开可以连点4下`暂停`按钮

## 模拟器相关
* 拿`雷电9`举例，其他模拟器自己尝试
1. 先装好游戏能进入了，模拟器开好`ROOT`，设置`System.vmdk 可写入`
2. 装`Magisk Delta`的`Canary`版 https://huskydg.github.io/magisk-files/
3. 进入`Magisk Delta` -> 给`ROOT权限` -> 安装`Magisk` -> 方式选择`安装到系统分区` -> 重启模拟器 -> `Magisk Delta`设置打开`Zygisk`
4. 安装`JsHook` -> 安装`Magisk模块` -> 选择下载`LsposedMod-v1.0.12-1012-zygisk-release.zip` -> 到`Magisk Delta`的`模块`里`从本地安装` -> 选择安装下载的文件，重启模拟器
5. `JsHook` -> 仓库 -> 下载脚本
6. `JsHook` -> 应用 -> 龍脈R -> 启动Hook服务 -> 启动配置（脚本配置） -> 启动下载的脚本
7. 运行游戏，没有显示任何内容的话，自己随便编个js`common.toast('...')`看能不能显示，能显示再切回之前的脚本

## 免root相关
### 黑盒方法：
#### 首次执行：
1. 安装`JsHook`
2. 安装黑盒，一般来说安装`BlackBox64` https://github.com/FBlackBox/BlackBox/releases
3. 打开`BlackBox64` -> 右上角三点 -> 软件设置 -> **开启进程守护（防止闪退）** -> 启动Xposed框架 -> 模块管理 -> 勾选`JsHook` -> 关闭`BlackBox64`
4. 打开`BlackBox64` -> 点+ -> 龍脈R 和 “兔子头” -> “兔子头”登录，点击OPEN -> 进入游戏主界面后关闭
5. 打开`BlackBox64` -> 打开`JsHook` -> 框架管理 -> 安装`FridaMod`
6. `JsHook`回首页 -> 仓库 -> 下载脚本
7. `JsHook`回首页 -> 应用 -> 龍脈R -> 启动Hook服务 -> 启动配置（脚本配置） -> 延时设置100 -> 选择注入框架`FridaMod` -> 启动下载的脚本
8. 重启`BlackBox64` -> 运行游戏
#### 游戏更新后：
* 外部更新游戏就行了，黑盒内部直接链接外部的应用的

### 普通方法：
#### 首次执行：
* 安装`JsHook`
* 打开`JsHook` -> 应用 -> 龍脈R -> 注入Hook服务 -> 卸载再安装（安装好后不要启动，启动了可以进应用设置里清除全部数据） -> 打开“兔子头”登录，点击OPEN
#### 游戏更新后：
* 下载游戏最新安装包，不要用兔子头更新
* 官方最新安装包地址 https://habxbit.com/download/launcher/AnotherEidos.apk
* 打开`JsHook` -> 安装包注入Hook服务 -> 选择下载的安装包 -> 安装 -> 启动
  
## 预览
![image](https://i.imgur.com/yc49Hcz.jpg)
