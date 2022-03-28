# java
- 하나의 자바 에플리케이션에는 main메서드를 포함한 하나의 클래스가 반드시 있어야 한다.  
main 메서드는 자바의 시작점임. main메서드 없이는 자바 에플리케이션은 실행 될 수 없다.  

- 하나의 소스파일에 둘 이상의 클래스 정의 가능.  
주의점:'소스파일의 이름은 public class의 이름과 일치해야함.  소스파일 내에 public class가 없다면, 소스파일 이름은 소스파일 내 어떤 클래스 이름으로 해도 무관  

#### 올바른 작성 예

    Hello2.java
    -----------
    public class Hello2{}
         class Hello3{}  //public class가 있는경우 ,소스파일의 이름은 반드시 public class 이름과 일치
         
    Hello2.java
    ----------
    class Hello2{}
    class Hello3{}   //public class가 하나도 없는 경우, 소스파일의 이름은 Hello2.java , Hello3.java 둘 다 가능
  
  
  #### 잘못된 예
    Hello2.java
    -------------
    public class Hello2{}
    public class Hello3{}  //하나의 소스파일에 public class 두개 안됨. 각 클래스를 별도 소스파일에 저장하거나 둘중 하나에 퍼블릭 빼야함

    Hello3.java
    -----------
    public class Hello2{}
    public class Hello3{}  //소스파일의 이름이 public class 의 이름과 맞지x 소스파일 이름 변경 필요
    
    hello2.java
    ----------
    public class Hello2{}
     class Hello3{}  //소스파일 이름과 public class이름 일치x .대소문자를 구분함으로 대문자로 변경.
    
    
## chapter02 -변수

변수 = 단 하나의 값을 저장할 수 있는 메모리상의 공간  

1. 변수의 선언, 초기화  

```
int age; // age라는 이름의 변수를 선언
          //int : 변수타입 , age : 변수 이름
```
          
           
변수 타입: 저장될 값이 어떤 타입인지 지정

변수이름: 저장될 메모리 공간에 이름을 붙이는것. 그래야 그 공간에 값을 저장하고, 읽어올 수 있음.

**변수선언시: 메모리의 빈 공간에 변수타입에 맞는 크기의 공간이 확보, 이 공간을 변수이름을 통해 사용**  

**변수초기화: 값을 넣어주는것 .변수 선언 후 바로 사용할 수 있으나 ,사용 전 반드시. 전에 다른 프로그램에 의한 쓰레기값 있을 수 있기 때문.  하지 않으면 null값 나옴**  
값을 저장할 시에는 대입연산자 ' = ' 이용 : 오른쪽의 값을 왼쪽에 저장.  

```int age = 26; //변수 age 선언, 26으로 초기화```  
  
```
int a;  
    int b;  
    int x = 0;  
    int y = 0;
    
위와  
int a,b;  
   int x=0, y=0;  
```  
는 같다. 타입이 같을시 콤마로 한줄에 선언 가능.  
  
  
  
```
class VariExl{
    public static void main(String[] args) {
        int year = 0;
        int age = 14;
        
        sysout(year);
        sysout(age);
        
        year = age + 2000;
        age = age +1; 
        
        sysout(year);
        sysout(age);
    }
}
```  
두 변수 교환하기  

```
class VariEx2{
    public static void main(String[] args) {
        int x = 10, y = 20;
        int tmp=0;
        
        sysout("x:"+x+"y"+y);
        
        tmp = x; 
        x = y; 
        y = tmp;
        
        sysout("x:"+x+"y"+y);
    }
}
```  
  
  
*변수의 명명 규칙  
1.대소문자 구별,길이 제한x  
2.예약어x (abstract,default,if,package,this ...)  
3.숫자 시작x  
4.특수문자는 - 와 & 만 허용 ex)$harp가능 S#arp 불가능    

*권장규칙  
1.클래스 이름 첫 글자는 대문자, 변수와 메서드 이름 첫 글자는 소문자  
2.여러 단어로 이루어진 이름은 카멜로 씀 ex) StringBuffer  
3.상수의 이름은 모두 대문자. 여러 단어로 이뤄진 경우 _로 구분  
