# I3a4dam's Plain sight
https://crackmes.one/crackme/6513567328b5870bef263329

## First run
+ unzip the binary (using 7z)
```
7z x <zipname>.zip
```
+ if there are no execute permissions, you can try `chmod +x <binaryname>`
+ let's run this
  
![image](https://github.com/user-attachments/assets/75e69e44-2369-45fa-ac33-a4f354d49af1)

## Static analysis
+ Open the same file in Ghidra & navigate to the main section

![image](https://github.com/user-attachments/assets/36cda2e0-03e0-460e-82e8-9455991278d6)

here's the decompiled output for the main function
```
int main(void){
Login();
return 0;
}
```
Now, let's navigate to the Login function definition by double clicking over it

This is the decompilation before

![image](https://github.com/user-attachments/assets/20c09744-0b83-45b6-bb6b-cc42b2764daa)

This is the decompilation after some edits

![image](https://github.com/user-attachments/assets/7103ac63-3a40-4658-b047-6670ff1fbcc3)

+ we can clearly infer that the string "do_not_hardcode" is being compared with our input. Hence this is the password

![image](https://github.com/user-attachments/assets/7ee1b30d-28b1-42bc-addb-661607beab62)
