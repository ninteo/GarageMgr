GarageMgr
=========

毕业设计

实现功能
=======

1.汽车进库，车主数据录入(worked)

2.车主数据存储(worked)

3.计费(worked)

4.短信提醒(worked)

5.汽车出库，车主数据删除(worked)

6.电脑和客户端互相控制(worked)

7.Google Card UI(finished)

实现方法
=======

1.车主输入个人信息，记录车主姓名，车牌号，手机号，同时调用系统函数记录入库时间

2.车主数据持久化采用SQLite数据库，生成表中包含字段：姓名，车牌号，手机号，入库时间。以车牌号为主键

3.当汽车出库时调用系统当前时间与数据库中的进库时间作对比，计算出停车费用

4.当数据库每次增加一个用户时，建立一个与之对应的线程，其中包含一个2个小时延时的定时器，定时器结束后自动给车主发送短信通知

5.汽车出库，输入出库汽车车牌号，删除数据库中相应信息

6.电脑客户端使用c#+winform平台，和手机客户端起一组成B/S结构，采用socket通信，实现电脑手机客户端数据
同步，详见/WindowsFormsApplication2 repo

License
-----

	Copyright 2014 Huang Ning Tao

	Licensed under the Apache License, Version 2.0 (the "License");
	you may not use this file except in compliance with the License.
	You may obtain a copy of the License at

	http://www.apache.org/licenses/LICENSE-2.0

	Unless required by applicable law or agreed to in writing, software
	distributed under the License is distributed on an "AS IS" BASIS,
	WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
	See the License for the specific language governing permissions and
	limitations under the License.
