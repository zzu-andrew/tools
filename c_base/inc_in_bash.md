## 在`Makefile`中添加头文

我们常这样写C程序：

```c
#inlcude <stdio.h>


int main(int argc, char *argv[])
{
    printf("Hello WOrld\n");



    return 0;
}
```
如果你的程序是工程性质的，或者所有的程序都使用同一个头文件，那你没有使用在Makefile中添加头文件的必要，但是如果你是经常教程或者学习时使用做学习笔记，这个功能就非常有用了，我们只需要在Makefile中添加需要的头文件就可以达到在c源文件的加头文件的同样目的。

在Makefile中添加头文件，其实是利用了gcc的-include选项，只需在编译程序的时候指定 -include xxx.h即同等于在源文件中使用`#include <xxx.h>`

在Makefile中指定头文件的程序可以像下面这样写：

```c
int main(int argc, char *argv[])
{
    printf("Hello WOrld\n");



    return 0;
}
```
编译的时候使用`gcc -include stdio.h inc_in_bash.c -o  inc_in_bash`
其中的`-include stdio.h` ==> `#include <stdio.h>`
