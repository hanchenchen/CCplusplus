# 读取字符串函数 [string] [char *]

| 读取函数 | gets | fgets | scanf | getline | cin    |
| -------- | ---- | ----- | ----- | ------- | ------ |
| 所用时间 | 72ms | 76ms  | 960ms | 2189ms  | 2275ms |

1. `gets`已被`c++11`废弃

2.  `fgets(s,n,stdin)`

   ```c++
   char s[100];
   char *s=(char *)malloc(100*sizeof(char));
   char *s;//❌，必须要分配空间后才能使用fgets
   fgets(s,100,stdin);//n>输入长度
   ```

   读取到`'\n'`，或读取了n-1个字符时，停止🤚，并在末尾添加`'\0'`

   ```c++
   /*
   example:
   123abc 
   */
   //1
   char s[5];
   fgets(s,5,fp);
   //s={'1','2','3','a','\0'}
   //2
   char s[10];
   fgets(s,10,fp);
   //s={'1','2','3','a','b','c','\n','\0'};
   ```

3. `getline(cin,s)`

   ```c++
   string s;
   ```

4. 1





##### Reference

[C语言中scanf、gets、fgets，C++中cin、getline读取字符串的效率比较][https://blog.csdn.net/richenyunqi/article/details/89203826]

[C语言文件操作之fgets（）][https://blog.csdn.net/daiyutage/article/details/8540932]

