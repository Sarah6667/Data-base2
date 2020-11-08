## 花20~30分钟时间，继续练习jqGrid的使用，保存代码提交。

### 制作中英文双语数据

Source: China Daily

Schools in Germany are advising pupils to bring blankets to class and wear hats, coats and scarves during lessons as part of the fight against the coronavirus.
ainst the coronavirus.	

作为抗疫举措之一，德国学校建议学生带毯子来上学，戴帽子围巾、穿厚外套上课。

Head teachers have issued the advice in response to new government guidelines that require schools to ventilate classrooms by opening the windows every twenty minutes.

新的政府指导意见要求学校每20分钟要开窗通风一次，为此各校长发布了这一建议。

Leaving the windows open a crack is not enough. Schools have been told to open classroom windows fully for three to five minutes, and to open doors as well when possible so air can circulate.

窗户只开一条缝是不够的。政府要求学校每次要保持教室窗户大开长达3到5分钟，如果可能的话也要打开门，以保持空气流通。

Daytime temperatures are already as low as 5C in parts of Germany and many classrooms are too cold to study in comfort.

德国部分地区的日间气温已经低至5摄氏度，许多教室都冷得没法好好学习了。

With winter temperatures often well below zero, no one is under any illusions about how cold classrooms could get.

冬天气温通常是零下好几度，谁都能想象到开窗通风情况下教室会有多冷。

### 将上述制作的数据通过jqGrid渲染到网页上
实现代码：
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="utf-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width,initial-scale=1">
    <title>Your page title</title>
       <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
     <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/jqueryui/1.11.4/themes/redmond/jquery-ui.min.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/free-jqgrid/4.15.5/css/ui.jqgrid.min.css">
    <script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/1.12.4/jquery.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/free-jqgrid/4.15.5/jquery.jqgrid.min.js"></script>
    <script>
    //<![CDATA[
    $(function () {
        "use strict";
        $("#grid").jqGrid({
            colModel: [
                { name: "Source" },
                { name: "Target" }
            ],
            data: [
                { id: 10, Source: "Schools in Germany are advising pupils to bring blankets to class and wear hats, coats and scarves during lessons as part of the fight against the coronavirus.", Target: "作为抗疫举措之一，德国学校建议学生带毯子来上学，戴帽子围巾、穿厚外套上课。" },
                { id: 20, Source: "Head teachers have issued the advice in response to new government guidelines that require schools to ventilate classrooms by opening the windows every twenty minutes.", Target: "新的政府指导意见要求学校每20分钟要开窗通风一次，为此各校长发布了这一建议。" },
                { id: 30, Source: "Leaving the windows open a crack is not enough. Schools have been told to open classroom windows fully for three to five minutes, and to open doors as well when possible so air can circulate.", Target: "窗户只开一条缝是不够的。政府要求学校每次要保持教室窗户大开长达3到5分钟，如果可能的话也要打开门，以保持空气流通。" },
                { id: 40, Source: "Daytime temperatures are already as low as 5C in parts of Germany and many classrooms are too cold to study in comfort.", Target: "德国部分地区的日间气温已经低至5摄氏度，许多教室都冷得没法好好学习了。" },
                { id: 50, Source: "With winter temperatures often well below zero, no one is under any illusions about how cold classrooms could get.", Target: "冬天气温通常是零下好几度，谁都能想象到开窗通风情况下教室会有多冷。" }
            ]
        });
    });
    //]]>
    </script>
</head>
<body>
<table id="grid"></table>
</body>
</html>
```
### 创建数据库与表，将上述制作的中英文双语数据导入数据库中

创建了数据库showpdo，数据库表show，双语数据已导入。

### 直接通过pdo访问数据库并包装返回结果

参考：https://jingyan.baidu.com/article/ce43664957dbea3773afd399.html
```
<?php

$pdo=new PDO('mysql:host=localhost;dbname=showpdo','root','root');
try{
	echo "<table border='1'>
	<tr>
	<th>source</th><th>target</th>
	</tr>";
	foreach ($pdo->query("select * from show") as $row)
	{
		echo "<tr>";
		echo "<td>".$row["source"]."</td>";
		echo "<td>".$row["target"]."</td>";
		echo "</tr>";
	}
	echo "</table>";
	
	$db=null;
	
}
catch (PDOException $e){
echo $e->getMessage();
}
?>	
```






