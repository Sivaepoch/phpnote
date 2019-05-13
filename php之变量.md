#### 变量

##### 1.可变变量
```java
	$name = 'siva';
	$siva = '24';
	echo $$name;  // 24
```

##### 2.超全局变量
```java
	$u = $_GET['uername'];  //get方法
	$u2 = $_POST['username']; // post方法
	// 可以获取表单中 <input type="text" name="username" />的值
	$_COOKIE //得到会话控制中cookie传值
	$_SESSION //得到会话控制中session传值
	$_FILES //得到文件上传的结果
	$_REQUEST //既能得到get传值结果,又能得到post传值结果
```

##### 3.环境变量
*  环境变量主要用的是$_SERVER 和 `$_ENV`两个,$_ENV逐渐被废弃
* 一些常用的环境变量

```java
	$_SERVER["REQUEST_METHOD"]  //请求当前php页面的方法
	$_SERVER["REQUEST_URL"]  //请求的url
	$_SERVER["REQUEST_SOFTWARE"]  //用的哪一种服务器
	$_SERVER["REMOTE_ADDR"]  //客户的IP地址
	$_SERVER["SERVER_ADDR"]  //当前服务器的IP地址
	$_SERVER["SCRIPT_FILENAME"]  //请求文件的路径
	$_SERVER["HTTP_USER_AGENT"]  //当前访问这个网址的电脑和浏览器的情况
	$_SERVER["HTTP_REFERER"]  //上级来源(用户从哪个地址进入当前网页)
	$_SERVER["REQUEST_TIME"]  //当前的时间
```

##### 4.变量引用
```java
	$test = 5;
	$test2 = $test;
	$test2 = 6;
	echo $test2; //6
	echo $test; //5
```

```java
	$test = 5 ;
	$test2 = &$test;
	$test2 = 6;
	echo $test2; //6
	echo $test; //6
```
> 变量前加上&符号,把变量指向同一个存值空间,也就是第二个例子里,$test变化的话,$test2就会变化,$test2变化的话,$test也会变.

