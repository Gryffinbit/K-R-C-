# 示例代码  
## 1.1  
* 第一个C语言程序  
```
#include <stdio.h>     //包含标准库的信息

/* 第一个C语言程序 */

main()                //定义名为main的函数，它不接受参数值
{
	printf("hello,world\n ");    //main函数的语句都被括在花括号中 
	
}
```  

* 多次调用该函数以分阶段得到一个长的输出行  
```
#include <stdio.h>

main()
{
	printf("hello, ");
	printf("world");
	printf("\n");
}
```
