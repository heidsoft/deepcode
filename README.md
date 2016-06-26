# deepcode
深入理解计算机系统



```
[root@localhost deepcode]# gcc -O1 -S code.c 
[root@localhost deepcode]# ls
README.md  code.c  code.s
[root@localhost deepcode]# gcc -O1 -c code.c 
[root@localhost deepcode]# ls
README.md  code.c  code.o  code.s
[root@localhost deepcode]# obj
objcopy  objdump  
[root@localhost deepcode]# objdump -d code.o

code.o:     file format elf32-i386


Disassembly of section .text:

00000000 <sum>:
   0:	55                   	push   %ebp
   1:	89 e5                	mov    %esp,%ebp
   3:	8b 45 0c             	mov    0xc(%ebp),%eax
   6:	03 45 08             	add    0x8(%ebp),%eax
   9:	01 05 00 00 00 00    	add    %eax,0x0
   f:	5d                   	pop    %ebp
  10:	c3                   	ret    
[root@localhost deepcode]# 
```
