## تصمیم گیری و شرط
در زبان جاوا با استفاده از شرط‌ها قادر هستید عملکرد برنامه را در حالت‌های مختلفی که ممکن است پیش بیاید تغییر دهید.

در جاوا شرط‌ها را به دو صورت می‌توانیم بنویسیم:

۱. ** if ... else **: معروف ترین نوع شرط که در تمام زبان‌های برنامه نویسی موجود است. اگر عبارتی که به عنوان شرط به if می‌دهید صحیح باشد بلوک کد مربوط به if را اجرا می‌کند. در غیر این صورت به سراغ else if ها رفته و هر کدام که شرط‌شان صحیح باشد بلوک مربوطه را اجرا می‌کند و اگر هیچ‌کدام از آن‌ها صحیح نبود در نهایت بلوک مربوط به else را اجرا می‌کند. (توجه کنید که else if ها و else اجباری نیستند و در صورتی که در کنار شرط if خود به آن‌ها نیاز دارید می‌توانید از آن‌ها استفاده کنید.)

سینتکس  if ... else در جاوا به صورت زیر است:
```
if (condition) {
    statements
} 
else if (condition) {
    statements
}
else {
    statements
}
```


مثال:
```java
class IfDemo {
    public static void main(String []args) {

        int age = 18;

        if (age == 18) {
            System.out.println("age is eighteen");
        } 
        else if (age == 19){
            System.out.println("age is nineteen");

        } 
        else if (age == 20){
            System.out.println("age is twenty");

        } 
        else {
            System.out.println("age isn't defined!");
        }
    }
}
```

خروجی:
```
➜  /tmp javac IfDemo.java 
➜  /tmp java IfDemo 
age is eighteen
```

۲. **switch**: این نوع شرط شباهت زیادی به else if دارد و با استفاده از آن می‌توانید مقدار یک متغیر را بررسی و با استفاده و رفتارهای موردنظر خود را برای حالت‌های مختلف اعمال کنید. سینتکس کلی switch به صورت زیر است:

```
switch (expression) {
    case firstValue:
        statements
        break; (optional)
    case secondValue:
        statements
        break; (optional)
    case thirdValue:
        statements
        break; (optional)
    ........
    default:
        statements
        break; (optional)
}
```

سوییچ در ابتدا یک expression دریافت می‌کند (که معمولا متغیر است) و سپس با استفاده از کلمه‌ی کلیدی case می‌توانید مقادیر expression داده شده را بررسی کنید و در صورت صحیح بودن هر یک از caseها، بلوک کد آن اجرا خواهد شد. همچنین در صورتی که هیچ یک از case ها صحیح نباشند، بلوک کد مربوط به default اجرا خواهد شد.


مثال:

```java
class SwitchDemo {
    public static void main(String []args){
        int age = 18;
        switch (age) {
            case 18:
                System.out.println("age is eighteen");
                break;
            case 19:
                System.out.println("age is nineteen");
                break;
            case 20:
                System.out.println("age is twenty");
                break;
            default:
                System.out.println("age isn't defined");
                break;
        }

    }

}
```
خروجی:

```
➜  /tmp javac SwitchDemo.java  
➜  /tmp java SwitchDemo 
age is eighteen
```

دقت کنید اگر `break` در پایان  هر case قرار نگیرد آن‌گاه هنگامی که switch با اولین شرط صحیح مواجه شود، علاوه بر بلوک کد case صحیح، بلوک کد مربوط به caseهای بعدی آن را نیز اجرا می‌کند.


مثال:
```java
class SwitchDemo{
    public static void main(String []args){
        int age = 18;

        switch (age){
            case 16:
                System.out.println("age is sixteen");
            case 17:
                System.out.println("age is seventeen");
            case 18:
                System.out.println("age is eighteen");
            case 19:
                System.out.println("age is nineteen");
            case 20:
                System.out.println("age is twenty");
            default:
                System.out.println("age isn't defined!");
        }
    }
}
```
خروجی:
```
➜  /tmp javac SwitchDemo.java 
➜  /tmp java SwitchDemo 
age is eighteen
age is nineteen
age is twenty
age isn't defined!
```