## ES6-数组,字符串,面向对象

#### 数组--map
> 映射,返回一个新的数组(一个对应一个)
```java
	let score = [90,20,61,58]
	let result = score.map(item => item > 60 ? '及格' : '不及格')
	console.log(score)  //[90,20,61,58]
	console.log(result) // ['及格','不及格','及格','不及格']
```
#### 数组-- reduce 
> 汇总,返回一个值(一堆出来一个)
```java
	//总和
	let arr = [12,90,150,52]
	arr.reduce((tmp,item,index) => {
		return tmp + item;
	})
```
#### 数组--filter
> 过滤器,筛选符合条件的
```java
	let arr = [12,5,8,99,27,36,56]
	let result = arr.filter(item => {
		return item % 3 == 0
	})
	console.log(result) //[12, 99, 27, 36]
```

#### 数组--forEach (迭代)
```java
	let arr = [12,25,1,12]
	arr.forEach((item,index) => {
		console.log(`第${index+1}个元素是${item}`)
	})
	//第1个元素是12
	//第2个元素是25
	//第3个元素是1
	//第4个元素是12
```
#### 字符串-- startsWith
判断字符串是否为指定元素开头
```java
	let str = 'https://www.qingxiaoyun.com'
	if(str.startsWith('https://')){
		console.log('加密地址')
	}else if(str.startsWith('git://')){
		console.log('git地址')
	}else if(str.startsWith('svn://')){
		console.log('svn地址')
	}
	// 加密地址
```
#### 字符串-- endsWith
判断字符串是否为指定元素结尾
```java
	let str = '1.txt';
	if(str.endsWith('.txt')){
		console.log('文本文件')
	}else if(str.endsWith('.png')){
		console.log('png图片')
	}
	// 文本文件
```

#### 字符串模板
```java
	let name = `siva`
	let str = `欢迎您!${a}` //欢迎您!siva"
	let title = '我是一个标题!'
	let tmp = `
		<h1>${title}</h1>
		<p>我是一个副
		标题</p>
	`
	//"
	//	<h1>我是一个标题!</h1>
	//	<p>我是一个副
	//	标题</p>
	//"
```

#### 面向对象
```java
	// es5的面向对象
	function User(name,age){
		this.name = name
		this.age = age
	}
	User.prototype.getName = function(){
		console.log(this.name)
	}
	User.prototype.getAge = function(){
		console.log(this.age)
	}
	var siva = new User('siva','24')
	siva.getName() // siva
	siva.getAge() // 24
	
	// 继承
	function VipUser(name,age,level){
		User.call(this,name,age)	
		this.level = level
	}
	VipUser.prototype = new User();
	VipUser.prototype.constructor = VipUser;
	VipUser.prototype.getLevel = function (){
		console.log(this.level)
	}

	var v1 = new VipUser('alex','20',3)
	v1.getName() // 'alex'
	v1.getAge() //20
	v1.getLevel() // 3
	
```

```java
	// es6
	class User {
		constructor(name,age){
			this.name = name
			this.age = age
		}
		getName(){
			console.log(this.name)
		} 
		getAge(){
			console.log(this.age)
		}
	}

	class VipUser extends User{
		constructor(name,age,level){
			super(name,age) // 父类 == 超类
			this.level = level
		}
		
		getLevel(){
			console.log(this.level)
		}
	}
	
	var siva = new VipUser ('siva','24',3)
	siva.getName() // siva
	siva.getAge() // 24
	siva.getLevel() // 3
	
```
