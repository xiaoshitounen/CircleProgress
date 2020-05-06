# CircleProgress 时间进度器

详细内容参考博客:[自定义View-CircleProgress](https://fanandjiu.com/%E8%87%AA%E5%AE%9A%E4%B9%89View-CircleProgress/)

简介：

用于记录时间的流逝，除了文本显示之外，还有进度显示。

app模块是使用例子，其运行效果：

![](https://github.com/xiaoshitounen/PageController/blob/master/self_view_page_controller.gif)


### 1. 添加依赖

Step 1. Add the JitPack repository to your build file

Add it in your root build.gradle at the end of repositories:
~~~
allprojects {
  repositories {
    ...
    maven { url 'https://jitpack.io' }
  }
}
~~~

Step 2. Add the dependency
~~~
dependencies {
    implementation 'com.github.xiaoshitounen:CircleProgress:1.0.5'
}
~~~

### 2. Xml文件中静态添加使用

~~~
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <swu.xl.circleprogress.CircleProgress
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        android:layout_centerInParent="true"
        app:total_progress="100"
        app:progress="20.0000"
        app:startAngle="270"
        app:endAngle="450"
        app:textColor="#ffffff"
        app:textSize="22"
        app:textLeftPadding="10"
        app:textTopPadding="10"
        />

</RelativeLayout>
~~~

#### ① 属性

- progress：当前的进度值，默认是0
- total_progress：总的进度值，默认是100
- startAngle：进度开始的位置，默认是0
- endAngle：进度结束的位置，位置是360
- textSize：进度文本的字体大小，默认是14sp
- textColor：进度文本的字体颜色，默认是白色
- textLeftPadding：绘制文本的左边间距
- textTopPadding：绘制文本的上边间距

#### ② 页面样式

页面样式是一个xml文件，目前不可以定义你想要的样式。

例子：
~~~
<?xml version="1.0" encoding="utf-8"?>
<shape xmlns:android="http://schemas.android.com/apk/res/android"
    android:shape="oval">

    <solid android:color="#E48093"
        />

    <stroke android:width="8dp" android:color="#EAB3BE"
        />

    <size android:width="120dp"
        android:height="120dp"/>

</shape>
~~~
