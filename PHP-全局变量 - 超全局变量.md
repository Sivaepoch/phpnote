##### PHP全局变量 - 超全局变量
##### 定义
* PHP中的许多预定义变量都是超全局的,这意味着他们在一个脚本的全部作用域中都可用.在函数或者方法中无需执行global
##### $GLOBALS
* $GLOBAL 是一个包含了全部变量的全局组合数组.变量的名字就是数组的键.

	<?php
	$x = 5;
	$y = 6;
	function test(){
		$GLOBALS['z'] = $GLOBALS['x'] + $GLOBALS['y'];
	}
	test();
	echo $z; //11
	?>
##### $_REQUEST
* 当用户点击提交按钮时,可以用$_REQUEST收集表单中的input字段数据

	<HTML>
		<body>
			<form methods="post" action="<?php echo $_SERVER['PHP_SELF'];?>"
				Name:<input type="text" name="name"/>
				<input type="submit">
			</form>

			<?php
				$name = $_REQUEST['name'];
				echo $name;
			?>
		</body>
	</HTML>