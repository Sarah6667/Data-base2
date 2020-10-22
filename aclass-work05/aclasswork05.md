### 学习jqGrid custom cell formatter的使用

参考： https://blog.csdn.net/chuangxin/article/details/86699635

#### 练习代码

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
$(function () {
        "use strict";
        $("#grid").jqGrid({
            colModel: [
                { name: "Item" },
                { name: "Price", formatter:'number',
					formatoptions:{
					thousandsSeparator: ",",
					decimalSeparator: ".",
					decimalPlaces : 1,
					deaultValue: "0.0"}
				
				}
            ],
            data: [
                { id: 1, Item: "A Dress", Price: "1317.8"},
				{ id: 2, Item: "A T-shirt", Price: "59.2"},
				{ id: 3, Item: "A Trouser", Price: "101.35"},
				{ id: 4, Item: "A shirt", Price: "80.01"}
			]
        });
    });
</script>	
</head>
<body>
<table id="grid"></table>
</body>
</html>
```

