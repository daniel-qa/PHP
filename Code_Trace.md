* F12 檢視歷紀錄
``` 
  Preserve log 打開  
```

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
