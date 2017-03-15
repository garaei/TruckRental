# 货车租赁系统（暂时为记录日志）

# v4.0（3.7）

**实现任务：**

* 地图功能已完成
* 地图自动定位，搜索定位，输入提示，规划路线和计算路径均已整合到项目中

**几点可以改进的方案：**

* 提示司机注册时，用AlertDialog
* 用户登录使用ProgressDialog
* 数据库CRUD使用LitePal，避免代码量大。

## v4.1 （3.14+3.15）

**实现任务：**

* 登录主界面改为手机账号登录
* 添加用户注册
* 修复工具校验类BUG
* 加入司机登录界面


# v3.0版本（2.8）

**实现任务：**

* 司机注册界面和功能已基本完成（剩下三级联动的城市List和日期转换的存储）
* 订单生成页面，即用户使用页面已初步完成

**下一步任务：**

* 订单页面功能实现
	* 包括GPS自动定位，路径选择
	* 存入数据库发生错误时的提示功能
* 抢单页面的初步开始

****
## v3.1（2.9）

**实现任务：**

* 订单生成页面逻辑简单完成（生下一对坑T^T）

## v3.2（2.10）

**实现任务:**

* 订单生成界面的错误信息展示

**下一步任务：**

* 在订单页面左上角添加一个 `我的` 按钮，用**抽屉式**的方式打开页面
	* 该页面包含：
		1. 订单记录
		2. 我的司机
	* 我的司机显示司机的姓名、电话、城市和车型  

## v3.3（2.11）

**实现任务：**

* `我的` 按钮添加完成，界面还不够优化，左侧导航栏中的内容没有实现

PS：左侧抽屉式的导航栏，这里面的坑太多了，搞了一个下午，晚上继续！

## v3.4（2.12）

**实现任务：**

* 左侧导航栏的优化（消除标题等琐碎杂事）　
* 添加导航栏菜单的点击事件
* 整理了java文件的位置，将单独的Listener类放到一起
* 整合订单页面功能，将日期规范加入进来

**未完成：**

* 导航栏菜单的真正逻辑未实现

# v2.0版本（2.2）

**实现任务：**

* 连接上SQLite数据库
* 写完用户的CRUD操作，并进行测试

**下一次目标：**

* 将剩下的两张表的CRUD操作写完
* 司机注册页面写出来并实现它的逻辑，即能放到数据库内
****

## v2.1（2.3）
**实现任务：**

* driver和order表单创建完成及它们的基础类（domain中）创建完成
* driver的数据库底层操作CURD完成

****
## v2.2（2.4）
**实现任务**

* order表的建立及CURD完成
* 修改以前建表时的几个错误（driver和order漏了一两个表项）
* 修改了一些命名不规范的地方和用法不统一的地方，如按钮必须都叫btn

**PS**：SQLite中本来没有boolean类型，但是拓展了这个类型，所以用这种类型存储进去，但是cursor取出来时却不能取出来，所以我把Boolean修改成了Integer，限制在0和1

****
## v2.3（2.5）

**实现任务：**

* 能从页面注册司机，司机的前后端交互基本完成
* 优化driverDao中update的代码，减少代码的重用性

**未完成的任务：**

* 将所有需要检验属性的放到一个Tools工具类里面，并且检验错误会提示错误码

****
## v2.4（2.6）

**实现任务：**

* 添加order表内字段order_car_type和order_start_date
* driver表中添加按货车类型查找方法，并优化以前的查找方法

****
## v2.5（2.7）

**实现任务：**

* 添加差错检验和密码加密功能，并放入单独的tools类中

****

## v1.0版本（Date：1.24）

**功能实现及未完成的部分：**
	
- 简单实现司机注册页面和主界面
- 采用了Android Studio提供的登录模板并加以修改
- 司机注册的业务逻辑检验没有写完，并且也未能存储到数据库

<p>PS：因为这几天都忙着购置年货，还打扫家里卫生，所以做的确实比较少
****

### v1.1（Date：1.29）
**实现任务：**

对货车司机注册界面进行简单优化，并添加图片

**接下一步目标：**

- 实现主界面卡片翻转效果
- 城市所在地，单独界面处理
- 与数据库连接

最后祝大家大年初二快乐！
****
### v1.2（Date：2.1）

**实现任务：**

- 连接上数据库，并对user表单进行简单的操作和测试