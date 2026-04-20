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

```
import java.util.Scanner;

class Calc {
    int a, b;

    void input() {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter first number: ");
        a = sc.nextInt();
        System.out.print("Enter second number: ");
        b = sc.nextInt();
    }

    void add() {
        System.out.println("Addition = " + (a + b));
    }

    void sub() {
        System.out.println("Subtraction = " + (a - b));
    }

    void mul() {
        System.out.println("Multiplication = " + (a * b));
    }

    void div() {
        System.out.println("Division = " + (a / b));
    }
}

public class calculator  {
    public static void main(String[] args) {
        Calc obj = new Calc();
        obj.input();
        obj.add();
        obj.sub();
        obj.mul();
        obj.div();
    }
}

```
<img width="399" height="196" alt="image" src="https://github.com/user-attachments/assets/13bd6b82-55fd-4978-bd28-dc369190398d" />

```
import java.util.Scanner;

class Dist {
    int meter, cm, mm;

    void input() {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter meter: ");
        meter = sc.nextInt();

        System.out.print("Enter centimeter: ");
        cm = sc.nextInt();

        System.out.print("Enter millimeter: ");
        mm = sc.nextInt();
    }

    void add(Dist d1, Dist d2) {
        mm = d1.mm + d2.mm;
        cm = d1.cm + d2.cm + (mm / 10);
        mm = mm % 10;

        meter = d1.meter + d2.meter + (cm / 100);
        cm = cm % 100;
    }

    void display() {
        System.out.println("Total Distance = " + meter + " m " + cm + " cm " + mm + " mm");
    }
}

public class distance {
    public static void main(String[] args) {

        Dist d1 = new Dist();
        Dist d2 = new Dist();
        Dist d3 = new Dist();

        System.out.println("Enter First Distance");
        d1.input();

        System.out.println("Enter Second Distance");
        d2.input();

        d3.add(d1, d2);

        d3.display();
    }
}
```
<img width="415" height="232" alt="image" src="https://github.com/user-attachments/assets/f0663804-05e8-4003-95a3-5fb81568720a" />

```
import java.util.Scanner;

class Distt {
    int meter, cm;

    void input() {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter meter: ");
        meter = sc.nextInt();

        System.out.print("Enter centimeter: ");
        cm = sc.nextInt();
    }

    void add(Distt d1, Distt d2) {
        cm = d1.cm + d2.cm;
        meter = d1.meter + d2.meter + (cm / 100);
        cm = cm % 100;
    }

    void display() {
        System.out.println("Total Distance = " + meter + " m " + cm + " cm");
    }
}

public class distance2 {
    public static void main(String[] args) {

        Distt d1 = new Distt();
        Distt d2 = new Distt();
        Distt d3 = new Distt();

        System.out.println("Enter First Distance");
        d1.input();

        System.out.println("Enter Second Distance");
        d2.input();

        d3.add(d1, d2);

        d3.display();
    }
}
```
<img width="408" height="234" alt="image" src="https://github.com/user-attachments/assets/a72329bb-0b37-489c-8c9d-23416903cddf" />

```
import java.util.Scanner;

class Timee {
    int hour, minute, second;

    void input() {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter hours: ");
        hour = sc.nextInt();

        System.out.print("Enter minutes: ");
        minute = sc.nextInt();

        System.out.print("Enter seconds: ");
        second = sc.nextInt();
    }

    void add(Timee t1, Timee t2) {
        second = t1.second + t2.second;
        minute = t1.minute + t2.minute + (second / 60);
        second = second % 60;

        hour = t1.hour + t2.hour + (minute / 60);
        minute = minute % 60;
    }

    void display() {
        System.out.println("Total Time = " + hour + " hr " + minute + " min " + second + " sec");
    }
}

public class time {
    public static void main(String[] args) {

        Timee t1 = new Timee();
        Timee t2 = new Timee();
        Timee t3 = new Timee();

        System.out.println("Enter First Time");
        t1.input();

        System.out.println("Enter Second Time");
        t2.input();

        t3.add(t1, t2);

        t3.display();
    }
}
```
<img width="399" height="246" alt="image" src="https://github.com/user-attachments/assets/8df2f3ec-5fa8-406b-91d0-eed2adc27d25" />

```
import java.util.Scanner;

class Timz {
    int hour, minute;

    void input() {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter hours: ");
        hour = sc.nextInt();

        System.out.print("Enter minutes: ");
        minute = sc.nextInt();
    }

    void add(Timz t1, Timz t2) {
        minute = t1.minute + t2.minute;
        hour = t1.hour + t2.hour + (minute / 60);
        minute = minute % 60;
    }

    void display() {
        System.out.println("Total Time = " + hour + " hr " + minute + " min");
    }
}

public class time2 {
    public static void main(String[] args) {

        Timz t1 = new Timz();
        Timz t2 = new Timz();
        Timz t3 = new Timz();

        System.out.println("Enter First Time");
        t1.input();

        System.out.println("Enter Second Time");
        t2.input();

        t3.add(t1, t2);

        t3.display();
    }
}
```
<img width="378" height="213" alt="image" src="https://github.com/user-attachments/assets/c76f0d2f-12a2-4776-a93e-b35754527d38" />

```
