### 练习使用bootstrap框架设计编写自己的在线CAT系统的宣传首页
    
代码如下：

```
<!DOCTYPE html>
<html>
<head>
  <title>Bootstrap 实例</title>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <link rel="stylesheet" href="https://cdn.staticfile.org/twitter-bootstrap/4.3.1/css/bootstrap.min.css">
  <script src="https://cdn.staticfile.org/jquery/3.2.1/jquery.min.js"></script>
  <script src="https://cdn.staticfile.org/popper.js/1.15.0/umd/popper.min.js"></script>
  <script src="https://cdn.staticfile.org/twitter-bootstrap/4.3.1/js/bootstrap.min.js"></script>

<style>
	.list-group-horizontal .list-group-item {
		display: inline-block;
	}
</style>
</head>
<body>

<div class="container">

      <div class="list-group list-group-horizontal">
        <a href="#" class="list-group-item active">Home</a>
        <a href="#" class="list-group-item">About</a>
        <a href="#" class="list-group-item">Contact</li>
		
	  
	  </div>

	  <div class="btn-group" style="float:right">
	  <button type="submit" class="btn btn-primary" >Register</button>
	  <button type="submit" class="btn btn-primary" >Log In</button>
	  </div>
      <p class="text-info">Welcome to this website. Hope you will get help.</p>
     
</div>
<div class="list-group list-group-horizontal">
        <a href="#" class="list-group-item active">Project management</a>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
        <a href="#" class="list-group-item">Term Base</a>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
        <a href="#" class="list-group-item">Translation Memory</li>
		
</div>

<img src="cat.bmp" alt="cat" title="cat" style="position:absolute;left:180px;top:80px;"/>
</body>
</html>
```

#### 参考

菜鸟教程
