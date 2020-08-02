# 练习代码  
## 练习1-2 
> 参数字符串中出现\c  
```
#include <stdio.h>     //包含标准库的信息

main()                //定义名为main的函数，它不接受参数值
{
	printf("hello,world\c ");    //main函数的语句都被括在花括号中 
	
}
```

> 运行结果: hello,worldc 

## 练习1-3
> 修改示例，使之在转换表的顶部打印一个标题  
```
#include <stdio.h>

int main(void)
{
    float fahr,celsius;
    int lower,upper,step;

    lower = 0;   /*温度表的下限*/
    upper = 300;  /*温度表的上限*/
    step = 20;  /*步长*/
    printf("----温度转换表----\n");
    fahr = lower;
    while (fahr <= upper){
        celsius = (5.0/9.0) * (fahr - 32);
        printf("%3.0f\t%6.1f\n",fahr,celsius);
        fahr = fahr + step;
    }

}
```
## 练习1-4
> 摄氏温度转换为华氏温度
```
#include <stdio.h>

int main(void)
{
    float fahr,celsius;
    int lower,upper,step;

    lower = 0;   /*温度表的下限*/
    upper = 300;  /*温度表的上限*/
    step = 20;  /*步长*/
    printf("----温度转换表----\n");
    printf("-Celsius-Fahr-\n");
    celsius = lower;
    while (celsius <= upper){
        fahr = celsius/(5.0/9.0) + 32;
        printf("%3.0f\t%6.1f\n",celsius,fahr);
        celsius = celsius + step;
    }

}
```
