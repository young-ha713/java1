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

### 1. 변수의 선언, 초기화  

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
4.특수문자는 - 와 & 만 허용 ex)$harp가능 S#arp 불가능*    

*권장규칙  
1.클래스 이름 첫 글자는 대문자, 변수와 메서드 이름 첫 글자는 소문자  
2.여러 단어로 이루어진 이름은 카멜로 씀 ex) StringBuffer  
3.상수의 이름은 모두 대문자. 여러 단어로 이뤄진 경우 _로 구분*  
  
  
### 2. 변수의 타입  

값  
1.문자  

2.숫자  
1)정수  
2)실수  

--------  
이러한 값(data)의 종류(type)에 따라 저장될 공간의 크기와 저장형식을 정의한것 = *자료형*  
  
자료형  
1. 기본형 : **실제 값 저장** 논리형(boolean),문자형(char/하나의 문자), 정수형(byte,short,int,long), 실수형(float,double) 총 8개  
  
  
1)기본형의 종류와 크기  

정수형: byte (1byte), short(2byte), int(4byte), long(8byte)  
문자형: char (2byte)  
논리형: boolean(1byte)  
실수형: float(4byte), double(8byte)  


  
  
  
##### 2. 참조형 : **출력시 무조건 주소값 반환** 기본형 제외한 나머지. 클래스 자료형 
 1)참조변수 선언 방법- **클래스 이름 변수이름;** //변수의 타입이 기본형이 아닌것은 모두 참조변수. String 등등  
 ```Date today;```  
 
 2)참조변수 초기화  
 ```Date today = new Date();  //Date 객체를 생성해서, 그 주소를 today에 저장 ```  
 <img width="500" alt="20220328_204914" src="https://user-images.githubusercontent.com/80766275/160392417-b34e6c8c-5307-44a4-9c49-c595477a3534.png">  
 결과는 주소값 나옴.
 

### 2.2 상수와 리터럴  
  
  
상수 : 값을 저장할 수 있는 공간.  
**변수와 차이점은 한번 값을 저장하면 변경 불가**  
  
1)선언&초기화
```타입 + 이름 ;  
   final int MAX_SPEED = 10;  // 상수는 모두 대문자 사용하고 여러 단어로 이루어졌을때는 _ 사용  
```  
  
**변수: 하나의 값만을 저장할 수 있는 데이터 상의 공간**  
**상수: 값을 한번만 저장 할 수 있는 공간 변경 불가**  
**리터럴: 그 자체로의 값을 의미함**  
  
``` int(자료형) year(변수) = 2022(리터럴);    
    final int MAX_SPEED(상수) = 10(리터럴);  
```  
  
***상수를 사용하는 이유    
  
``` final int WIDTH = 20;   
    final int HEIGHT = 10;  
  
    int triangleArea = (WIDTH * HEIGHT) / 2;  
    int rectangleArea = WIDTH * HEIGHT ;  
```  

상수값으로 설정해놓으면 여러곳 수정 필요 x 상수 초기화만 하면 됨 *상수는 리터럴에 '의미있는 이름'을 붙여 코드 이해와 수정 쉽도록 함

  
스캐너 (Scanner) 클래스: 화면에서 입력받는 법.  
  
1.유틸 임포트하기  
```import java.utill.*;  // 스캐너 클래스 사용받기위해 다운?하는 늑김``` 
  
2.Scanner 클래스 객체 생성 
```Scanner scanner = new Scanner(System.in);```
  
3.nextLine() 메소드 호출  
```String input = scanner.nextLine();  // 입력대기 상태에 있다가 입력 마치고 앤터 누르면 입력 내용이 문자열(String)으로 저장  
   int num = Integer.ParseInt(input);  //입력받은 내용을 int타입으로 변환  
```  
***Integer.Parser(); - 입력받은것을 정수로 전환  / scanner.nextInt(); 정수로 입력받음***  
  
  
### 형변환 (Casting)  
  
***변수 또는 상수의 타입을 다른 타입으로 변환하는것 why?다른 타입끼리는 연산x so 연산전에 타입을 일치시킴***  



