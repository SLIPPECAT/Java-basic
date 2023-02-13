# Java-basic
It is the repository for Java

변수: 단 하나의 값을 저장할 수 있는 메모리 공간

메모리공간은 공간이 구분될 수 있도록 메모리 주소를 가지고 있다.
사람이 부르기 불편하므로 특정 메모리 영역에 이름을 붙이고 주소 대신에 이름을 붙여 사용해서 메모리 값을 저장하고 읽을 수 이게 한 것

byte 1bytes
short 2bytes
int 4bytes
long 8bytes

값의 종류(타입)에 따라 변수의 메모리 공간 크기가 결정된다.

변수 선언
선언 이유: 메모리에 값을 저장할 공간을 마련하기 위함
선언 방법: 변수타입 변수 이름 ex. int age; int num or int age, num;

class Variable_1{
}
변수 생성 규칙
1. 대소문자 구분되며 길이에 제한x
2. 예약어 상용 불가
3. 숫자로 시작 불가
4. 특수 문자_와 $만 허용


변수의 여러가지 형태
1. Camel case ex. 
2. Snake case ex. 
3. Pascal case(✗) ex. VarTest
4. Kebab case(✗) ex. var-test

 변수의 초기화
 : 변수에 처음으로 값을 저장하는 것을 의미
 class Variable_2{
   public static void main(String[] args){
      boolean flag = false;
      char grade = 'A';
      byte val = 127;
      shrt sval = 128;
      int num = 32768
      long price = 2_147_483_648L
      float tax = 3.14f;
      double score = 3.14159265358979;
      
      System.out.prtinln("boolean = " + flag)
   }
 
변수의 값 읽기
class Variable1_3 {
    public static void main(String[] args) {
        int age = 23;

        year = age + 2000;
        System.out.println("year = " + year); // 2023

        // 변수의 값을 읽어오는 과정
        // year = age + 2000;
        // year = 23 + 2000;
        // year = 2023;

        age = age + 1;
        System.out.println("age = " + age); // 24
        System.out.println("year = " + year); // 2023

        // 변수의 값을 읽어오는 과정
        // age = age + 1;
        // age = 23 + 1;
        // age = 24;
        // 프로그램은 순차적으로 코드가 실행되기 때문에
        // 여기서 age의 값이 바뀌었다고 year에 영향을 주지 않는다.
    }
}

변수의 종류
: 변수의 종류에는 클래스, 인스턴스, 지역 변수가 있다.
class Variable1_4 {
    static int classVal = 100; // 클래스 변수
    int instanceVal = 200; // 인스턴스 변수

    public static void main(String[] args) {
        int num; // 지역 변수
//        System.out.println("int = " + num); // Error 발생
        num = 300;
        System.out.println("int = " + num); // 100

        // 인스턴스 변수
//        System.out.println("instanceVal = " + instanceVal); // Error 발생
        Variable1_4 instance = new Variable1_4 (); // 인스턴스 변수 사용을 위해 객체 생성
        System.out.println("instanceVal = " + instance.instanceVal); // 100

        // 클래스 변수
        System.out.println("classVal = " + classVal);
        // 같은 클래스 내부는 바로 접근 가능
        System.out.println("Main.classVal = " + Variable1_4.classVal);
        // 클래스 변수 : 클래스명.클래스변수명 으로 접근 or
    }
 }
 
 상수
 한 번만 값이 저장 가능한 변수
 선언 방법: final 변수타입 변수이름.
 
 int
 final int
 
 리터럴
 그 자체로 값을 의미하는 것
 상수와 구별하기 위해 사용하는 용어
 
 변수, 상수, 리터럴 구하기
 score: 변수
 finalScore: 상수
 100, 1000: 리터럴
 
 리터럴의 접두사와 접미사
 논리형, 문자형, 문자열: 없음
 정수형: 접미사 L  ex. byte, short, int, long(L)
 실수형: 접미사 f, d  ex. double(d) float(f)  double > float
 
 변수와 리터럴의 타입 불일치
 범위가 '변수 > 리터럴'인 경우 통과
 범위가 '변수 < 리터럴'인 경우 에러
 
 기본형과 참조형
 기본형
 논리, 문자, 정수, 실수형
 boolean , byte, short, int, long, float, double, char
 
 아스키 코드: 128개의 문자조합을 제공하는 7비트 부호
 유니코드: 16비트로 표현 최대 65536자 표현 가능
 UTF-8: 유니코드를 사용하는 인코딩 방식 중 하나
 
 정수형 오버플로우
 
 타입간의 변환방법
 문자와 숫가간의 변환
 1. 숫자를 문자로: 숫자 + '0' -> 문자
 2. 문자를 숫자로: 문자 - '0' -> 숫자
 
 문자열로의 변화
 1. 숫자를 문자열로: 숫자 +"" -> 문자열
 2. 문자를 문자열로: 문자 +"" -> 문자열
 
 문자열을 숫자, 문자로 변환
 1. 문자열을 숫자로: Integer.parseInt("문자열"), Double.parseDouble("문자열")
 2. 문자열을 문자로: "문자열".charAt(0)
 
 참조형
 기본형을 제외한 나머지 타입  ex. String, System
 null(어떤 객체의 주소도 저장되지 않음) 또는 메모리 주소를 저장한다. 항상 4byte (JVMdl 64비트일 경우 8바이트)
 
 문자와 문자열
 문자와 문자열의 차이 확인하기
 String char = "" 문자열, 빈 문자열, 문자 한 개 가능
 문자열 결함
 tmp를 이용한 값의 교환
 
 <h1>증감 연산자와 부호 연산</h1>
 증가 연산자 ++  감소 연산자 --
 전위형, 후위형
 
 부호연산자
 '-'는 피연산자의 부호를 반대로 변경합니다.
 '+'는 아무런 일도 하지 않습니다. (실제 사용x)
 
 <h3>형변환 연산자와 자동 형변환</h3>
 <h5>형변환 연산자</h5>
 형변환이라?
 변수 또는 상수의 타입을 다른 타입으로 변환하는 것을 의미한다.
 피연산자
 타입
 int -> char
 char -> int
 float -> int
 int -> float
 
 자동 형변환
 floatf = 1234, floatf = (float)1234 생략 가능
 int i = 3.14f; inti = (int)3.14f
 기존의 값을 최대한 보존할 수 있는 타입으로 자동 형변환된다.
 
 <h3>사칙 연사자와 산술변환</h3>
 사칙 연산자: 덧셈 뺄셈, 곱셈, 나눗셈
 
 산술변환
 연산 전에 피연산자의 타입을 일치시키는 것을 의미
 1. 두피연산자의 타입을 같게 일치시킨다.(보다 큰 타입으로 일치)
 2. 피연산자의 타입이 int보다 작은 타입이면 int로 변환된다.
 숫자끼리 변환해야할 땐 뒤에 대문자로 표시 또는 f
 문자를 숫자로 변환하거나 해야할 때는 변수 앞에 (int)를 붙여주기
 
 <h3>Math 클래스와 나머지 연산자</h3>
 Math
 Math는 수학과 관련된 메서드를 가지고 있는 클래스
 메서드는 특정한 기능을 수행하기 위해 코드로 작성된 단위!
 
 round() 실수를 소수점 첫 째자리에서 반올림한 정수를 반환
 ceil() 올림값을 double형으로 반환
 floor() 내림값을 double형으로 
 abs() int, double 기본형 모두 사용 가능하며 절대값을 얻는다.

나머지 연산자 %
오른쪽 피연산자로 나누고 남은 나머지를 반환  cf. 나눗셈을 할 때는 정수부분만 반환했다.
나누는 피연산자는 0이 아닌 정수만 허용
부호는 무시된다.

<h3>비교연산자와 문자열의 비교</h3>
비교연산자
== 왼쪽과 오른쪽의 피연산자가 같으면 참을 반환
!= 왼쪽과 오른쪽의 피연산자가 같지 않으면 참을 반환
> 왼쪽의 피연산자가 오른쪽의 피연산자보다 크면 참을 반환
> = 왼쪽의 피연산자가 오른쪽의 피연산자보다 크거나 같으면 참을 반환
< 왼쪽의 피연산자가 오른쪽의 피연산자보다 작으면 참을 반환
< = 왼쪽의 피연산자가 오른쪽의 피연산자보다 작거나 같으면 참을 반환
두 피연산자를 비교해서 true(참) 또는 false(거짓)를 반환


문자열의 비교
문자열 비교에는 == 대신 equals()를 사용한다.
equals: 비교하고자 하는 두 피연산자의 값 자체를 비교한다.
==: 비교하고자 하는 두 피연산자의 주소를 비교한다.
        
        String s1 = "사랑";
        String s4 = "우정";
        System.out.println(s1.equals(s4));
        // false
        
        String s3 = new String("사랑");
        System.out.println(s1 == s3);  // false 주소값이 다르기 때문에 false
        System.out.println("s1.equals(s3) = " + s1.equals(s3)); // true 값 자체가 같기 때문에 true

<h3>논리 연산자와 비트 연산자</h3>
 
 
 
 
 
 
 
 
