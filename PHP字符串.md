
#### 字符串

##### 1. 单引号声明 和双引号声明的区别
* 双引号解析变量,单引号不解析
* 在双引号里面插入变量,变量后面如果有中文或英文字符,他会把这个字符和变量拼接起来,视为一整个变量.一定要在变量的后面接上特殊字符,例如空格分开
* 在双引号里面插变量的时候,后面不想有空格,可以拿大括号将变量包起来
* 双引号解析转义字符,单引号不解析
* 单引号的效率高于双引号,尽可能使用单引号
* 双引号和单引号可以互插,双引号中插入单引号,单引号中插入变量,这个变量会被解析
* 我们将定界符声明字符串视为双引号一样的功能来看.

```java
	<?php
		$name = 'siva';
		$test = "$name 名字会出现吗?";  
		$test2 = '$name 名字会出现吗?';  
		$test3 = "{$name}名字会出现吗?";
		$test4 = "'$name'名字会出现吗?";
		echo $test;  // siva 名字会出现吗?
		echo $test2;  // $name 名字会出现吗?
		echo $test3;  //siva名字会出现吗?
		echo $test4;  //'siva'名字会出现吗?
	?>
```

##### 2. 字界符声明
* 在变量后面的等号后写三个小于号(<<<)
* 在<<<后写字符(建议英文大写字符)
* 换行写上你任意想写的字符
* 洗完后,顶行,在行最开始处,写上<<<后面的字符和分号
```java
	<?php
		$test = <<< ABC
			如果
			<b>你有</b>
			<h2>哈哈哈</h2>
		ABC;
	?>
```
##### 3. 字符串链接

    <?php 
	    $a = 'hello';
	    $name = ' siva';
	    $plat = '简书';
	    echo $a . $name . '!欢迎来到' . $plat  // hello siva!欢迎来到简书
	 ?>
	 
##### 4. strlen()
* 返回字符串的长度
* 在utf-8下 strlen()把中文字符算成3个字节,英文,空格,符号占1个;

	<?php
		$name = '欢迎你!';
		echo strlen($name) ; //10
		echo strlen('hi bye!'); // 7
	?>
	
##### 5.  strpos() 
* 在字符串内查找一个字符或一段指定的文本.
* 若在字符串中找到匹配,该函数会返回**第一个匹配**的字符位置,如果未找到匹配 返回false

	<?php
		echo strpos( 'welcome','l'); //2
		echo strpos( '我的世界','世'); //6
	?>
	
##### 6.常量
* 常量是单个值的标识符,在脚本中无法改变该值
* 有效的常量名以字符或者下划线开头(常量名称前面没有$符号)
* 常量名可以小写,通常用大写
* 常量是贯穿整个脚本,是自动全局的.
* 设置PHP常量
	* 使用define()函数
	* 首个参数定义常量的名称
	* 第二个参数定义常量的值
	* 第三个参数可选,规定常量名是否对大小写敏感.默认false

	<?php
		define('STATICSTR','welcome!');
		echo STATICSTR;  // welcome!
		echo staticstr; //staticstr!
		
		define('STATICSTRS','welcome!',true);
		echo STATICSTRS; //welcome!
		echo staticstrs; // welcome!
	?>
* 常量默认是全局变量,可以在整个运行的脚本的任何地方使用

	<?php
		header('Content-type:text/html;charset=utf-8');
		define('STATICSTR','你好');
		function test(){
			echo STATICSTR;
		}
		test();   // 你好
	?>


