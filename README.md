# ui
一个集串口调试助手、示波器和图像显示三个功能于一体的上位机，请看README！
Example中是所有的基于Qt的源文件，demo中是脱离Qt环境输出时产生的文件，具体方法请看网上教程。
Output中是完全可用的最终版和通信协议以及配置教程，单片机采用Kea128系列，我相信如果你有兴趣开发上位机，那把这个通信协议移植到stm32上是轻而易举的。
另外两个文件是debug和release产生的一些输出文件，作用不大。
这是我第一次在Qt平台开发软件，整体框架结构并不好，希望广大有兴趣的朋友可以加入一起开发完善。

QQ交流群：823710278

下边是对有兴趣的同学进行里边一些文件的依赖关系进行简单的说明，因为确实有些乱。（手动微笑）
所有的ui界面都是通过编程实现，没有用Qt自带的ui设计器，所以格式配置内容比较多，第一次做，太粗糙。
main.cpp是main函数所在文件
menu.cpp对ui界面的一些细节作出设置
content.cpp对下述三个模块进行汇总的一个雷

usart.cpp是串口调试助手所在类的文件

electric.cpp是示波器模块所在类
echart.cpp是示波器模块中用于波形显示的类
emythread.cpp是因为在示波器模块中由于要处理的数据过于庞大（16个通道同时进行），所以用了多线程

camera.cpp是图像显示模块所在类
epoint.cpp是图像输出的类

希望有兴趣的朋友可以加入我们，共同开发。
