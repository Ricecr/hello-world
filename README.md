# 编译过程

```
#include <stdio.h>

int main()
{
	/* 我的第一个 C 程序 */
	printf("Hello, World! \n");

	return 0;
}
```

使用如下命令一步到位：

```
gcc HelloWorld.c -o HelloWorld
./HelloWorld
```

输出如下：

```
Hello, World!
```

## 预处理阶段

在该阶段，编译器将上述代码中的`stdio.h`编译进来，并且用户可以使用`gcc`的选项`-E`进行查看，该选项的作用是让`gcc`在预处理结束后停止编译过程。

```
gcc -E HelloWorld.c -o HelloWorld.i
```

## 编译阶段

编译阶段，在这个阶段中，`gcc`首先要检查代码的规范性、是否有语法错误等，以确定代码的实际要做的工作，在检查无误后，`gcc`把代码翻译成汇编语言。用户可以使用`-S`选项来进行查看，该选项只进行编译而不进行汇编，生成汇编代码。 

```
gcc -S HelloWorld.i -o HelloWorld.s
```

## 汇编阶段

使用选项`-c`，将汇编代码已转化为`.o`的二进制目标代码 。

```
gcc -c HelloWorld.s -o HelloWorld.o
```

## 链接阶段

在成功编译之后，就进入了链接阶段。完成了链接之后，`gcc`就可以生成可执行文件 。

```
gcc HelloWorld.o -o HelloWorldDD
./HelloWorldDD
```

输出如下：

```
Hello, World!
```



# <!--hello-world-->

<!--I come here for myself.-->

<!--长夜漫长，还好`我`并不孤独。-->


<!--This is because of the sincere heart.-->


<!--寓言十九，重言十七，卮言日出，和以天倪。-->

<!--寄寓的言论十句有九句让人相信，-->

<!--引用前辈圣哲的言论十句有七句让人相信，-->

<!--随心表达、无有成见的言论天天变化更新，-->

<!--跟自然的区分相吻合。-->