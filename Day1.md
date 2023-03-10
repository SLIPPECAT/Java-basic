<h1>변수</h1>
<h2>상수와 리터럴</h2>
<h3>상수</h3>
한 번만 값이 저장 가능한 변수
선언 방법: final 변수타입 변수이름;
<h3>리터럴</h3>
그 자체로 값을 의미하는 것
<h3>변수 ,상수, 리터럴 구별하기</h3>
변수: 하나의 값을 저장하기 위한 공간
상수: 값을 한 번만 저장할 수 있는 공간
리터럴: 그 자체로 값을 의미하는 것
score: 변수, finalScore: 상수, 100, 1000: 리터럴
<h3>리터럴의 접두사와 접미사</h3>
논리형 ,문자형, 문자열 x
정수형(L:long), 실수형(f,d)
<h3>변수와 리터럴의 타입 불일치</h3>
단 하나의 값을 저장할 수 있는 메모리 공간
메모리공간은 공간이 구분될 수 있도록 메모리 주소를 가지고 있다.
사람이 부르기 불편하므로 특정 메모리 영역에 이름을 붙이고 주소 대신에 이름을 붙여 사용해서 메모리 값을 저장하고 읽을 수 있게 한 것

byte 1bytes
short 2bytes
int 4bytes
long 8bytes

값의 종류(타입)에 따라 변수의 메모리 공간 크기가 결정된다.

변수 선언
변수란 단 하나의 값을 저장할 수 있는 저장 공간
선언 이유: 메모리에 값을 저장할 공간을 마련하기 위함
선언 방법: 변수타입 변수 이름 ex. int age; int num or int age, num;
선언 이후 대입을 하게 되지만, 연속적으로 쓸 수 있다. int x;, x=5;를 int x = 5;로 나타낼 수 있다.

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

변수의 값 읽기

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
 
 <h2>기본형과 참조형<h2/>
 기본형
 논리, 문자, 정수, 실수형
 boolean , byte, short, int, long, float, double, char(변수당 한 문자만 지정)
 
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
 
 <h2>문자와 문자열</h2>
 <h3>문자와 문자열의 차이 확인하기</h3>
 String char = "" 문자열, 빈 문자열, 문자 한 개 가능
 문자열 결함
 tmp를 이용한 값의 교환 (저장한 공간에 다른 값이 들어오기 때문에 미리 저장공간을 마련해두어야 한다.
 
 <h2>증감 연산자와 부호 연산</h2>
 증가 연산자 ++  감소 연산자 --
 전위형, 후위형
 
 부호연산자
 '-'는 피연산자의 부호를 반대로 변경합니다.
 '+'는 아무런 일도 하지 않습니다. (실제 사용x)
 
 <h2>형변환 연산자와 자동 형변환</h2>
 <h3>형변환 연산자</h3>
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
 
 <h2>사칙 연사자와 산술변환</h2>
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

<h2>논리 연산자와 비트 연산자</h2>
<h3>논리 연산자</h3>
&& 논리식이 모두 참이면 참을 반환 (논리 AND 연산)
|| 논리식이 중에서 하나라도 참이면 참을 반환 (논리 OR 연산)
! 논리식의 결과가 참이면 거짓을, 거짓이면 참을 반환(논리 NOT 연산)

 <h3>비트 연산자</h3>
 ❗️ '비트가 모두 1이다'는 무엇을 뜻하죠?
 : 
 & 대응되는 비트가 모두 1이면 1을 반환 (비트 AND 연산자)
 | 대응되는 비트 중에서 하나라도 1이면 1을 반환 (비트 OR 연산)
 ^ 대응되는 비트가 서로 다르면 1을 반환 (비트 XOR 연산)
 ~ 비트를 1이면 0으로, 0이면 1로 반전 (비트 NOT 연산)
 << 명시된 수만큼 비트들을 전부 왼쪽으로 이동시킨다. (left shift 연산) 진수가 커지는 것
 >> 부호를 유지하면서 지정한 수만큼 전부 오른쪽으로 이동시킨다. (right shift 연산) 진수가 작아지는 것
 🧐 이거이거 비트를 하나씩 이동한다는 게 진수가 하나씩 커지거나 작아진다는 것을 말하는구나!
 >>> 지정한 수만큼 비트를 전부 오른쪽으로 이동시키며, 새로운 비트는 전부 0이 됨
 <<< 요거는 없는 걸로 나오네요.

 비트 연산자는 값을 비트 단위로 연산한다.
 따라서 0과 1로 표현이 가능한 정수형이나 형변환이 가능한 자료형만 연산이 가능하다.
 int num1 = 8, num2 = -8;
        System.out.println("8의 2진수 = " + Integer.toBinaryString(num1)); // 0 생략 가능!
        
 <h3>2진수의 음수표현</h3>
 진수의 음수를 표현하는 방식에는 부호 절대값, 1의 보수, 2의 보수가 있다.(8비트 기준으로 설명)
 1. 부호 절대값
 가장 왼쪽에 있는 비트를 부호비트라고 했을 때 이 부호가 0인지 1인지에 따라 양수 ,음수로 구분된다.
 0일때 양수, 1일때 음수
 2진수 00000011 = 10진수: 3
 2진수 10000011 = 10진수: -3
 되게 똑똑하다! 앞에 0, 1로 구분할 생각을 하다니
 2. 1의 보수
 1의 보수는 11111111 - x 를 하는 방식
 11111111 - x는 x를 반전시킨 것과 같다.
 즉, 1이면 0, 0면 1이 된다.
 11111111 - 00101001 = 11010110
 13을 1의 보수 방식으로 표현해 보면
 13을 2진수로 표현: 00001101
 11111111 - x 공식에 대입
 결과: 11110010
 이걸 어디에 쓰는 걸까?
 3. 2의 보수 
 🧐 부호 절대값과 1의 보수 방식을 합쳐둔 것 같다! 그리고 9비트를 이용하는 것 같다!
 아 근데 다르네.. 1의 보수 방식은 11111111이었고 2의 보수 방식은 100000000
 100000000 - 0001101해서 나온 값이구만!
 2진수니까 내려줄 때 나는 1이 되는식으로. 오케이!
 가장 많이 사용하는 방식
 2의 보수는 100000000 - x 를 하는 방식
 2의 보수 방식도 가장 왼쪽 숫자가 0일 경우 양수, 1일 경우 음수를 표현 
 13을 2진수로 표현: 00001101
 100000000 - x 공식에 대입
 결과: 11110011
 
 쉽게 계산하는 방법은 1의 보수를 구한 뒤에 나온 수에 +1을 하면 된다.라고 하는데. .음...
 -9를 1의 보수 방식으로 표현하면
 9를 2진수로 표현: 00001001
  11111111 -  x 공식에 대입
  00001001
  계산하면 11110110
  여기에 +1 
  결과: 11110111
  그냥 계산해보면
  100000000
   00001001
   11110111
   아직은 많이 안해봐서 헷갈리는데 확시리 1의 보수로 계산하는게 쉬운 것 같다. 자리수가 같아져서!
 
 <h3>2진수의 음수표현</h3>
 <h2>조건 연산자와 대입 연산</h2>
 <h3>조건 연산자</h3>
 삼항 연산자: 조건식?반환값1:반환값2
 class Operator8_1 {
    public static void main(String[] args) {
        int num1 = 5, num2 = 7;
        int result;
        String 결과1 = "그렇다", 결과2 = "아니다";
        result = num1 - num2 > 0 ? num1 : num2;

        System.out.println("두 정수 중 더 큰 수는 " + result + "입니다."); // 7
    }
}
 
 <h3>대입 연산자</h3>
 =, +=, -=, *=, /=, $=, &=, !=, ^=, <<=, >>=, >>>=
 
 어?.. 방금 1시 50분이었는데 지금 2시 42분?.. 뭐..지 merge...^^
 
 
 
 
 
 
 
 
