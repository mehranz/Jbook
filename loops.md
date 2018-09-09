## حلقه‌ها

هنگام برنامه نویسی ممکن است قصد داشته باشید برنامه‌ی خود را به حالت‌های مختلف پیاده کنید! یکی از این حالت‌ها تکرار کردن یک یا چند عمل به تعدادی مشخص یا نامشخص است. در این مواقع حلقه‌ها به کار شما خواهند آمد. 

در زبان جاوا چندین نوع حلقه داریم که عبارت‌اند از -

۱. **while**: این حلقه تا زمانی شرطش صحیح باشد، بلوک کد تعیین شده را اجرا می‌کند.

سینتکس حلقه‌ی while به صورت زیر است:
```java
while (condition) {
    statements
}
```
مثال:
```java
class WhileLoopDemo {
    public static void main(String []args){
        int myVar = 1;
        while (myVar < 10){
        System.out.println(myVar);
        myVar++;
        }
    }
}
```
نتیجه:
```
➜  /tmp javac WhileLoopDemo.java 
➜  /tmp java WhileLoopDemo 
1
2
3
4
5
6
7
8
9
```


۲. **for**: این حلقه بلوک کد خود را به تعداد معینی اجرا می‌‌کند.

سینتکس حلقه‌ی for به صورت زیر است:
```java
for (initializationCondition; loopCondition; increment/decrement) {
    statements
}
```


حلقه‌ی for یک مقدار اولیه، شرط حلقه و در نهایت فرمان افزایش و یا کاهش را دریافت می‌کند. اگر شرط حلقه صحیح بود، بلوک کد خود را اجرا کرده و به فرمان افزایش یا کاهش باز می‌گردد و آن را انجام می‌دهد سپس دوباره بررسی می‌کند که آیا شرط حلقه صحیح است یا خیر و آن‌قدر این کار را انجام می‌دهد تا شرط حلقه نادرست شود. مثال:
```java
class ForLoopDemo{
    public static void main(String []args){
        for (int myVar = 1; myVar < 10; myVar++){
            System.out.println("value is: " + myVar);
        }
    }
}
```

خروجی:
```
➜  /tmp javac ForLoopDemo.java
➜  /tmp java ForLoopDemo       
value is: 1
value is: 2
value is: 3
value is: 4
value is: 5
value is: 6
value is: 7
value is: 8
value is: 9
```

۳. **do ... while**: این حلقه شباهت زیادی به حلقه‌ی while دارد با این تفاوت که شرط حلقه را می‌توانید در انتهای آن تعریف کنید. سینتکس حلقه‌ی do ... while به صورت زیر است:
```
do {
statements
} while(condition);
```
مثال:
```java
class DoWhileLoopDemo{
    public static void main(String []args){
        int myVar = 1;
        do {
            System.out.println(myVar);
            myVar++;
        } while(myVar < 10);
    }
}
```
خروجی:
```
➜  /tmp javac DoWhileLoopDemo.java   
➜  /tmp java DoWhileLoopDemo 
1
2
3
4
5
6
7
8
9
```


## کنترل کردن حلقه‌ها
گاهی نیاز است که روند عادی اجرا شدن حلقه‌ها را کنترل کنیم که بدین منظور در زبان جاوا دو گزاره فراهم شده است که عبارت‌اند از -

۱. **break**: این گزاره حلقه را می‌شکند و آن را پایان می‌دهد.

مثال:
```java
class BreakDemo{
    public static void main(String []args){
        int myVar = 1;
        while (myVar < 10){
            myVar++;
            System.out.println(myVar);
            if (myVar == 8){
                break;
            }
        }
        System.out.println("Loop Breaked!");
    }
}
```


در برنامه‌ی بالا ابتدا متغیری با نام `myVar` و با مقدار 1 تعریف کردیم.

سپس یک حلقه‌ی while ساختیم که تا زمانی که مقدار متغیر `myVar` کوچکتر از 10 باشد، بلوک کد خود را اجرا کند.

در بلوک کد حلقه ابتدا یک واحد به مقدار متغیر مورد نظرمان اضافه کردیم و سپس آن را چاپ کردیم.

در مرحله‌ی بعدی با استفاده از یک شرط (در بخش بعدی کاملا با آن‌ها آشنا خواهید شد) مشخص کردیم که وقتی مقدار متغیر به 8 رسید حلقه را بشکند و از آن خارج شود. 


خروجی:
```
➜  /tmp javac BreakDemo.java 
➜  /tmp java BreakDemo 
2
3
4
5
6
7
8
Loop Breaked!
```

۲. **continue**: هر گاه این گزاره اجرا شود به کامپایلر اعلام می‌کند که از اجرای بقیه‌ی دستورات درون بلوک کد حلقه جلوگیری کرده و حلقه را مجددا از ابتدا اجرا کند.

مثال:
```java
class ContinueDemo{
    public static void main(String []args){
        int myVar = 1;
        while (myVar < 10){
            myVar++;
            if (myVar == 5){
                continue;
                System.out.println("this is continue!");
            }
            System.out.println(myVar);
        }
    }
}
```


در این برنامه مانند قبل ابتدا یک متغیر با نام `myVar` و مقدار 1 تعریف کردیم.

سپس یک حلقه‌ی while ساختیم تا زمانی که مقدار متغیر کوچکتر از 10 باشد بلوک کد خود را اجرا کند.
بلوک کد این حلقه شامل دستور اضافه کردن یک واحد به متغیر `myVar`و یک شرط که بیانگر زمانی است که مقدار متغیر `myVar` برابر 5 باشد، است.

درون بلوک کدِ شرط، یک گزاره‌ی `continue` وجود دارد که بیان می‌کند هنگامی که مقدار متغیر `myVar‍` به عدد 5 رسید، بقیه‌ی محتویات بلوک حلقه را اجرا نکرده و به ابتدای آن بازگردد. همچنین یک عبارت را نیز چاپ می‌کند تا متوجه تاثیر continue بر روی اعداد، شویم.

و در نهایت مقدار متغیر را چاپ می‌کنیم.

خروجی مطلوب است:
```
➜  /tmp javac ContinueDemo.java 
➜  /tmp java ContinueDemo 
2
3
4
this is continue!
6
7
8
9
10

```