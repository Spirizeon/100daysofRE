# TheFakeKing's Basic Crackme ConsoleBased
https://crackmes.one/crackme/6492036733c5d43938913a58

## Steps to crack
+ Unzip the crackme
+ Start analysis in Ghidra, navigate to main function

```
int __cdecl main(int _Argc,char **_Argv,char **_Env)

{
  undefined uVar1;
  undefined8 unaff_RBP;
  undefined uVar2;
  undefined in_R9B;
  
  uVar2 = SUB81(_Env,0);
  uVar1 = SUB81(_Argv,0);
  __main();
  do {
    GetPassword((char)_Argc,uVar1,uVar2,in_R9B,(char)unaff_RBP);
  } while( true );
```

+ `ErhwHwrhrwWhrwwHwhr` is the password

```
/* GetPassword() */

void GetPassword(undefined param_1,undefined param_2,undefined param_3,undefined param_4,
                undefined1 param_5)

{
  bool bVar1;
  uint uVar2;
  longlong *local_38 [5];
  
  system("cls");
  std::operator<<((longlong *)&std::cout,"Input a password\n>");
  std::__cxx11::basic_string<>::basic_string((longlong *)local_38);
  bVar1 = std::operator==((basic_string<> *)local_38,"ErhwHwrhrwWhrwwHwhr");
  if (bVar1) {
    std::operator<<((longlong *)&std::cout,"Vaild Password\n<Enter anything to Retry>");
  }
  std::operator>>(&std::cin,local_38);
  uVar2 = std::operator!=((basic_string<> *)local_38,"ErhwHwrhrwWhrwwHwhr");
  if ((char)uVar2 != '\0') {
    std::operator<<((longlong *)&std::cout,"Invaild Password\n<Enter anything to Retry>");
  }
  std::operator>>(&std::cin,local_38);
  std::__cxx11::basic_string<>::~basic_string((basic_string<> *)local_38);
  return;
}
```
+ here "ErhwHwrhrwWhrwwHwhr" is the password
+ cracked
