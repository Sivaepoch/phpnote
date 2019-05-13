#### 数组
##### 数组的长度
* count()

	$name = ['siva','lara','alex'];
    echo count($name); // 3

##### 数组排序  sort()--升序 / rsort() --降序
* **sort一般是用来排序数字索引数组的,如果关联数组通过sort排序,则键值会丢失**

	<?php
		$x = [100,3,9,k,a,A];
		$y = [a => nn, b => cc , c => aa];
		sort($x);sort($y);
		var_dump($x); // [A,a,k,3,9,100]
		var_dump($y); // [aa,cc,nn] 索引变成数字
     ?>
#####  关联数组排序 asort() -- 升序 / arsort() -- 降序
	<?php
		$y = [a => nn, b => cc , c => aa];
		asort($y);
		var_dump($y); // [c => aa , b => cc , a => nn]
	?>
##### 对键值排序 ksort() -- 升序 /  krsort() -- 降序
	<?php
		$y = [b => nn, c => cc , a => aa];
		ksort($y);
		var_dump($y); // [a => aa , b => nn , c => cc]
	?>