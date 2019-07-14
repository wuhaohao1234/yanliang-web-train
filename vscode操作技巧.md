# vscode 全局替换

* 适用正则表达式替换

1. ctrl l + f 为查找选中

	这里可以写入正则表达式

	<link href=(.*) rel=(.*)>

	href内地址匹配所有, ref内地址匹配所有

2. ctrl + h 为替换

	<link th:href="@{$1}" rel=prefetch>

	匹配为 已@{为开头

	$1 : 为开头的意思


