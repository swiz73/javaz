# javaz


[program-1 add and mul using onjects and claases](#prog1)   
[program-2 Write a class for addition of two distance where each distance is given in m,cm,mm.](#prog2)  
[program-3 Similarly, test the result by creation of object in main class where each distance is given 
in m,cm.](#prog3)  
[program-4 Similarly for time given in hours, min and seconds.](#prog4)  
[program-5 Time given in hours and minutes.](#prog5)   
[program-6 Collect the code from internet for any five programs of c language. (Fact, armstrong, palindrome, Fibonacci, pattern).](#prog6)   
[program-7 Write a class that is having four method for 1-dimensional array. (Input, output 1,out2, reverse).](#prog7) 
[program-8 write a class with multiple methods to perform matrix operations (transpose, addition, sum of rows, sum of columns, sum of diagonal).](#prog8)  
[program-9 Write a program using three classes to print 1-100 ,1-100,1-100 with and without thread and analyse the output and repeat the same program using runnable interface.](#prog9)  
[program-10 Using the concept of multithreading the output of all three threads must be synchronised (use join method).](#prog10)   
[program-11 Addition of 2 numbers using swing.](#prog11)   
[program-12 Make a registration form with 10 elements and send the data into database (use jdbc connectivity)](#prog12)  
[program-13 Make one calculator in swing.](#prog13)   
[program-14 Matrix Addition using swing class.](#prog14)   
[program-15 Create one jframe apply 10 buttons on that after clicking on each button a new 
structure is created.(Circle, oval rectangle, etc ....)](#prog15)   
[program-16 Just using mouse Event create a frame like paint brush with selection of colour and width .](#prog16)   
[program-17 Create a package of any 5 classes of your choice and import it.](#prog17)    
[program-18 Create one package and sub package  import and test it .](#prog18)   
[program-19 Create one small array of size 5 apply array out of bounds exception using try catch give a proper message in catch and demonstrate the exception exactly in the same fashion demonstrate arithmetic exception .](#prog19)    
[program-20 To test the range of age of one student.write a program using user defined exception.](#prog20)   
[program-21 File Handling Programs (given in the PPT)](#prog21)    
[program-22 Inheritance Programs, using interface and abstract classes.](#prog22)   

## prog1
## prog2 
## prog3 
## prog4
## prog5
## prog6 
## prog7
## prog8
## prog9 
## prog10 
## prog11
## prog12
## prog13
## prog14
## prog15
## prog16
## prog17
## prog18 
## prog19
## prog20
## prog21
## prog22 

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
import java.util.Scanner;

class Factorial {
    
    int findFactorial(int n) {
        int fact = 1;

        for(int i = 1; i <= n; i++) {
            fact = fact * i;
        }

        return fact;
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Factorial obj = new Factorial();

        System.out.print("Enter a number: ");
        int n = sc.nextInt();

        System.out.println("Factorial = " + obj.findFactorial(n));
    }
}
```
<img width="377" height="136" alt="image" src="https://github.com/user-attachments/assets/62f9f561-cf49-4e4d-bd0b-2923c605166a" />

```
import java.util.Scanner;

class Armstrong {

    void checkArmstrong(int num) {
        int original = num, rem, result = 0;

        while(num != 0) {
            rem = num % 10;
            result = result + (rem * rem * rem);
            num = num / 10;
        }

        if(original == result)
            System.out.println("Armstrong Number");
        else
            System.out.println("Not Armstrong Number");
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Armstrong obj = new Armstrong();

        System.out.print("Enter a number: ");
        int n = sc.nextInt();

        obj.checkArmstrong(n);
    }
}
```
<img width="371" height="103" alt="image" src="https://github.com/user-attachments/assets/d0c454a8-85c1-431a-9a4e-8983f82875f8" />

```
import java.util.Scanner;

class Palindrome {

    void checkPalindrome(int num) {
        int original = num, reverse = 0, rem;

        while(num != 0) {
            rem = num % 10;
            reverse = reverse * 10 + rem;
            num = num / 10;
        }

        if(original == reverse)
            System.out.println("Palindrome Number");
        else
            System.out.println("Not Palindrome Number");
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Palindrome obj = new Palindrome();

        System.out.print("Enter a number: ");
        int n = sc.nextInt();

        obj.checkPalindrome(n);
    }
}
```
<img width="421" height="125" alt="image" src="https://github.com/user-attachments/assets/5320815d-02d8-41fb-b789-5383b8c96f6c" />

```
import java.util.Scanner;

class Fibonacci {

    void printSeries(int n) {
        int a = 0, b = 1, c;

        for(int i = 1; i <= n; i++) {
            System.out.print(a + " ");
            c = a + b;
            a = b;
            b = c;
        }
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Fibonacci obj = new Fibonacci();

        System.out.print("Enter number of terms: ");
        int n = sc.nextInt();

        obj.printSeries(n);
    }
}
```
<img width="466" height="127" alt="image" src="https://github.com/user-attachments/assets/1425e709-39c4-443b-970c-30dab5ff1a69" />

```
import java.util.Scanner;

class StarPattern {

    void printPattern(int n) {

        for(int i = 1; i <= n; i++) {

            // Print spaces
            for(int j = 1; j <= n - i; j++) {
                System.out.print(" ");
            }

            // Print stars
            for(int k = 1; k <= (2 * i - 1); k++) {
                System.out.print("*");
            }

            System.out.println();
        }
    }

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);
        StarPattern obj = new StarPattern();

        System.out.print("Enter number of rows: ");
        int n = sc.nextInt();

        obj.printPattern(n);
    }
}
```

<img width="383" height="205" alt="image" src="https://github.com/user-attachments/assets/df307d03-5213-4dfb-bbf1-0f8c75cdecbe" />

```
import java.util.Scanner;

class ArrayOperation {
    int a[] = new int[5];

    void input() {
        Scanner sc = new Scanner(System.in);

        System.out.println("Enter 5 elements:");

        for(int i = 0; i < 5; i++) {
            a[i] = sc.nextInt();
        }
    }

    void out1() {
        System.out.println("Original Array:");

        for(int i = 0; i < 5; i++) {
            System.out.print(a[i] + " ");
        }

        System.out.println();
    }

    void reverse() {
        for(int i = 0; i < 5 / 2; i++) {
            int temp = a[i];
            a[i] = a[4 - i];
            a[4 - i] = temp;
        }
    }

    void out2() {
        System.out.println("Reversed Array:");

        for(int i = 0; i < 5; i++) {
            System.out.print(a[i] + " ");
        }

        System.out.println();
    }
}

public class array {
    public static void main(String[] args) {

        ArrayOperation obj = new ArrayOperation();

        obj.input();
        obj.out1();
        obj.reverse();
        obj.out2();
    }
}
```
<img width="415" height="221" alt="image" src="https://github.com/user-attachments/assets/4f43dbac-7f42-4c64-af5c-436f620bb243" />

```
import java.util.Scanner;

class MatrixOperation {
    int a[][] = new int[3][3];
    int b[][] = new int[3][3];
    int c[][] = new int[3][3];

    void input() {
        Scanner sc = new Scanner(System.in);

        System.out.println("Enter elements of First Matrix:");
        for(int i = 0; i < 3; i++) {
            for(int j = 0; j < 3; j++) {
                a[i][j] = sc.nextInt();
            }
        }

        System.out.println("Enter elements of Second Matrix:");
        for(int i = 0; i < 3; i++) {
            for(int j = 0; j < 3; j++) {
                b[i][j] = sc.nextInt();
            }
        }
    }

    void addition() {
        System.out.println("Addition of Matrices:");

        for(int i = 0; i < 3; i++) {
            for(int j = 0; j < 3; j++) {
                c[i][j] = a[i][j] + b[i][j];
                System.out.print(c[i][j] + " ");
            }
            System.out.println();
        }
    }

    void transpose() {
        System.out.println("Transpose of First Matrix:");

        for(int i = 0; i < 3; i++) {
            for(int j = 0; j < 3; j++) {
                System.out.print(a[j][i] + " ");
            }
            System.out.println();
        }
    }

    void rowSum() {
        System.out.println("Sum of Rows:");

        for(int i = 0; i < 3; i++) {
            int sum = 0;
            for(int j = 0; j < 3; j++) {
                sum = sum + a[i][j];
            }
            System.out.println("Row " + (i+1) + " = " + sum);
        }
    }

    void columnSum() {
        System.out.println("Sum of Columns:");

        for(int j = 0; j < 3; j++) {
            int sum = 0;
            for(int i = 0; i < 3; i++) {
                sum = sum + a[i][j];
            }
            System.out.println("Column " + (j+1) + " = " + sum);
        }
    }

    void diagonalSum() {
        int sum = 0;

        for(int i = 0; i < 3; i++) {
            sum = sum + a[i][i];
        }

        System.out.println("Sum of Diagonal = " + sum);
    }
}

public class matrix {
    public static void main(String[] args) {

        MatrixOperation obj = new MatrixOperation();

        obj.input();
        obj.addition();
        obj.transpose();
        obj.rowSum();
        obj.columnSum();
        obj.diagonalSum();
    }
}

```
<img width="498" height="670" alt="image" src="https://github.com/user-attachments/assets/9cc8bbcd-8a30-4577-923b-29fc85e01fea" />

```
class A extends Thread {
    public void run() {
        for(int i=1; i<=100; i++)
            System.out.println("A : " + i);
    }
}

class B extends Thread {
    public void run() {
        for(int i=1; i<=100; i++)
            System.out.println("B : " + i);
    }
}

class C extends Thread {
    public void run() {
        for(int i=1; i<=100; i++)
            System.out.println("C : " + i);
    }
}

public class ThreadWith {
    public static void main(String[] args) {
        A t1 = new A();
        B t2 = new B();
        C t3 = new C();

        t1.start();
        t2.start();
        t3.start();
    }
}
```
<img width="382" height="594" alt="image" src="https://github.com/user-attachments/assets/a6241a79-8bd0-41b3-a434-92e60c34ce48" />

```
class X implements Runnable {
    public void run() {
        for(int i=1; i<=100; i++)
            System.out.println("X : " + i);
    }
}

class Y implements Runnable {
    public void run() {
        for(int i=1; i<=100; i++)
            System.out.println("Y : " + i);
    }
}

class Z implements Runnable {
    public void run() {
        for(int i=1; i<=100; i++)
            System.out.println("Z : " + i);
    }
}

public class RunnableWith {
    public static void main(String[] args) {
        Thread t1 = new Thread(new X());
        Thread t2 = new Thread(new Y());
        Thread t3 = new Thread(new Z());

        t1.start();
        t2.start();
        t3.start();
    }
}
```
<img width="417" height="425" alt="image" src="https://github.com/user-attachments/assets/d84a2436-67f6-4f16-b1d0-c93e1aadda20" />

```
class X implements Runnable {
    public void run() {
        for(int i=1; i<=100; i++)
            System.out.println("X : " + i);
    }
}

class Y implements Runnable {
    public void run() {
        for(int i=1; i<=100; i++)
            System.out.println("Y : " + i);
    }
}

class Z implements Runnable {
    public void run() {
        for(int i=1; i<=100; i++)
            System.out.println("Z : " + i);
    }
}

public class RunnableWithout {
    public static void main(String[] args) {
        X obj1 = new X();
        Y obj2 = new Y();
        Z obj3 = new Z();

        obj1.run();
        obj2.run();
        obj3.run();
    }
}
```
<img width="384" height="429" alt="image" src="https://github.com/user-attachments/assets/3d31c30d-b247-4736-a6ef-2959f992556c" />

```
class A extends Thread {
    public void run() {
        for(int i = 1; i <= 100; i++) {
            System.out.println("A : " + i);
        }
    }
}

class B extends Thread {
    public void run() {
        for(int i = 1; i <= 100; i++) {
            System.out.println("B : " + i);
        }
    }
}

class C extends Thread {
    public void run() {
        for(int i = 1; i <= 100; i++) {
            System.out.println("C : " + i);
        }
    }
}
    public class JoinThread {
    public static void main(String[] args) throws InterruptedException {

        A t1 = new A();
        B t2 = new B();
        C t3 = new C();

        t1.start();
        t1.join();

        t2.start();
        t2.join();

        t3.start();
        t3.join();
    }
}
```
<img width="388" height="435" alt="image" src="https://github.com/user-attachments/assets/703e0ab4-f963-42ef-a94e-8504947e6f67" />

```
import javax.swing.*;
import java.awt.event.*;

public class AdditionSwing extends JFrame implements ActionListener
{
    JLabel l1, l2, l3;
    JTextField t1, t2, t3;
    JButton b1;

    AdditionSwing()
    {
        l1 = new JLabel("Enter First Number:");
        l2 = new JLabel("Enter Second Number:");
        l3 = new JLabel("Result:");

        t1 = new JTextField();
        t2 = new JTextField();
        t3 = new JTextField();

        b1 = new JButton("Add");

        l1.setBounds(50, 50, 150, 30);
        t1.setBounds(200, 50, 150, 30);

        l2.setBounds(50, 100, 150, 30);
        t2.setBounds(200, 100, 150, 30);

        l3.setBounds(50, 150, 150, 30);
        t3.setBounds(200, 150, 150, 30);

        b1.setBounds(150, 220, 100, 30);

        add(l1);
        add(l2);
        add(l3);
        add(t1);
        add(t2);
        add(t3);
        add(b1);

        b1.addActionListener(this);

        setSize(450, 350);
        setLayout(null);
        setVisible(true);
        setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
    }

    public void actionPerformed(ActionEvent e)
    {
        int a, b, c;

        a = Integer.parseInt(t1.getText());
        b = Integer.parseInt(t2.getText());

        c = a + b;

        t3.setText(String.valueOf(c));
    }

    public static void main(String[] args)
    {
        new AdditionSwing();
    }
}
```
<img width="453" height="347" alt="image" src="https://github.com/user-attachments/assets/9995557c-474c-403d-99d6-9bc053910e5c" />

```
import javax.swing.*;
import java.awt.event.*;
import java.sql.*;

public class RegistrationForm extends JFrame implements ActionListener
{
    JLabel l1,l2,l3,l4,l5,l6,l7,l8,l9,l10;
    JTextField t1,t2,t3,t4,t5,t6,t7,t8;
    JPasswordField p1;
    JRadioButton r1,r2;
    JButton b1;
    ButtonGroup bg;

    RegistrationForm()
    {
        l1 = new JLabel("Name");
        l2 = new JLabel("Father Name");
        l3 = new JLabel("Email");
        l4 = new JLabel("Password");
        l5 = new JLabel("Gender");
        l6 = new JLabel("Mobile");
        l7 = new JLabel("Address");
        l8 = new JLabel("City");
        l9 = new JLabel("State");
        l10 = new JLabel("Pincode");

        t1 = new JTextField();
        t2 = new JTextField();
        t3 = new JTextField();
        t4 = new JTextField();
        t5 = new JTextField();
        t6 = new JTextField();
        t7 = new JTextField();
        t8 = new JTextField();

        p1 = new JPasswordField();

        r1 = new JRadioButton("Male");
        r2 = new JRadioButton("Female");

        bg = new ButtonGroup();
        bg.add(r1);
        bg.add(r2);

        b1 = new JButton("Register");

        l1.setBounds(50,30,100,30);
        t1.setBounds(180,30,150,30);

        l2.setBounds(50,70,100,30);
        t2.setBounds(180,70,150,30);

        l3.setBounds(50,110,100,30);
        t3.setBounds(180,110,150,30);

        l4.setBounds(50,150,100,30);
        p1.setBounds(180,150,150,30);

        l5.setBounds(50,190,100,30);
        r1.setBounds(180,190,70,30);
        r2.setBounds(260,190,80,30);

        l6.setBounds(50,230,100,30);
        t4.setBounds(180,230,150,30);

        l7.setBounds(50,270,100,30);
        t5.setBounds(180,270,150,30);

        l8.setBounds(50,310,100,30);
        t6.setBounds(180,310,150,30);

        l9.setBounds(50,350,100,30);
        t7.setBounds(180,350,150,30);

        l10.setBounds(50,390,100,30);
        t8.setBounds(180,390,150,30);

        b1.setBounds(140,450,120,30);

        add(l1); add(t1);
        add(l2); add(t2);
        add(l3); add(t3);
        add(l4); add(p1);
        add(l5); add(r1); add(r2);
        add(l6); add(t4);
        add(l7); add(t5);
        add(l8); add(t6);
        add(l9); add(t7);
        add(l10); add(t8);
        add(b1);

        b1.addActionListener(this);

        setSize(450,550);
        setLayout(null);
        setVisible(true);
        setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
    }

    public void actionPerformed(ActionEvent e)
    {
        String name = t1.getText();
        String fname = t2.getText();
        String email = t3.getText();
        String pass = String.valueOf(p1.getPassword());
        String gender = "";

        if(r1.isSelected())
            gender = "Male";
        else
            gender = "Female";

        String mobile = t4.getText();
        String address = t5.getText();
        String city = t6.getText();
        String state = t7.getText();
        String pincode = t8.getText();

        try
        {
            try {
                Class.forName("com.mysql.cj.jdbc.Driver");
            } catch (ClassNotFoundException ex) {
                System.getLogger(RegistrationForm.class.getName()).log(System.Logger.Level.ERROR, (String) null, ex);
            }

            Connection con = null;
            try {
                con = DriverManager.getConnection(
                        "jdbc:mysql://localhost:3306/studentdb",
                        "root",
                        "password"
                );
            } catch (SQLException ex) {
                System.getLogger(RegistrationForm.class.getName()).log(System.Logger.Level.ERROR, (String) null, ex);
            }

            PreparedStatement ps = con.prepareStatement(
                "insert into register values(?,?,?,?,?,?,?,?,?,?)"
            );

            ps.setString(1,name);
            ps.setString(2,fname);
            ps.setString(3,email);
            ps.setString(4,pass);
            ps.setString(5,gender);
            ps.setString(6,mobile);
            ps.setString(7,address);
            ps.setString(8,city);
            ps.setString(9,state);
            ps.setString(10,pincode);

            ps.executeUpdate();

            JOptionPane.showMessageDialog(this,"Registration Successful");

            con.close();
        } catch (SQLException ex) {
            System.getLogger(RegistrationForm.class.getName()).log(System.Logger.Level.ERROR, (String) null, ex);
        }
    }

    public static void main(String[] args)
    {
        new RegistrationForm();
    }
}
```
<img width="448" height="544" alt="image" src="https://github.com/user-attachments/assets/c0da465c-e398-4dc9-b8fe-3ab309cf6a08" />

```
import javax.swing.*;
import java.awt.event.*;

public class CalculatorSwing extends JFrame implements ActionListener
{
    JLabel l1, l2, l3;
    JTextField t1, t2, t3;
    JButton b1, b2, b3, b4;

    CalculatorSwing()
    {
        l1 = new JLabel("First Number");
        l2 = new JLabel("Second Number");
        l3 = new JLabel("Result");

        t1 = new JTextField();
        t2 = new JTextField();
        t3 = new JTextField();

        b1 = new JButton("Add");
        b2 = new JButton("Sub");
        b3 = new JButton("Mul");
        b4 = new JButton("Div");

        l1.setBounds(50,50,100,30);
        t1.setBounds(170,50,150,30);

        l2.setBounds(50,100,100,30);
        t2.setBounds(170,100,150,30);

        l3.setBounds(50,150,100,30);
        t3.setBounds(170,150,150,30);

        b1.setBounds(30,220,80,30);
        b2.setBounds(120,220,80,30);
        b3.setBounds(210,220,80,30);
        b4.setBounds(300,220,80,30);

        add(l1); add(t1);
        add(l2); add(t2);
        add(l3); add(t3);

        add(b1); add(b2); add(b3); add(b4);

        b1.addActionListener(this);
        b2.addActionListener(this);
        b3.addActionListener(this);
        b4.addActionListener(this);

        setSize(450,350);
        setLayout(null);
        setVisible(true);
        setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
    }

    public void actionPerformed(ActionEvent e)
    {
        int a = Integer.parseInt(t1.getText());
        int b = Integer.parseInt(t2.getText());
        int c = 0;

        if(e.getSource() == b1)
            c = a + b;

        if(e.getSource() == b2)
            c = a - b;

        if(e.getSource() == b3)
            c = a * b;

        if(e.getSource() == b4)
            c = a / b;

        t3.setText(String.valueOf(c));
    }

    public static void main(String[] args)
    {
        new CalculatorSwing();
    }
}
```
<img width="447" height="346" alt="image" src="https://github.com/user-attachments/assets/7500c117-6e9b-4616-b2a6-bd1a9c5548fc" />

```
import javax.swing.*;
import java.awt.event.*;

public class MatrixAddition extends JFrame implements ActionListener
{
    JLabel l1;
    JTextField t1,t2,t3,t4,t5,t6,t7,t8;
    JButton b1;

    MatrixAddition()
    {
        l1 = new JLabel("Matrix Addition (2 x 2)");

        t1 = new JTextField();
        t2 = new JTextField();
        t3 = new JTextField();
        t4 = new JTextField();

        t5 = new JTextField();
        t6 = new JTextField();
        t7 = new JTextField();
        t8 = new JTextField();

        b1 = new JButton("Add");

        l1.setBounds(120,20,200,30);

        t1.setBounds(50,70,50,30);
        t2.setBounds(110,70,50,30);
        t3.setBounds(50,110,50,30);
        t4.setBounds(110,110,50,30);

        t5.setBounds(220,70,50,30);
        t6.setBounds(280,70,50,30);
        t7.setBounds(220,110,50,30);
        t8.setBounds(280,110,50,30);

        b1.setBounds(150,170,100,30);

        add(l1);

        add(t1); add(t2); add(t3); add(t4);
        add(t5); add(t6); add(t7); add(t8);

        add(b1);

        b1.addActionListener(this);

        setSize(420,300);
        setLayout(null);
        setVisible(true);
        setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
    }

    public void actionPerformed(ActionEvent e)
    {
        int a11 = Integer.parseInt(t1.getText());
        int a12 = Integer.parseInt(t2.getText());
        int a21 = Integer.parseInt(t3.getText());
        int a22 = Integer.parseInt(t4.getText());

        int b11 = Integer.parseInt(t5.getText());
        int b12 = Integer.parseInt(t6.getText());
        int b21 = Integer.parseInt(t7.getText());
        int b22 = Integer.parseInt(t8.getText());

        int c11 = a11 + b11;
        int c12 = a12 + b12;
        int c21 = a21 + b21;
        int c22 = a22 + b22;

        JOptionPane.showMessageDialog(this,
            "Result Matrix:\n" +
            c11 + "   " + c12 + "\n" +
            c21 + "   " + c22);
    }

    public static void main(String[] args)
    {
        new MatrixAddition();
    }
}
```
<img width="422" height="294" alt="image" src="https://github.com/user-attachments/assets/2742cf2f-039f-40c5-836c-156ef67974f0" />

```
import javax.swing.*;
import java.awt.*;
import java.awt.event.*;

class Shapes extends JFrame implements ActionListener
{
    JButton b1,b2,b3,b4,b5,b6,b7,b8,b9,b10;
    String shape="";

    Shapes()
    {
        b1=new JButton("Circle");
        b2=new JButton("Oval");
        b3=new JButton("Rectangle");
        b4=new JButton("Square");
        b5=new JButton("Line");
        b6=new JButton("Triangle");
        b7=new JButton("Arc");
        b8=new JButton("RoundRect");
        b9=new JButton("Cube");
        b10=new JButton("Ellipse");

        b1.setBounds(20,20,100,30);
        b2.setBounds(130,20,100,30);
        b3.setBounds(240,20,100,30);
        b4.setBounds(350,20,100,30);
        b5.setBounds(460,20,100,30);

        b6.setBounds(20,60,100,30);
        b7.setBounds(130,60,100,30);
        b8.setBounds(240,60,100,30);
        b9.setBounds(350,60,100,30);
        b10.setBounds(460,60,100,30);

        add(b1); add(b2); add(b3); add(b4); add(b5);
        add(b6); add(b7); add(b8); add(b9); add(b10);

        b1.addActionListener(this);
        b2.addActionListener(this);
        b3.addActionListener(this);
        b4.addActionListener(this);
        b5.addActionListener(this);
        b6.addActionListener(this);
        b7.addActionListener(this);
        b8.addActionListener(this);
        b9.addActionListener(this);
        b10.addActionListener(this);

        setSize(600,500);
        setLayout(null);
        setVisible(true);
        setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
    }

    public void actionPerformed(ActionEvent e)
    {
        if(e.getSource()==b1) shape="Circle";
        if(e.getSource()==b2) shape="Oval";
        if(e.getSource()==b3) shape="Rectangle";
        if(e.getSource()==b4) shape="Square";
        if(e.getSource()==b5) shape="Line";
        if(e.getSource()==b6) shape="Triangle";
        if(e.getSource()==b7) shape="Arc";
        if(e.getSource()==b8) shape="RoundRect";
        if(e.getSource()==b9) shape="Cube";
        if(e.getSource()==b10) shape="Ellipse";

        repaint();
    }

    public void paint(Graphics g)
    {
        super.paint(g);

        if(shape.equals("Circle"))
            g.drawOval(230,180,100,100);

        if(shape.equals("Oval"))
            g.drawOval(210,180,150,90);

        if(shape.equals("Rectangle"))
            g.drawRect(210,180,150,100);

        if(shape.equals("Square"))
            g.drawRect(230,180,100,100);

        if(shape.equals("Line"))
            g.drawLine(200,180,350,280);

        if(shape.equals("Triangle"))
        {
            g.drawLine(260,170,210,270);
            g.drawLine(260,170,310,270);
            g.drawLine(210,270,310,270);
        }

        if(shape.equals("Arc"))
            g.drawArc(210,180,150,100,0,180);

        if(shape.equals("RoundRect"))
            g.drawRoundRect(210,180,150,100,30,30);

        if(shape.equals("Cube"))
        {
            g.drawRect(210,200,100,100);
            g.drawRect(250,160,100,100);
            g.drawLine(210,200,250,160);
            g.drawLine(310,200,350,160);
            g.drawLine(310,300,350,260);
            g.drawLine(210,300,250,260);
        }

        if(shape.equals("Ellipse"))
            g.drawOval(200,190,180,90);
    }
}

public class Shape
{
    public static void main(String[] args)
    {
        new Shapes();
    }
}
```
<img width="579" height="295" alt="image" src="https://github.com/user-attachments/assets/38b45947-0160-4298-a101-02809b7f2a9a" />
<img width="560" height="293" alt="image" src="https://github.com/user-attachments/assets/1eacff76-3ee2-4688-ab98-270081393f4f" />

```
import javax.swing.*;
import java.awt.*;
import java.awt.event.*;

class PaintBrush extends JFrame implements MouseListener, MouseMotionListener
{
    int x, y, w = 3;
    Color c = Color.BLACK;

    JButton b1, b2, b3, b4, b5;

    PaintBrush()
    {
        b1 = new JButton("Red");
        b2 = new JButton("Blue");
        b3 = new JButton("Green");
        b4 = new JButton("Thin");
        b5 = new JButton("Thick");

        b1.setBounds(20,40,80,30);
        b2.setBounds(110,40,80,30);
        b3.setBounds(200,40,80,30);
        b4.setBounds(290,40,80,30);
        b5.setBounds(380,40,80,30);

        add(b1); add(b2); add(b3); add(b4); add(b5);

        b1.addActionListener(e -> c = Color.RED);
        b2.addActionListener(e -> c = Color.BLUE);
        b3.addActionListener(e -> c = Color.GREEN);

        b4.addActionListener(e -> w = 3);
        b5.addActionListener(e -> w = 10);

        addMouseListener(this);
        addMouseMotionListener(this);

        setSize(700,500);
        setLayout(null);
        setVisible(true);
        setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
    }

    public void mouseDragged(MouseEvent e)
    {
        Graphics g = getGraphics();

        g.setColor(c);
        g.fillOval(e.getX(), e.getY(), w, w);
    }

    public void mousePressed(MouseEvent e)
    {
        x = e.getX();
        y = e.getY();
    }

    public void mouseReleased(MouseEvent e) {}
    public void mouseClicked(MouseEvent e) {}
    public void mouseEntered(MouseEvent e) {}
    public void mouseExited(MouseEvent e) {}
    public void mouseMoved(MouseEvent e) {}
}

public class Paint
{
    public static void main(String[] args)
    {
        new PaintBrush();
    }
}
```
<img width="644" height="445" alt="image" src="https://github.com/user-attachments/assets/12d45576-0b11-44bc-9d57-dacb786f3713" />

```
package mypack;

class Student
{
    void show1()
    {
        System.out.println("Student Class");
    }
}

class Teacher
{
    void show2()
    {
        System.out.println("Teacher Class");
    }
}

class Employee
{
    void show3()
    {
        System.out.println("Employee Class");
    }
}

class Manager
{
    void show4()
    {
        System.out.println("Manager Class");
    }
}

class Principal
{
    void show5()
    {
        System.out.println("Principal Class");
    }
}

public class Package
{
    public static void main(String[] args)
    {
        Student s = new Student();
        Teacher t = new Teacher();
        Employee e = new Employee();
        Manager m = new Manager();
        Principal p = new Principal();

        s.show1();
        t.show2();
        e.show3();
        m.show4();
        p.show5();
    }
}
```
<img width="357" height="158" alt="image" src="https://github.com/user-attachments/assets/e2095256-a9fa-48c5-b1e9-e8a94998d848" />

```
package animals.pet;

public class cat
{
    public void sound()
    {
        System.out.println("Cat Meows");
    }
}
package animals;

import animals.pet.cat;

class Dog
{
    void sound()
    {
        System.out.println("Dog Barks");
    }
}

public class test
{
    public static void main(String args[])
    {
        Dog d = new Dog();
        cat c = new cat();

        d.sound();
        c.sound();
    }
}
```
<img width="368" height="125" alt="image" src="https://github.com/user-attachments/assets/71300101-8ad6-41e0-88eb-355f473e440f" />

```
public class Exception
{
    public static void main(String args[])
    {
        int a[] = {10,20,30,40,50};

        try
        {
            System.out.println("Array Element = " + a[7]);
        }
        catch(ArrayIndexOutOfBoundsException e)
        {
            System.out.println("Error: Array Index is Out of Bounds");
        }

        try
        {
            int x = 10;
            int y = 0;
            int z = x / y;

            System.out.println("Result = " + z);
        }
        catch(ArithmeticException e)
        {
            System.out.println("Error: Number Cannot be Divided by Zero");
        }
    }
}
```
<img width="376" height="128" alt="image" src="https://github.com/user-attachments/assets/49814296-718a-4f96-acd8-a9cf93d65a5c" />

```
import java.util.Scanner;

class AgeException extends RuntimeException
{
    AgeException(String msg)
    {
        super(msg);
    }
}

public class AgeTest
{
    public static void main(String args[])
    {
        Scanner sc = new Scanner(System.in);

        int age;

        System.out.print("Enter Student Age: ");
        age = sc.nextInt();

        try
        {
            if(age < 5 || age > 25)
            {
                throw new AgeException("Invalid Age! Age must be between 5 and 25");
            }
            else
            {
                System.out.println("Valid Age");
            }
        }
        catch(AgeException e)
        {
            System.out.println(e.getMessage());
        }
    }
}
```
<img width="397" height="122" alt="image" src="https://github.com/user-attachments/assets/7e0f940a-61e2-458e-871f-2f44384d8b5b" />

```
import java.io.*;

public class FileTransfer
{
    public static void main(String args[]) throws IOException
    {
        FileReader fr = new FileReader("input.txt");
        FileWriter fw = new FileWriter("output.txt");

        int ch;

        while((ch = fr.read()) != -1)
        {
            fw.write(ch);
        }

        fr.close();
        fw.close();

        System.out.println("File transferred successfully character to character.");
    }
}
```
```
import java.io.*;

public class ByteTransfer
{
    public static void main(String args[]) throws IOException
    {
        FileInputStream fin = new FileInputStream("input.txt");
        FileOutputStream fout = new FileOutputStream("output.txt");

        int b;

        while((b = fin.read()) != -1)
        {
            fout.write(b);
        }

        fin.close();
        fout.close();

        System.out.println("File transferred successfully byte to byte.");
    }
}
```
```
import java.io.*;

public class FileCopy
{
    public static void main(String args[]) throws IOException
    {
        FileReader fr = new FileReader("original.txt");
        FileWriter fw = new FileWriter("copy.txt");

        int ch;

        while((ch = fr.read()) != -1)
        {
            fw.write(ch);
        }

        fr.close();
        fw.close();

        System.out.println("File copied successfully.");
    }
}
```
```
class Person
{
    void showName()
    {
        System.out.println("I am a Person");
    }
}

// Single Inheritance
class Student extends Person
{
    void study()
    {
        System.out.println("Student is Studying");
    }
}

// Multilevel Inheritance
class Monitor extends Student
{
    void duty()
    {
        System.out.println("Monitor Manages Class");
    }
}

// Hierarchical Inheritance
class Teacher extends Person
{
    void teach()
    {
        System.out.println("Teacher is Teaching");
    }
}

public class InheritanceTypes
{
    public static void main(String args[])
    {
        Monitor m = new Monitor();

        m.showName();
        m.study();
        m.duty();

        Teacher t = new Teacher();

        t.showName();
        t.teach();
    }
}
```
<img width="375" height="171" alt="image" src="https://github.com/user-attachments/assets/d99bdf6e-579b-4842-8f69-5eb4ad174175" />

```
interface Writer
{
    void write();
}

interface Singer
{
    void sing();
}

class Artist implements Writer, Singer
{
    public void write()
    {
        System.out.println("Artist Writes Songs");
    }

    public void sing()
    {
        System.out.println("Artist Sings Beautifully");
    }

    void perform()
    {
        System.out.println("Artist Performs on Stage");
    }
}

public class MultipleInheritance
{
    public static void main(String args[])
    {
        Artist a = new Artist();

        a.write();
        a.sing();
        a.perform();
    }
}
```
<img width="381" height="147" alt="image" src="https://github.com/user-attachments/assets/0f8dc56a-da49-4696-a80f-d534ec41896f" />
