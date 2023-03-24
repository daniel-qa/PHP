* 查看 Cookie  
```
F12 -> Application -> Storage -> Cookies
```

* [javascript trace](https://github.com/daniel-qa/PHP/wiki/javascript-trace)

* Trace
```
  echo "test1 __construct <br>";
  exit;
```

```
echo " php test ";

echo " php test ";exit;

//echo " jeff test";
//exit;

// echo $abc;exit;
```


* 印出 boolan 值

```
echo $bool_val ? 'true' : 'false';

Or if you only want output when it's false:
echo !$bool_val ? 'false' : '';
```


* 在 View 中 打印 Debug 字串

```
<?php echo "view test";exit; ?>

```

* 打印 json Array

```
 echo json_encode($arr);
```
* 打印 Array
```
$fruits = array("Apple", "Mango", "Banana", "Pears", "Watermelon", "Guava");
print_r($fruits);
```

* var_dump
```
Catchable fatal error: Object of class stdClass could not be converted to string in ……\***.php on line 10

具体错误是语句：echo $result;
从错误说明中可知$result是class stdClass类型，我们用var_dump()函数进行了输出，此函数显示关于一个或多个表达式的结构信息，包括表达式的类型与值。数组将递归展开值，通过缩进显示其结构。 语句为

var_dump($result);

显示结果为：

object(stdClass)＃2 (1) { ["return"]=> string(46) "Hello, My Friend!"}

很明显，我们想要输出的结果就是“Hello,My Friend!”，代表的就是这个类对象中return变量的值，因此，我们可用如下语句输出我们想要的值：

echo $result->return;

替代原来的echo $result；
```

* js 

```
console.log('123');
// 查看 主控台的 log是否有出現  log 字串
alert('hello world');
//直接會跳出 Alert 訊息

```

* 迴圈中，直接指定出錯元素執行

```
foreach ($filed as $item) {

 $item = $filed[2];

}
```


* chrome F12

https://blog.51cto.com/u_12890843/5347153


* DOM元素节点发生改变时
```
在Elements面板中指定的DOM节点上右击，在弹出的菜单中选择Break on…，可以看到三个选择项，比如我们选择Subtree modifications，
那么当选择的节点里面的子节点被添加、删除、修改，则断点就会被触发。

```

* F12 檢視歷紀錄
``` 
  Preserve log 打開  
```
