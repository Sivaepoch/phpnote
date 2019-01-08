#### PHP运算符
##### 1.PHP算术运算符

| &nbsp;&nbsp;&nbsp;运算符&nbsp;&nbsp;&nbsp;  |   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;例子&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; |  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;结果&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
| :-------- | :------: | :------: |
| +   |  \$x + \$y |  求和  |
| -   |  \$x - \$y |  差值  |
| *   |  \$x * \$y |  乘积  |
| /   |  \$x / \$y |  商值  |
| %   |  \$x % \$y |  取余 5%2 为 1  |


	<?php
		$x = 10;
		$y = 4;
		echo ($x + $y); // 14
		echo ($x - $y); // 6
		echo ($x * $y); // 40
		echo ($x / $y); // 2.5
		echo ($x % $y); // 2
	?>

##### PHP赋值运算符
* `$a = 5`  把等号右边的值赋值给左边的变量
##### PHP字符串运算符
* `$a = 'siva';$b = 'hello ' . $a;` 用点连接.
##### PHP递增/递减运算符
* 赋值符号的优先级比递增/递减运算符大.先赋值,后递增/递减
	
	<?php
		$x = 5;
		$y = $x ++ ;
		echo $y;  //5
		echo $x; //6
		
		$a = 5;
		$b = 6;
		$c = $a-- + $b--;  // ++同理
		echo $c;  //11
	?>
##### PHP比较运算符
* 同js中比较算法
##### PHP逻辑运算符
* 同js
##### PHP数组运算符

| 运算符&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; |&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 例子&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; |   结果|
| :-------- | --------:| :------: |
| + | \$x + \$y | &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;两个数组的联合,不覆盖重复的键,若有重复.以第一个数组为准 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|
| == | \$x + \$y | &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;两个数组拥有相同的键值对,则返回true &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|
| === | \$x + \$y | &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;两个数组拥有相同的键值对,且顺序类型都相同,则返回true &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|
| != | \$x + \$y | &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;两个数组不同,则返回true&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|
| <> | \$x + \$y | &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;两个数组不同,则返回true&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|
| !== | \$x + \$y | &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;两个数组不同,则返回true&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|


	<?php
		$x = ['a' => 'haha' , 'b' => 'xixi' , 'c' => '12' ];
		$y = ['a' => 'houhou' , 'd' => 'duangduang'];
		$z = ['c' => 12 , 'a' => 'haha' , 'b' => 'xixi'];
		$n = ['a' => 'haha' , 'b' => 'xixi' , 'c' => 12];
		echo '<pre>';
		var_dump($x + $y); //['a' => 'haha','b' => 'xixi' , 'c' => '12' , 'd' => 'duangduang' ] 有相同的键的时候,不会覆盖
 		echo '<br>';
		var_dump($x + $z); //和$x相同
		echo '<br>';
		var_dump($x == $y); //false
		echo '<br>';
		var_dump($x == $z); //true
		echo '<br>';
		var_dump($x === $z); // false (顺序和类型都不相等)
		echo '<br>';
		var_dump($x != $y); //true
		echo '<br>';
		var_dump($x != $z); //fasle
		echo '<br>';
		var_dump($x !== $z); //true
		echo '<br>';
		var_dump($x === $n); //false (类型不同)
		echo '<br>';
	?>

##### 三目运算符
* 同js
