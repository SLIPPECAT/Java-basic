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
 
 
 
 
 
 
 
 
 
 
 
