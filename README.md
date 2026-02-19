# javaz

[program-1 wap to print and input int](#p-1)

[program-2 wap to calculate m,cm,mm](#p-2)
## p-1
## p-2
```

import java.util.Scanner;

public class lalala {

   
    public static void main(String[] args) {
        dumb d1=new dumb();
        dumb d2=new dumb();
        d1.input();
        d1.proc();
        d1.output();
        System.out.println("Jashika");      // TODO code application logic here
    }
    
}
class dumb{
    int a;
    int b;
    void input(){
    Scanner sc=new Scanner(System.in);
    System.out.print("Entr");
    a=sc.nextInt();
    
}
     void proc(){
     a=a*2;
     }
void output(){
System.out.println("a="+a);
}    
}
```

<img width="518" height="127" alt="image" src="https://github.com/user-attachments/assets/09e4160a-b65b-460d-9258-0f284cc69db9" />


```

import java.util.Scanner;

public class zeee {
    public static void main(String[] args) {
        abs a1=new abs();
        abs a2=new abs();
        abs a3=new abs();
        a1.input();
        a2.input();
        a3.add(a1,a2);
        a3.output();
}
}
class abs{
int m;
int cm;
int mm;
void input(){
    Scanner sc=new Scanner(System.in);
    System.out.print("Entr");
    m=sc.nextInt();
    cm=sc.nextInt();
    mm=sc.nextInt();
      }
void output(){
  System.out.print("m="+m);
  System.out.print("cm="+cm);
  System.out.print("mm="+mm);
}
void add(abs a1, abs a2){
    m=a1.m+a2.m;
    cm=a1.cm+a2.cm;
    mm=a1.mm+a2.mm;
    if(mm>=10){
        cm+=1;
        mm-=10;
    }
    if(cm>=100){
        m+=1;
        cm-=100;
    }
    
}
}
```
<img width="433" height="155" alt="image" src="https://github.com/user-attachments/assets/f526eb26-3ad9-48ab-a379-654b69be0a1d" />

