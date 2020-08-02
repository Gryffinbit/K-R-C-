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

* 当fahr=0，20，....300时，分别打印华氏温度和摄氏温度对照表

```
#include <stdio.h>

int main(void)
{
    int fahr,celsius;
    int lower,upper,step;

    lower = 0;   /*温度表的下限*/
    upper = 300;  /*温度表的上限*/
    step = 20;  /*步长*/

    fahr = lower;
    while (fahr <= upper){
        celsius = 5 * (fahr - 32) / 9;
        printf("%3d\t%6d\n",fahr,celsius);
        fahr = fahr + step;
    }

}
```

* 浮点数版本  当fahr=0，20，....300时，分别打印华氏温度和摄氏温度对照表  
> 常数中的小数点表明该常数是一个
    }浮点型
    }，因此5.0/9.0是两个浮点数相除，结果不会被舍位
    
```
#include <stdio.h>

int main(void)
{
    float fahr,celsius;
    int lower,upper,step;

    lower = 0;   /*温度表的下限*/
    upper = 300;  /*温度表的上限*/
    step = 20;  /*步长*/

    fahr = lower;   /*把int型操作数转换为float型*/
    while (fahr <= upper){
        celsius = (5.0/9.0) * (fahr - 32);
        printf("%3.0f\t%6.1f\n",fahr,celsius);   /* %3.0f表示待打印的浮点数至少占3个字符宽，且不带小数点和小数部分*/
        fahr = fahr + step;  /* %6.1f表明至少占6个字符宽，且小数点后面有一位数字 */
    }

}
```
