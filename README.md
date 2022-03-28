# java1
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
