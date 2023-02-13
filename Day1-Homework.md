<h3>Report1</h3>

    // 2-4. 다음 중 변수를 잘못 초기화 한 것은?
    byte b = 256;  ❗️ byte는 -128~127의 범위내에서 저장 가능하다.
    char c = ''; ❗️ char는 빈 문자를 선언할 수 없다.
    char answer = 'no'; ❗ char는 한 문자만을 선언할 수 있다.
    float f = 3.14  ❗ 리터럴과 타입이 일치하지 않으므로 3.14뒤에 f를 붙이거나 float을 double로 바꾸어 줄 수 있다.
    double d = 1.4e3f;


    //2-7. 다음 문장들의 출력 결과를 적으세요. 오류가 있는 문장의 경우, '오류' 라고 적으세요.
    System.out.println("1" + "2");  // ❗12
    System.out.println(true+"");  // ❗true
    System.out.println('A' + 'B');  // ❗AB
    System.out.println('1' + 2);  // ❗12
    System.out.println('1' + '2');  // ❗12
    System.out.println('J' +"ava");  // ❗Java
    System.out.println(true + null);  // ❗오류 연산자를 boolean에 적용할 수 없다.


    //2-8. 아래는 변수 x, y, z의 값을 서로 바꾸는 예제이다. 결과와 같이 출력되도록 코드를 넣으세요.
    public class Exercise2_8{
        public static void main(String[] args){
            int x = 1;
            int y = 2;
            int z = 3;
             
             int tmp = x;
              x=y;
              y=z;
              z=tmp;
           
            System.out.println("x="+x);
            System.out.println("y="+y);
            System.out.println("z="+z);
        }
    }
    //예상 결과 : x=2, y=3, z=1

<h3>Report2</h3>

    //3-1. 다음 중 형변환을 생략할 수 있는 것은? (모두 고르시오)
    public class Exercise2_8{
    public static void main(String[] args) {
    byte b = 100;
    char ch = 'A';
    int i = 100;
    long l = 1000L;
    //3-1. 다음 중 형변환을 생략할 수 있는 것은? (모두 ❗️로 고르시오)
    //대응시키려는 타입의 값이 대응값의 타입보다 작은 범위의 타입일 경우 형변환을 생략할 수 없다.
    b = (byte)i;  // 형변환을 생력할 수 없다. 이 경우 디폴트 타입은 int인데 byte는 int보다 작은 범위를 갖는 타입이다.
    ch = (char)b;  // 형변환을 생력할 수 없다. b는 byte 타입의 숫자를 나타내고 ch는 char 타입의 문자이므로 형변환을 해주어야 한다.
    short s = (short)ch;  // 형변환을 생력할 수 없다. s는 short 타입의 숫자를 나타내고 ch는 char 타입의 문자이므로 형변환을 해주어야                                 한다.
    float f = (float)l;  // ❗️f는 float타입이고 l은 long타입인데 float타입의 범위가 더 넓으므로 float는 형변환 생략을 할 수 있다.
    i = (int)ch;  // ❗ i = (int)'A'에서 현재 디폴트 값이 int이므로 형변환을 생략할 수 있다.
    
    
    //3-2. 다음 연산의 결과와 그 이유를 적으세요.
    class Exercise3_2{
    public static void main(String[] args){
        int x = 2;
        int y = 5;
        char c = 'A'; // 'A'의 문자코드는 65, 'Z'의 문자코드 90, 'C'의 문자코드 67

        System.out.println(y >= 5 || x < 0 && x > 2);  //❗️true
        // y>=5가 true, x < 0이 false, x>2가 false
        // 비교연산자는 &&의 우선순위가 높으므로 (true || (false && true)) -> (true || false) -> (true)
        System.out.println(y += 10 - x++);  //❗️13
        // y에 10을 더한 값에서 (아직 덧셈이 안 된) x를 뺀 값이므로 15-2 = 13
        System.out.println(x += 2);  //❗️5
        // 위의 x++로 인해 x가 3이 됐고 이 x에 2를 더한 수이므로 5
        System.out.println(!('A' <= c && c <= 'Z'));  //❗️false
        // 'A' <= c가 true, c <= 'Z'가 true, (true && true) -> (true)이지만 앞에 !를 붙였으므로 (false)로 반환
        System.out.println('C' - c);  //❗️2
        // 'C'의 문자코드는 67, 67 - 65이므로 2
        System.out.println('5' - '0');  //❗️5
        // 자동 형변환으로 인해 int('5') - int('0')이 되어 5-0=5
        System.out.println(c + 1);  //❗️66
        // 자동 형변환으로 인해 65 + 1 =66
        System.out.println(++c);  //❗️'B'
        // c인 'A' 보다 1큰 문자를 반환하므로 'B'
        System.out.println(c++);  //❗️'B'
        // c인 'B'를 반환하고 1큰 문자가 되기 때문에 'B'
        System.out.println(c);  //❗️'C'
        // 현재 c는 'B' 보다 1큰 문자가 되었으므로 'C'
            }
        }


    //3-3. 아래는 변수의 num 값 중에서 백의 자리 이하를 버리는 코드이다.
    //만일 변수 num의 값이 '456'이라면 '400'이 되고, '111'이라면 '100'이 된다.
    //알맞은 코드를 넣으시오.
            class Exercise3_3 {
                public static void main(String[] args){
                    int num = 456;
                    System.out.println((Math.round(num-50)/100)*100);
                }
            }
            // ❗️ 방법: 정수형으로 접근하기! 정수형으로 접근할 수 있는건 Math.round()밖에 안되니까
            // 일부 버리고 나누는 방법으로 하기!
    //예상 결과 -> 400

    //3-4. 아래의 코드는 사과를 담는데 필요한 바구니(버켓)의 수를 구하는 코드이다.
    //만일 사과의 수가 123개이고 하나의 바구니에는 10개의 사과를 담을 수 있다면, 13개의 바구니가 필요할 것이다.
    //알맞은 코드를 넣으시오.
            class Exercise3_4{
                public static void main(String[] args){
                    int numOfApples = 123; // 사과의 개수
                    int sizeOfBucket = 10; // 바구니의 크기(바구니에 담을 수 있는 사과의 개수)
                    int numOfBucket = Math.round((numOfApples+9)/sizeOfBucket); // 모든 사과를 담는데 필요한 바구니의 수

                    System.out.println("필요한 바구니의 수 :"+numOfBucket);
                }
            }
            // ❗️ 방법1. 올림의 개념으로 접근 이건.. 잘 안되네요..
            // ❗️ 방법2. 반올림 개념으로 접근 (numOfApples+9)/sizeOfBucket 실수를 정수로 반환하므로 +9를 해서 범위를 맞춰준다.
    //예상 결과 -> 필요한 바구니의 수 :13


    //3-5. 아래는 변수 num의 값에 따라 '양수', '음수', '0'을 출력하는 코드이다.
    //삼항연산자를 이용해서 빈칸에 알맞은 코드를 넣으시오.
    //Hint : 삼항 연산자를 두 번 사용할 것!
            class Exercise3_5{
                public static void main(String[] args){
                    int num = 10;
                    System.out.println(num<0?"음수":num>0?"양수":"0");
                }
            }
    //예상 결과 : 양수


    //3-6. 아래는 화씨(Fahrenheit)를 섭씨(Celcius)로 변환하는 코드이다.
    //변환 공식이 'C = 5/9*(F-32)'라고 할 때, 빈 칸에 알맞은 코드를 넣으시오.
    // 단, 변환값은 소수점 셋째자리에서 반올림하며, Math.round() 함수를 사용하지 않고 처리할 것!
            class Exercise3_6{
                public static void main(String[] args){
                    int fahrenheit = 100;
                    float celcius = (int)(((fahrenheit-32)*5*100)/9F+1)/100F;

                    System.out.println("Fahrenheit:"+fahrenheit);
                    System.out.println("Celcius:"+celcius);
                }
            }
        ❗️ 접근: 한 번 정수로 만들어주고 나눗셈을하여 소수로 만들어주기, 반올림이 안되니까 +1을 해보았다.
        ❗️ F를 이용해서 소수점 자리 표현을 하려고 했다.
        ❓ 왜 100을 곱해야했을까? 셋째자링메서 반올림을 한다했으니 자릿수는 둘째 자리까지 표현된다.

    ////예상 결과 : Fahrenheit:100, Celcius:37.78
    //    }
    //}
