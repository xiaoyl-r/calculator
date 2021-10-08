# 校园生活计算器App

## 项目介绍
#小组: 永远在debug</br>
#小组成员： 潘美然、肖玉兰</br>
#项目主题：校园生活计算器
#开发环境: Android Studio
#语言: Java

## 项目进度安排
|  时间   |进度安排|
| :----: | :---- |
| 9/22-9/27 |设计app的UI界面</br>实现四则运算功能|
| 9/28-9/5 | 各自完成五项额外功能</br>上传代码到github</br>将代码实现的功能汇总到一个项目中</br>互相提出改进建议|
| 9/6-10/12 |选择部分用户进行测试，获取反馈意见，改进app</br>有时间的前提下完善各项功能，在原有的基础上创新，打造我们的特色</br>小组成员交流，分享心得体会，准备项目发布材料</br>发布项目|
| 10/12-之后 |投入小规模使用，维护app运行</br>改进app相应功能，获取更多用户|

## 功能介绍

### 四则运算

实现实数范围内的基本加减乘除运算，包括有括号的优先级运算。目前主要是输入整数和小数，不提供分数和根式输入。  

实现方法：  

因为是用java代码写四则运算，会涉及到精度丢失的问题，这里借助了java提供的BigDecimal类。目前限制保留小数位数6位。  

此外，输入错误的表达式会报错。  

[![5ipSdU.jpg](https://z3.ax1x.com/2021/10/08/5ipSdU.jpg)](https://imgtu.com/i/5ipSdU)

### 三角函数计算

三角函数计算主要借助了java里面的math类自带的三角函数计算，同样为了防止精度丢失，用了BigDecimal类，且限制保留6位小数。  

使用注意事项：  

用户必须自己手动添加右括号,否则会报错，在结果显示栏显示“error！”  

[![5ipPJJ.jpg](https://z3.ax1x.com/2021/10/08/5ipPJJ.jpg)](https://imgtu.com/i/5ipPJJ)

### 反应速度测试

反应速度测试结合了打地鼠小游戏，让测试变得更加有趣！  

测试游戏设置为横屏模式，主要是为了增加用户的体验。目前仅支持横屏模式。  

从人物开始出现到点击人物，计算用户反映时间，根据用户反应时间反馈。  

反应时间小于120ms，屏幕上会显示反应时间和“您的反应速度比刘翔还快！”； 

反应在120ms到400ms之间，屏幕上会显示反应时间和“哎哟不错哦”；

超过400ms，显示反应时间和“你比正常人稍稍慢了点”。  

[![5iSsaD.jpg](https://z3.ax1x.com/2021/10/08/5iSsaD.jpg)](https://imgtu.com/i/5iSsaD)

点击右下角“开始”按钮，开始反应速度测试。  

进入游戏背景音乐会自动打开，右上角可以选择打开或关掉背景音乐。  

左上角会有计时器，30s后会自动询问用户是否继续。点击继续会从新开始计时，点击退出会回到主界面。  

也可以自行点击右下角“退出”按钮返回主界面。 

### 节假日倒计时&考试时间倒计时

节假日倒计时为用户提供更加直观的节假日时间概念，而考试时间倒计时则为不清楚各类大赛、考证日期的用户提供信息。  

实现方法：  

首先使用Calendar类获取实时日期，动态展示在卡片控件上。  

同时，采用了Date类转换Integer计算天数差，然后再转换成String显示在控件上。节日列表的整体控件使用了RecyclerView，传入一个特定  

的HolidayItem List作为数据源。

[![5iSBqK.jpg](https://z3.ax1x.com/2021/10/08/5iSBqK.jpg)](https://imgtu.com/i/5iSBqK)

### 图形计算器
包含六个基础图形（圆形、球形、平行四边形、圆环、三角形、椭圆）的函数计算，比如弧长、面积、体积、周长等，便于用户计算一些简单  

的图形数据。  

其中，加入了空值判定，在一些必须要输入的数据空缺时，会发出提醒；对于圆环，如果没有输入中心角，则默认为360°；  

此外，三角形还额外增加了能否构成三角形的提醒。  

对于计算过程，首先从EditText获取用户输入的数据，然后转换为Integer，计算后再转换为String显示。

[![5iSGaF.jpg](https://z3.ax1x.com/2021/10/08/5iSGaF.jpg)](https://imgtu.com/i/5iSGaF)

### 刷锻完成时间预测
根据用户输入的每周锻炼情况，结合目前已经完成的公里数，计算出预计的80km刷锻完成时间。由此，用户可以用这一数据  

和刷锻截止时间相比较，结合天气、季节等因素，对自己的计划做出调整。  

实现方法：  

基本原理与日期的计算差不多。这里同样加入了空值判断，但与图形计算稍有不同，需考虑实际情况，比如没有游泳计划等等。  

[![5iSn8s.jpg](https://z3.ax1x.com/2021/10/08/5iSn8s.jpg)](https://imgtu.com/i/5iSn8s)

### BMI计算

简单明了的BMI计算界面，数据输出后，用户可以根据界面上的数值表进行对比。  

实现方法：根据公式体重/身高^2，考虑到用户习惯于输入厘米制，因此还加入了一个单位转换。

[![5iSSCd.jpg](https://z3.ax1x.com/2021/10/08/5iSSCd.jpg)](https://imgtu.com/i/5iSSCd)

## App下载方式

可直接将apk文件传到安卓手机上下载
