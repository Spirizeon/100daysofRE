# Deroxs's Find a password
https://crackmes.one/crackme/6640f06b6b8bd8ddfe33c826

![image](https://github.com/user-attachments/assets/e0ac2294-62ef-480e-a530-73e3fb9972c1)

## how to crack
+ Open the file up in x64DBG
+ Search for the `strcmp` in intermodular calls for all modules
+ Set breakpoint at `0000000000402081 | E8 7A230000              | call <JMP.&strcmp>                      |`
+ Run through the breakpoints till the password is accepted
+ Check register values
  
![image](https://github.com/user-attachments/assets/6264b457-a0d0-4bea-b248-a70fdedf9d1b)
+ In  `00000000004021FB | 48:39D1                  | cmp rcx,rdx                             | rcx:"112233", rdx:"ll$_zor0c%7^"`, we have our password being compared to `rdx`'s value
+ Check that string on the program...
+ Cracked!

![image](https://github.com/user-attachments/assets/fd7067a8-6bad-45a2-b27f-0b4cae717995)
