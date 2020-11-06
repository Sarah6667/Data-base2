## 练习php解析tmx

来源：https://www.runoob.com/php/php-xml-simplexml.html

### 使用 PHP simpleXML
xml文件：
```
<?xml version="1.0" encoding="ISO-8859-1"?>
<note>
<to>Tove</to>
    <from>Jani</from>
    <heading>Reminder</heading>
    <body>Don't forget me this weekend!</body>
</note>
```

1. 输出 $xml 变量（是 SimpleXMLElement 对象）的键和元素
php文件：
```
<?php
$xml=simplexml_load_file("note.xml");
print_r($xml);
?>
```
输出： SimpleXMLElement Object ( [to] => Tove [from] => Jani [heading] => Reminder [body] => Don't forget me this weekend! )

2. 输出 XML 文件中每个元素的数据：
php文件：
```
<?php
$xml=simplexml_load_file("note.xml");
echo $xml->to . "<br>";
echo $xml->from . "<br>";
echo $xml->heading . "<br>";
echo $xml->body;
?>
```
输出：SimpleXMLElement Object ( [to] => Tove [from] => Jani [heading] => Reminder [body] => Don't forget me this weekend! )

### 使用phpQuery
php文件：
```
<?php
include 'phpQuery.php'; 
phpQuery::newDocumentFile('note.xml'); 
echo pq('contact > age:eq(0)');
?>
```
输出：SimpleXMLElement Object ( [to] => Tove [from] => Jani [heading] => Reminder [body] => Don't forget me this weekend! )
