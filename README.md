#Selector——状态选择器

![G1](http://img.blog.csdn.net/20160428164544292)

[GitHub：https://github.com/kongqw/SelectorDemo](https://github.com/kongqw/SelectorDemo)
[我的博客：http://blog.csdn.net/q4878802/article/details/51275718](http://blog.csdn.net/q4878802/article/details/51275718)

##点击按钮换背景图


```
<Button
    android:layout_width="match_parent"
    android:layout_height="wrap_content"
    android:background="@drawable/selector_button_type1"
    android:text="点击按钮换背景图" />
```



##点击按钮换背景色

```
<Button
    android:layout_width="match_parent"
    android:layout_height="wrap_content"
    android:layout_marginTop="10dp"
    android:background="@drawable/selector_radio_button"
    android:text="点击按钮换背景色" />
```


##点击按钮换字体颜色

```
<Button
    android:layout_width="match_parent"
    android:layout_height="wrap_content"
    android:layout_marginTop="10dp"
    android:background="#33333333"
    android:text="点击按钮换字体颜色"
    android:textColor="@drawable/selector_button_type2" />
```

##点击TextView换背景

```
<TextView
    android:layout_width="match_parent"
    android:layout_height="50dp"
    android:layout_marginTop="10dp"
    android:background="@drawable/selector_button_type1"
    android:clickable="true"
    android:gravity="center"
    android:text="点击TextView换背景" />
```

##点击TextView换字体颜色

```
<TextView
    android:layout_width="match_parent"
    android:layout_height="50dp"
    android:layout_marginTop="10dp"
    android:clickable="true"
    android:gravity="center"
    android:text="点击TextView换字体颜色"
    android:textColor="@drawable/selector_button_type2" />
```


##RadioGroup

```
<RadioGroup
    android:layout_width="match_parent"
    android:layout_height="wrap_content"
    android:layout_marginTop="10dp"
    android:orientation="vertical">

    <RadioButton
        android:id="@+id/rb1"
        android:layout_width="match_parent"
        android:layout_height="40dp"
        android:background="@drawable/selector_radio_button"
        android:button="@null"
        android:checked="true"
        android:drawableRight="@drawable/selector_radio_button_right_pic"
        android:paddingLeft="30dp"
        android:paddingRight="30dp"
        android:text="Item 1"
        android:textColor="#FF3A3A3A"
        android:textSize="15sp" />

    <View
        android:layout_width="match_parent"
        android:layout_height="1dp"
        android:background="#FFEFEFEF" />

    <RadioButton
        android:id="@+id/rb2"
        android:layout_width="match_parent"
        android:layout_height="40dp"
        android:background="@drawable/selector_radio_button"
        android:button="@null"
        android:drawableRight="@drawable/selector_radio_button_right_pic"
        android:paddingLeft="30dp"
        android:paddingRight="30dp"
        android:text="Item 2"
        android:textColor="#FF3A3A3A"
        android:textSize="15sp" />

    <View
        android:layout_width="match_parent"
        android:layout_height="1dp"
        android:background="#FFEFEFEF" />

    <RadioButton
        android:id="@+id/rb3"
        android:layout_width="match_parent"
        android:layout_height="40dp"
        android:background="@drawable/selector_radio_button"
        android:button="@null"
        android:drawableRight="@drawable/selector_radio_button_right_pic"
        android:paddingLeft="30dp"
        android:paddingRight="30dp"
        android:text="Item 3"
        android:textColor="#FF3A3A3A"
        android:textSize="15sp" />
</RadioGroup>
```



##其他

* selector_button_type1.xml

	```
	<?xml version="1.0" encoding="utf-8"?>
	<selector xmlns:android="http://schemas.android.com/apk/res/android">
	    <!-- 按下 -->
	    <item android:drawable="@drawable/shape_login_button_press" android:state_pressed="true" />
	    <!-- 获取焦点 -->
	    <item android:drawable="@drawable/shape_login_button_press" android:state_focused="true" />
	    <!-- 正常状态 -->
	    <item android:drawable="@drawable/shape_login_button_normal" />
	</selector>
	```


* selector_radio_button.xml

	```
	<?xml version="1.0" encoding="utf-8"?>
	<selector xmlns:android="http://schemas.android.com/apk/res/android">
	    <item android:drawable="@android:color/white" android:state_enabled="true" android:state_focused="true" android:state_pressed="false" />
	    <item android:drawable="@android:color/darker_gray" android:state_enabled="true" android:state_pressed="true" />
	    <item android:drawable="@android:color/white" android:state_checked="true" android:state_enabled="true" />
	    <item android:drawable="@android:color/white" />
	</selector>
	```


* selector_button_type2.xml

	```
	<?xml version="1.0" encoding="utf-8"?>
	<selector xmlns:android="http://schemas.android.com/apk/res/android">
	    <!-- 按下 -->
	    <item android:color="#55555555" android:state_pressed="true" />
	    <!-- 获取焦点 -->
	    <item android:color="#55555555" android:state_focused="true" />
	    <!-- 正常状态 -->
	    <item android:color="#FF000000" />
	</selector>
	```


* selector_radio_button_right_pic.xml

	```
	<?xml version="1.0" encoding="utf-8"?>
	<selector xmlns:android="http://schemas.android.com/apk/res/android">
	    <item android:drawable="@mipmap/icon_choose" android:state_checked="true" />
	    <item android:drawable="@mipmap/icon_empty" android:state_checked="false" />
	</selector>
	```


* shape_login_button_normal.xml

	```
	<?xml version="1.0" encoding="utf-8"?>
	<shape xmlns:android="http://schemas.android.com/apk/res/android">
	    <solid android:color="#FF4583C9" />
	    <corners android:radius="5dp" />
	    <stroke
	        android:width="1px"
	        android:color="#FF4583C9" />
	</shape>
	```

* shape_login_button_press.xml

	```
	<?xml version="1.0" encoding="utf-8"?>
	<shape xmlns:android="http://schemas.android.com/apk/res/android">
	    <solid android:color="#FFB5CDE9" />
	    <corners android:radius="5dp" />
	    <stroke
	        android:width="1px"
	        android:color="#FFB5CDE9" />
	</shape>
	```

