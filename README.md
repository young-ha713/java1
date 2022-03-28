# java
- 하나의 자바 에플리케이션에는 main메서드를 포함한 하나의 클래스가 반드시 있어야 한다.  
main 메서드는 자바의 시작점임. main메서드 없이는 자바 에플리케이션은 실행 될 수 없다.  

- 하나의 소스파일에 둘 이상의 클래스 정의 가능.  
주의점:'소스파일의 이름은 public class의 이름과 일치해야함' 소스파일 내에 public class가 없다면 소스파일 이름은 소스파일 내 어떤 클래스 이름으로 해도 무관  

#### 올바른 작성 예

    Hello.java
    -----------
    public class Hello2{}
         class Hello3{}  //public class가 있는경우 ,소스파일의 이름은 반드시 public class 이름과 일치
         
    Hello.java
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
    
    hello.java
    ----------
    public class Hello2{}
    public class Hello3{}  //소스파일 이름과 public class이름 일치x .대소문자를 구분함으로 대문자로 변경.
    
    
## chapter02 -변수

변수 = 단 하나의 값을 저장할 수 있는 메모리상의 공간  

1. 변수의 선언, 초기화  

    int age; // age라는 이름의 변수를 선언
          //int : 변수타입 , age : 변수 이름
          
           
변수 타입: 저장될 값이 어떤 타입인지 지정

변수이름: 저장될 메모리 공간에 이름을 붙이는것. 그래야 그 공간에 값을 저장하고, 읽어올 수 있음.

**변수선언시: 메모리의 빈 공간에 변수타입에 맞는 크기의 공간이 확보, 이 공간을 변수이름을 통해 사용**
