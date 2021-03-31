# Crackme0x02
## Description

If x/s 0x804856c is used we get input format is "%d" we get following lines if disassemble main is used before compare statement.
   0x0804842b <+71>:	mov    DWORD PTR [ebp-0x8],0x5a
   0x08048432 <+78>:	mov    DWORD PTR [ebp-0xc],0x1ec
   0x08048439 <+85>:	mov    edx,DWORD PTR [ebp-0xc]
   0x0804843c <+88>:	lea    eax,[ebp-0x8]
   0x0804843f <+91>:	add    DWORD PTR [eax],edx
   0x08048441 <+93>:	mov    eax,DWORD PTR [ebp-0x8]
   0x08048444 <+96>:	imul   eax,DWORD PTR [ebp-0x8]
   0x08048448 <+100>:	mov    DWORD PTR [ebp-0xc],eax
   0x0804844b <+103>:	mov    eax,DWORD PTR [ebp-0x4]

1. ebp-0x8=90 in decimal
2. ebp-0xc=492 in decimal
3. edx=492
4. eax=ebp-0x8
5. ebp-0x8=90+492=582
6. eax=582
7. eax=582*582=338724
8. ebp-0xc=338724
9. eax=given input value

So our input value is compared with 338724 and 338724 is our password 
```
338724
```
