# Crysadm+ 云端监控
=============
![image](https://github.com/hauntek/crysadm/raw/master/static/img/preview.png)

最新更新：2017-08-30
在线预览：http://www.crysadmapp.cn/guest

# 运行环境
建议 Python 3.4.2 及 Redis 2.8 以上

# 项目配置
=============
1.安装项目依赖扩展
- 终端执行命令 `pip install redis, requests, flask`

2.配置项目启动参数
- 使用支持UTF-8格式编辑器编辑config.py 配置 redis server

crysadm.py 启动web服务
- 默认启动为单线程模式，如多并发请使用多线程模式启动
- 多线程模式启动命令: `./crysadm.py runserver --threaded`

crysadm_helper.py 启动后台服务

4.启动web服务后访问 /install 生成管理员账号

## Update 2017-08-30
=============

1.调整用户注册为数字+英文用户名，不可包含特殊符号

2.优化用户修改密码判断流程，减少不必要的查询

3.修复切换统计产量显示跳转其他标签问题

## Update 2017-03-31
=============

1.优化手机端网页排版显示，支持首页方块双排

2.修复部分矿机设备详情页面出错问题

## Update 2017-03-29
=============

1.优化后端提现状态检测，提升自动提现任务效率

2.支持前端页面同比产量，产量/速度双重显示

3.整合前端页面我的矿机，全部账号操作按钮

4.重写显示迅雷统计收益函数，支持速度条控制

5.重写显示控制面板今日收益、图表速度、速度详情函数

6.为了让后端离线用户数据统计更准确，调整如下
- 每90秒刷新一次离线用户数据

7.调整运行日记页面，每页最多可显示50条记录

8.以及大幅优化整体部分代码细节，提升稳定性

## Update 2017-03-25
=============

1.优化秘银进攻/免费宝箱接口，顺便参数合并

2.补上后端自动秘银复仇任务，复仇接口与进攻合并

3.优化后端免费宝箱逻辑，取消一次性全部循环

4.优化后端摇晃宝箱逻辑，取消一次性全部循环

5.优化后端幸运转盘逻辑，优先判断秘银数量

6.调整后端执行线程间隔时间，调整如下
- 每180分钟检测一次秘银进攻
- 每240分钟检测一次秘银复仇
- 每300分钟检测一次幸运转盘

7.预留迅雷游乐场接口函数，以后替代原秘银进攻接口

8.更换新日记记录模式，自动清除超出7天后的记录

9.更换新日记记录模式，有效降低redis占用内存/储存空间

## Update 2017-03-24
=============

1.优化后端自动日记记录重组函数

2.优化后端多进程等待上个进程，降低没必要的负载

## Update 2017-03-23
=============

1.修复线上/线下更新，部分下载到启动命令路径

2.调整控制终端页面，编辑内容为查询用户详情

## Update 2017-03-22
=============

1.修复新矿机速度统计，计算平均值不准确

## Update 2017-03-21
=============

1.添加后端自动摇晃宝箱任务

2.添加前端摇晃宝箱开关

3.支持特殊节日假期提现操作

4.修复自动任务开关不执行问题

5.优化新矿机速度统计，计算平均值

6.重写后端数据刷新脚本，提升稳定性

7.线下更新判断配置文件存在，则忽略配置文件

## Update 2017-02-28
=============

1.添加终端程序，无限制平台

2.增加 控制终端页面
- 页面及按钮权限仅管理员可见，实时反馈结果

3.取消禁用权限检查

4.调整session过期时间

5.支持线上更新后立即生效

## Update 2017-02-22
=============

1.修复项目检查文件不存在出错问题

## Update 2017-02-12
=============

1.优化项目更新脚本

2.优化项目下载性能

3.优化文件校验逻辑

## Update 2017-02-11
=============

1.优化项目更新脚本

2.优化前端更新流程

3.优化文件对比逻辑

4.修复更新导致系统根目录文件夹创建

5.修复检查更新缓存不删除问题

## Update 2017-02-10
=============

1.添加更新程序，无限制平台

2.增加 检查及更新（在关于-更新历史）
- 按钮权限仅管理员可见，更新后默认会备份原有的

3.前端增加update文件监控

4.优化升级交互，添加实时反馈更新进度

5.修复开启备份后不更新问题

## Update 2017-02-09
=============

1.修正后端速度循环统计

## Update 2017-02-08
=============

1.添加 清除历史数据（在账号管理-我的个人信息）
- 删除全部监控历史记录数据 例如：历史速度，历史产量等 如果显示不出迅雷收益柱可以用这个方法解决

2.更新RSA加密函数，优化加密性能

## Update 2017-01-29
=============

1.模板主题标题，右侧添加用户交流、加入群组按钮

2.调整关于页面排版问题

3.前端网站静态资源库(static)，更新INSPINIA 2.7底版

4.更换继承简洁模板(横向菜单)，依照INSPINIA 2.7模板调整

5.右上角添加当前动态时间

6.以及部分界面样式优化
