# کلاس‌ها و اشیاء

مهم‌ترین ویژگی زبان جاوا، شی گرایی است. با استفاده از مفاهیم شی گرایی و عمل به آن‌ها می‌توانید همواره برنامه‌های تمیز، سازماندهی شده‌ و قدرت‌مندی بنویسید. دو مفهوم اصلی شی گرایی کلاس‌ها و اشیا هستند.

### کلاس‌ها {#classes}

به طور خلاصه، کلاس‌‌ها را می‌توان مجموعه‌ای از رفتارها و ویژگی‌ها برای یک شی دانست، که می‌توان اشیاء را از روی آن‌ها ساخت. تمام اشیایی که که از روی یک کلاس ساخته می‌شوند ویژگی‌های همان کلاس را دارا هستند مگر این‌که پس از ساختن کلاس برخی از آن‌ها را که قابل تغییر هستند، تغییر دهید.

#### چگونه کلاس‌ها را بسازیم؟

برای ساختن یک کلاس در جاوا، ابتدا باید کلمه‌ی کلیدی class را بنویسید و سپس نام مورد نظر خود را برای کلاس تعیین کنید. سپس با استفاده از علامت } می‌توانید کلاس را باز کرده و پس از اینکه محتویات کلاس خود را نوشتید لازم است که با علامت { کلاس را خاتمه دهید.

سینتکس ساخت کلاس‌ها در جاوا به صورت زیر است:

```java
class Name {
    // class contents
}
```

توجه کنید که در هنگام نام گذاری کلاس، حرف اول نام کلاس باید یک حرف بزرگ باشد، همچنین اگر نام کلاس شما از چند کلمه تشکیل شده است بهتر است حرف اول هر کلمه با حروف بزرگ آغاز شود. مانند: MyNewClass

یک کلاس می‌تواند هر کدام از انواع متغیرهای زیر را در خود جای دهد:

**۱. متغیرهای محلی** - متغیرهایی که درون متدها، سازنده‌ها و سایر بلوک‌های کد ساخته می‌شوند.

۲. **متغیرهای نمونه** - متغیرهایی که داخل یک کلاس و خارج از هر نوع متد، سازنده و بلوک کد ساخته می‌شوند.

**۳. متغیرهای کلاس** - متغیرهایی که درون یک کلاس و خارج از هر متدی ساخته می‌شوند و دارای کلید واژه‌ی `static` هستند.

همچنین یک کلاس می‌تواند هر تعداد متد و به هر منظوری را درون خود جای دهد.

### اشیاء {#objects}

همان‌گونه که بارها گفته شد، اشیا از روی کلاس‌ها ساخته می‌شوند و برای این‌که از روی یک کلاس یک شی بسازید:

۱. ابتدا باید نام کلاس را بنویسید. \(که اصطلاحا نوع شی نام دارد\)

۲. سپس نام مورد نظر خود برای شی‌ای که می‌خواهید بسازید را انتخاب کنید

۳. پس از آن با یک علامت مساوی \(=\) و سپس کلید واژه‌ی new، متد سازنده‌ی کلاس را فرابخوانید!

**متد سازنده‌ی یک کلاس، همواره متدی با نامی دقیقا برابر با نام همان کلاس است.**

در  ادامه سینتکس ساخت یک شی از روی یک کلاس را مشاهده خواهید کرد:

```java
ClassName objectName = new Constructor();
```

### سازنده‌ها {#constructors}

وقتی صحبت از کلاس‌ها و اشیا می‌کنیم یکی از مهم‌ترین مسائلی که در این مورد وجود دارد متد یا تابع سازنده \(constructor\) است که پیش از این نیز اسم آن را شنیده اید. تمامی کلاس‌ها در جاوا حداقل یک تابع سازنده دارند و حتی اگر آن را تعریف نکنیم نیز کامپایلر جاوا یک سازنده‌ی پیش‌فرض برای آن در نظر می‌گیرد.

هر بار که یک شی ایجاد می‌شود، حداقل یک سازنده فراخوانی می‌شود. قاعده‌ی اصلی سازنده‌ها این است که باید دقیقا هم نام با کلاس خود باشند. همچنین یک کلاس می‌تواند چندین سازنده نیز داشته باشد. در ادامه مثالی داریم از یک کلاس به همراه دو سازنده:

```java
public class JavaLearn {
    JavaLearn(){
        // first constructor
    }
    JavaLearn(int myNumber){
        // second constructor with a parameter, myNumber.
    }
}
```

نکته: سازنده‌ی دوم دارای یک پارامتر است و مقداری را از نوع `int`با نام `myNumber` به عنوان پارامتر دریافت می‌کند. در بخش متدها با این موضوع بیشتر آشنا خواهید شد.

**توجه کنید که سازنده‌ها همواره فاقد نوع هستند! در واقع حتی void نیز نیستند! همچنین یک متد سازنده هیچ مقداری را بر نمی‌گرداند!**

### دسترسی به متغیرهای نمونه و متدهای کلاس {#access-to-instance-variables-and-class-methods}

متغیرهای نمونه و متدها پس از ساخت اشیا به سادگی در دسترس هستند. برای دسترسی به یک متد یا متغیر نمونه در داخل یک کلاس، پس از ساختن یک شی از کلاس مورد نظر، کافیست نام شی‌ای که ساختید را نوشته و سپس با گذاشتن یک علامت نقطه " **.** " آن‌ها را فرابخوانید. سینتکس کلی این موضوع نیز به صورت زیر است:

```java
// create an object
ObjectClassName objectName = new Constructor();

// call a method
objectName.methodName();

// call a variable
objectName.variableName;
```

همچنین با توجه به سطوح دسترسی، قادر خواهید بود مقادیر را نیز تغییر دهید، مثلا:

```text
objectName.variableName = Value;
```

بسیار خب! بیاید یک کلاس بسازیم و سپس یک شی از روی آن کلاس بسازیم و حالت‌های مختلف را مورد بررسی قرار دهیم.

یک سگ را در نظر بگیرید. این سگ ویژگی‌هایی همچون نژاد، سن، رنگ و ... دارد. همچنین یک سگ می‌تواند شامل رفتارهایی همچون غذا خوردن، خوابیدن، دویدن و ... باشد. حال بیاید همین ویژگی‌ها و رفتارها را در قالب یک کلاس با عنوان `Dog` بنویسیم:

```java
public class Dog {
    String color = "brown";
    String breed = "bulldog";
    int age = 3;
    // constructor
    Dog(String name){
        System.out.println("your dog name is: " + name);
    }
    void eating(){
        System.out.println("Dog is eating");
    }
    void sleeping(){
        System.out.println("Dog is sleeping");
    }
    void running(){
        System.out.println("Dog is running");
    } 
}
```

حالا کلاسی برای یک سگ با ویژگی‌ها و رفتارهایی که ذکر شده داریم. برای استفاده از این کلاس دو راه داریم.

اولین راه نوشتن کل کلاس در داخل فایل اصلی برنامه است و سپس ساخت شی از آن است. بدین صورت:

```java
// Dog Class
class Dog {
    String color = "brown";
    String breed = "bulldog";
    int age = 3;
    // constructor
    Dog(String name){
        System.out.println("your dog name is: " + name);
    }
    void eating(){
        System.out.println("Dog is eating");
    }
    void sleeping(){
        System.out.println("Dog is sleeping");
    }
    void running(){
        System.out.println("Dog is running");
    } 
}
// the main class of program
public class MyProgram {
    public static void main(String []args){
        Dog myDog = new Dog("Jessie");
        myDog.eating();
        myDog.color = "white";
        myDog.sleeping();
        System.out.println("my dog's color is: " + myDog.color);
    }
}
```

دقت کنید، هنگامی که به فایل اصلی برنامه‌ی خود به جز کلاس اصلی برنامه، یک کلاس دیگر اضافه می‌کنید \(مثل همین Dog\) نباید از کلید واژه‌ی public درون آن استفاده کنید.

راه دوم ذخیره کردن فایل کلاس به صورت جداگانه است. بدین صورت که ابتدا کلاس \`Dog\` را روی فایلی به نام Dog.java می‌نویسید. سپس فایل برنامه‌ي اصلی خود را مانند همیشه و با رعایت کردن قاعده‌ها نوشته و کارهای نظیر ساخت شی و استفاده از آن را درون فایل اصلی برنامه‌ی خود انجام می‌دهید.

با این روش فایل اصلی برنامه‌ی شما باید به صورت زیر باشد:

```java
public class MyProgram {
    public static void main(String []args){
        Dog myDog = new Dog("Jessie");
        myDog.eating();
        myDog.color = "white";
        myDog.sleeping();
        System.out.println("my dog's color is: " + myDog.color);
    }
}
```

و همچنین  فایل کلاس \`Dog\` نیز دقیقا باید در مسیری که فایل اصلی برنامه‌ی خود را ساخته‌اید، وجود داشته باشد. و  دقت کنید که کلاس Dog حتما باید کلیدواژه‌ی public را داشته باشد.

حال بیاید برنامه را کامپایل و اجرا کنیم:

```text
➜  /tmp javac MyProgram.java 
➜  /tmp java MyProgram 
your dog name is: Jessie
Dog is eating
Dog is sleeping
my dog's color is: white
```

نتیجه‌ای که انتظارش را داشتیم حاصل شد.

### کلمه‌ی کلیدی this

کلمه‌ی کلیدی `this` برای استفاده از متغیرهای نمونه، متدها و یا سازنده‌های داخل کلاسی که در آن قرار داریم استفاده می‌شود. با استفاده از کلمه‌ی کلیدی `this` می‌توانیم اشاره‌ی خود را به عناصر داخل کلاس \(خارج از هر بلوک کدی\) محدود کنیم. برای فراخوانی عناصر داخل کلاس از طریق کلمه‌ی کلیدی this کافیست که ابتدا کلمه‌ی کلیدی this را قرار داده و پس از قرار دادن یک نقطه متغیر نمونه، متد و یا سازنده‌ی خود را صدا بزنیم.

بیاید با یک مثال این موضوع را روشن‌تر کنیم:

```java
class MyAgeClass {
    int myAge = 19;
    void showAge(int myAge) {
        System.out.println("the method's argument for age is:‌ " + myAge);
        System.out.println("the age from instance variable is: " + this.myAge);
    }
}

public class Age {
    public static void main (String []args) {
        MyAgeClass myAgeObject = new MyAgeClass();
        myAgeObject.showAge(18);
    }
}
```

در برنامه‌ی بالا -

ابتدا یک کلاس با نام `MyAgeClass` ساختیم.

سپس متغیری به نام `myAge` از نوع `int` ساختیم که دارای مقدار `19` بود.

پس از آن متدی به نام `showAge` ساختیم که یک آرگومان از نوع int با نام `myAge` دریافت می‌کند. نکته‌ای که این‌جا وجود دارد این است که متغیر ‍`myAge` که متد `showAge` آن را به عنوان آرگومان می‌گیرد، هیچ ارتباطی به متغیر نمونه‌ی `myAge` ندارد و دقیقا کاربرد کلمه‌ی کلیدی `this` در همین موضوع است!

همان‌طور که مشاهده می‌کنید درون متد `showAge` دو متد چاپ قرار داده شده است که اولی مقداری که به عنوان آرگومان به تابع `showAge` داده شده است  را چاپ می‌کند و دومین متد نیز متغیر نمونه‌ی `myAge` را چاپ می‌کند.

حال در کلاس و متد اصلی برنامه یک شی از کلاس `MyAgeClass` می‌سازیم و سپس متد `showAge` را با مقدار `18` به عنوان آرگومان فراخوانی می‌کنیم.

حال برنامه را کامپایل و اجرا می‌کنیم تا نتیجه را مشاهده کنیم:

```
➜  /tmp javac Age.java
➜  /tmp java Age      
the method's argument for age is:‌ 18
the age from instance variable is: 19
```

همان‌طور که مشاهده می‌کنید، اولین متد چاپ، مقداری را که به عنوان آرگومان به متد showAge داده بودیم چاپ کرد و دومین متد چاپ نیز مقدار متغیر محلی myAge را به نمایش در آورد.

## وراثت

یکی از مهم ترین مفاهیم شی گرایی در جاوا، مفهوم وراثت است. با استفاده از مفهوم وراثت، می‌توانید از روی یک کلاس، یک کلاس مجزای دیگر بسازید. در این حالت کلاس اصلی و اولیه، کلاس پدر\(اصطلاحا Super Class نیز گفته می‌شود.\)، و کلاسی که از روی کلاس پدر ساخته شده، کلاس فرزند \(Sub Class نیز گفته می‌شود.\) نام دارد. برای ساخت یک کلاس فرزند از روی یک کلاس، ابتدا باید کلید واژه‌ی `class` و نام کلاس فرزند را نوشته و سپس با کلید واژه‌ی `extends` کلاس پدر را مشخص کنید.

سینتکس وراثت در جاوا به صورت زیر است:

```java
class MySuperClass {
    // class contenets
}

class MySubClass extends MySuperClass {
    // class contents
}
```

در مثال بالا کلاس `MySubClass` یک کلاس فرزند برای `MySuperClass` محسوب می‌شود.

کلاس فرزند تمام پارامترهای کلاس اصلی را به ارث می‌برد همچنین به جز تعدادی معدود \(که در بخش اصلاح کننده‌ها متوجه آن‌ها خواهید شد.\)،  از کلاس فرزند می‌توان به تمام محتویات کلاس اصلی دسترسی داشت.

کد زیر مثالی از یک کلاس پدر و فرزند است:

```java
class Calculation {
    public int multiply(int firstNumber, int secondNumber){
        return firstNumber * secondNumber;
    }
}
class MyCalculation extends Calculation {
    public int division(int firstNumber, int secondNumber){
        return firstNumber / secondNumber;
    }
}

public class Calculate {
    public static void main(String []args){
        MyCalculation testCalculate = new MyCalculation();
        System.out.println(testCalculate.multiply(4, 5));
        System.out.println(testCalculate.division(20, 4));
    }
}
```

نتیجه:

```
➜  /tmp javac Calculate.java
➜  /tmp java Calculate      
20
5
```



### کلمه‌ی کلیدی super

کاربرد کلمه‌ی کلیدی super شبیه به کلمه‌ی کلیدی this است با این تفاوت که اعضای کلاس پدر را از کلاس فرزند تفکیک  می‌کند. در واقع می‌توان گفت هر زمان که بخواهیم در کلاس‌های فرزند، سازنده، متغیر و یا متدی را از کلاس اصلی فراخوانی کنیم که دقیقا نام آن‌ها با نام یک متغیر، سازنده و یا متد در کلاس فرزند یکی باشد، از super استفاده می‌کنیم.  همچنین یکی از کاربردهای مهم super فراخوانی سازنده‌ی کلاس پدر از سازنده‌ی کلاس فرزند است. برای روشن‌تر شدن موضوع به مثال زیر توجه کنید:

```java
class MySuperClass {
    String myString = "Hello From Super Class!";
}

class MySubClass extends MySuperClass {
    String myString = "Hello From Sub Class";
    void showMyString() {
        System.out.println(myString);
    }
}

public class MyInharitance{
    public static void main(String []args){
        MySubClass mySub = new MySubClass();
        mySub.showMyString();
    }
}
```

برنامه‌ی بالا صرفا یک کلاس و یک فرزند از روی همان کلاس است که کار بسیار ساده‌ای می‌کند و منطق آن کاملا واضح است. اگر برنامه را کامپایل کنیم خروجی ای مانند این خواهیم داشت:

```
➜  /tmp javac MyInharitance.java
➜  /tmp java MyInharitance      
Hello From Sub Class
```

در مثال بالا دو متغیر با نام `myString` مشاهده می‌کنید که یکی از آن‌ها در داخل کلاس اصلی یعنی `MySuperClass` و دومی نیز در کلاس فرزند یعنی `MySubClass` قرار دارد. حال ما درون متد `showMyString` که در داخل کلاس فرزند واقع شده است، متد چاپ در جاوا را فراخوانی کردیم تا مقدار `myString`را مشاهده کنیم. حال فرض کنید به متغیر `myString` واقع در کلاس اصلی \(`MySuperClass`\) نیاز دارید. اینجاست که `super` به کار شما خواهد آمد!

برای روشن شدن قضیه برنامه را به شکل زیر تغییر می‌دهیم:

```java
class MySuperClass {
    String myString = "Hello From Super Class!";
}

class MySubClass extends MySuperClass {
    String myString = "Hello From Sub Class";
    void showMyString() {
        System.out.println(super.myString);
    }
}

public class MyInharitance{
    public static void main(String []args){
        MySubClass mySub = new MySubClass();
        mySub.showMyString();
    }
}
```

حال در متد چاپ کلمه‌ی کلیدی `super` را اضافه کردیم، این به این معناست که به متغیر `myString` موجود در تابع پدر اشاره داریم.  نتیجه مطلوب است:

```
➜  /tmp javac MyInharitance.java 
➜  /tmp java MyInharitance 
Hello From Super Class!
```

همان‌طور که مشاهده می‌کنید متغیر واقع شده در کلاس پدر چاپ شد.

کاربرد دیگر `super` فراخوانی متد سازنده‌ی کلاس اصلی در کلاس فرزند است. بدین ترتیب که هر گاه درون سازنده‌ی کلاس فرزند، متد `super()` را استفاده کنید، سازنده‌ی کلاس اصلی اجرا می‌شود! به مثال زیر دقت کنید:

```java
class MyClass {
    MyClass() {
        System.out.println("Hello from super class!");
    }
}
class MySecondClass extends MyClass {
    MySecondClass() {
      super();
      System.out.println("Hello From Sub Class!")  
    }
}

public class MySuperTest {
    public static void main(String []args){
        MySecondClass myObject = new MySecondClass();
    }
}
```

### رابطه‌ی IS-A {#packages}

در زبان جاوا IS-A نام یک مفهوم است که بیان می‌کند، این شی یک نوع از آن شی است! \(this object is a that object\) . برای روشن‌تر شدن موضوع نگاهی به کد زیر بیندازید:

```java
public class Car {
}
public class Mercedes extends Car{
}
public class Porsche extends car{
}
public class Panamera extends Porsche {
}
```

در تکه کد بالا -- 

کلاس `Mercedes` یک فرزند برای کلاس `Car` است.

کلاس `Porsche` نیز یک فرزند برای کلاس `Car` است.

کلاس `Panamera` یک فرزند برای کلاس `Porsche` محسوب می‌شود.

کلاس `Panamera` فرزند هر دو کلاس `Car` و `Porsche` محسوب می‌شود.

حال اگر بخواهیم با رابطه‌ی IS-A روابط بین این کلاس‌ها را بنویسم می‌توانیم به صورت زیر این کار را انجام دهیم:

Mercedes IS-A Car

Porsche IS-A Car

Panamera IS-A Porsche

Hence: Porsche IS-A Car as well



در بحث وراثت باید به یاد داشته باشید که در جاوا یک کلاس نمی‌تواند بیشتر از یک کلاس دیگر را گسترش \(extend\) دهد! مثلا مثال زیر در زبان جاوا پذیرفته نیست:

```java
public class MyClass extends Mercedes, Porsche {
}
```

### بسته‌ها در جاوا {#packages}

بسته‌ها یا پکیج‌ها در جاوا راهی برای سازماندهی کردن کلاس‌ها و رابط‌ها هستند. هنگام توسعه‌ی برنامه‌‌ها در جاوا ممکن است هزاران کلاس و رابط بنویسید، از این رو مرتب کردن و سازماندهی کردن آن‌ها می‌تواند به روند پیشرفت پروژه کمک شایانی کند و دسترسی به اجزای سورس برنامه نیز ساده‌تر باشد. این کار به کمک بسته‌ها امکان پذیر است.

