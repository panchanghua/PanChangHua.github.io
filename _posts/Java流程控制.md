### Java流程控制
### 1.顺序结构
	顺序结构是程序中最简单最基本的流程控制，没有特定的语法结构，按照代码的先后顺序，依次执行，程序中大多数的代码都是这样执行的。
### 2.分支结构
	分支结构也被称为选择结构。
	分支结构有特定的语法规则，代码要执行具体的逻辑运算进行判断，逻辑运算的结果有两个，所以产生选择，按照不同的选择执行不同的代码。
#### if
	if(关系表达式) {//首先判断关系表达式看其结果是true还是false
	     语句体1;//如果是true就执行语句体
	}//如果是false就不执行语句体
#### if else
	if(关系表达式) {//首先判断关系表达式看其结果是true还是false
	     语句体1;//如果是true就执行语句体1
	}else {
		 语句体2;//如果是false就执行语句体2
	}
#### if else if else
	if(关系表达式1) {//首先判断关系表达式1看其结果是true还是false
	     语句体1;//如果是true就执行语句体1
	}else  if (关系表达式2) {//如果是false就继续判断关系表达式2,看其结果是true还是false
		 语句体2;//如果是true就执行语句体2
	}//如果是false就继续判断关系表达式…看其结果是true还是false
	……
	else {
		 语句体n+1;//如果没有任何关系表达式为true，就执行语句体n+1
	}
#### switch
	switch(表达式)
	{ 
		case 常量值1:
			语句块1
    		[break;]
		...
		case 常量值n:
    		语句块2
    		[break;]
		default:
    		语句块 n+1;
	}
	switch语句中表达式的值必须是整型或字符型，常量值1~n必须也是整型或字符型。JDK1.7后加入字符串。
	switch语句先计算表达式的值，如果表达式的值与case后的常量值相同，则执行该case后的若干个语句，直到遇到break语句为止。如果没有break，则继续执行下一case中的若干语句，直到遇到break为止。若没有一个常量的值与表达式的值相同，则执行default后面的语句。default语句可选，如果不存在default语句，而且switch语句中的表达式的值与任何case的常量值都不相同，则switch不做任何处理。并且，同一个switch语句，case的常量值必须互不相同。
### 3.循环结构
	循环语句就是在满足一定条件的情况下反复执行某一个操作。包括while循环语句、do···while循环语句和for循环语句。
#### while
	while循环语句的循环方式为利用一个条件来控制是否要继续反复执行这个语句。
	while(条件表达式) {
		循环体
	}
#### do···while
	do···while循环语句与while循环语句的区别是，while循环语句先判断条件是否成立再执行循环体，而do···while循环语句则先执行一次循环后，再判断条件是否成立。也即do···while至少执行一次。
	do
	{
    	循环体
	}  while (条件表达式);
####  for
	for(表达式1; 表达式2; 表达式3)
	{
		语句序列
	}
	表达式1为初始化表达式，负责完成变量的初始化；表达式2为循环条件表达式，指定循环条件；表达式3为循环后操作表达式，负责修整变量，改变循环条件。
#### 增强for（foreach）
	foreach是Java5后新增的for语句的特殊简化版本，并不能完全替代for语句，但所有foreach语句都可以改写为for语句。
	for(元素变量x : 遍历对象obj) {
		循环体;
	}
### 跳转语句
#### break
	break语句在for、while、do···while循环语句中，用于强行退出当前循环，为什么说是当前循环呢，因为break只能跳出离它最近的那个循环的循环体。
	假设有两个循环嵌套使用，break用在内层循环下，则break只能跳出内层循环
	for(int i=0; i<n; i++) {    // 外层循环
	    for(int j=0; j<n ;j++) {    // 内层循环
	        break;
	    }
	}
#### continue
	continue语句只能用于for、while、do···while循环语句中，用于让程序直接跳过其后面的语句，进行下一次循环。
	while(i < 10) {
		i++;
		if(i%2 == 0) {
			continue;    // 跳过当前循环
		}
	}
#### return
	return语句可以从一个方法返回，并把控制权交给调用它的语句。
