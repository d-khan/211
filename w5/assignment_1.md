# This is heading 1
## This is heading 2
### This is heading 3
Please check my code.  
```
section .text
   global _start          ;must be declared for linker (gcc)
	
_start:                   ;tell linker entry point
   mov	edx,1		  ;message length
   mov	ecx,choice        ;message to write
   mov	ebx,1		  ;file descriptor (stdout)
   mov	eax,4		  ;system call number (sys_write)
   int	0x80		  ;call kernel

   mov	eax,1		  ;system call number (sys_exit)
   int	0x80		  ;call kernel

; the following section is for data

section .data
choice DB 'y'
```

This is my inline code `add eax,0`

```python
print("Hello World")
mov eax, 0
```



