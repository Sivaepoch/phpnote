####  一  echo && print

#####1. 区别
* echo -- 可以输出一个或多个字符串;
*  print -- 只允许输出一个字符串,返回值为1;
*  echo输出的速度比print快.echo没有返回值.

##### 2.echo
echo是一个语言结构,使用的时候可以加括号,也可以不加;

    echo xxx;
    echo(xxx);

#### 二 数据类型
* Interger(整型);
* String(字符串);
* Float(浮点型);
* Boolean(布尔型);
* Array(数组);
* Object(对象);
* NULL(空值);

##### 1.查看数据类型
* gettype()  -- 可以获得变量的类型
* var)dump() -- 可以获得变量的类型,长度和值
##### 2.整型(int)
* 整数规则
	* 整数必须有至少一个数字
	* 整数不能包含逗号或空格
	* 整数不能有小数点
	* 整数正负均可
	* 可以用三种格式规定整数:十进制,十六进制,八进制
##### 3.字符串(String)
* 声明字符串
	* 用单引号声明
	* 用双引号声明
	* 用字界符声明(需要输入非常大段的字符串时使用)
* 单引号声明
	* `$name = 'siva'`
	
* 双引号声明
	* `$name = "siva"`
* 字界符声明
	*  在变量后面的等号写三个小于号 <<<;
	*  然后在 <<< 后面写上字符
	*  然后换行写上任意想写的字符
	*  写完后,顶行.在行的最开始处,写上<<< 后面的字符和分号.
	
    <?php
    $name = <<<ABC
    我是
	    用
    定界符
	    定义的
    字符串
    ABC;  
    ?>

##### 4.浮点型(float/double)
##### 5.布尔型(bool -- true/false)
##### 6.数组(Array)
	$names = array('siva','lara','alex');
	$otherName = ['siva','lara','alex'];
##### 7.对象(Object)
* 在php中,必须明确的尚明对象
* 必须先声明对象的类,之后再细说
#####8.NULL
* 通过变量赋值,明确的指定变量为NULL;
* 没有声明变量 或者声明变量但没有赋值
* 使用函数unset()将变量销毁掉
	
	<?php
	$a = null;
	$b;
	$c = 'hh';
	unset($b);
	var_dump($a);  // NULL
	var_dump($b);   // NULL
	var_dump($c);   // NULL
	var_dump($d);   // NULL
	?>

##### 9.empty()
* 变量的值如果为false或者null,返回true
#####10.isset()
* 可以向括号中传入一个或者多个变量,其中只要有一个变量为null,则返回false,否则,返回true;

	<?php
		$a = 0;
		$b = false;
		$c = null;
		isset($a,$b,$c);  //false
		isset($a,$b); // true
	?>
	
	