# QT学习

<p align=right>~J.K. Huang</p>

[toc]

[QT教程](https://qtguide.ustclug.org/ch00-00.htm)

## 安装

在[QT中文官网](https://www.qt.io/zh-cn/)下载[在线安装程序](https://www.qt.io/download-qt-installer?hsCtaTracking=99d9dd4f-5681-48d2-b096-470725510d34%7C074ddad0-fdef-4e53-8aa8-5e8a876d6ab4)

注册账号

**安装文件夹**时选择custom installation便于后续自行选择组件，安装组件介绍如下：

![在这里插入图片描述](https://pic-1312360537.cos.ap-nanjing.myqcloud.com/images/202208300957876.png)

个人后续可能需要配合VS使用，但自带IDE也进行了安装，具体选项如下;Qt Design Studio部分尚不清楚 所以按默认配置。

![image-20220703223147940](https://pic-1312360537.cos.ap-nanjing.myqcloud.com/images/202208300957453.png)

## 学习

### main函数

```C++
#include <QtWidgets/QApplication>
#include <QtWidgets/QLabel>

int main(int argc, char *argv[])
{
    QApplication a(argc, argv); //定义一个 Qt 应用程序对象 Qt图形界面程序的入口
    QLabel label( QLabel::tr("Hello Qt!") ); //定义了一个 QLabel 标签控件对象
    label.show(); //显示控件窗口

    return a.exec(); //进入 Qt 应用程序的事件循环函数等待用户操作
}
```

所有的Qt类均包含tr函数，代表可翻译字符串

