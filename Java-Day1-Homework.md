<h3>Report1</h3>

    // 2-4. 다음 중 변수를 잘못 초기화 한 것은?
    byte b = 256;  ❗️ byte는 -128~127의 범위내에서 저장 가능하다.
    char c = ''; ❗️ char는 빈 문자를 선언할 수 없다.
    char answer = 'no'; ❗ char는 한 문자만을 선언할 수 있다.
    float f = 3.14  ❗ 리터럴과 타입이 일치하지 않으므로 3.14뒤에 f를 붙이거나 float을 double로 바꾸어 줄 수 있다.
    double d = 1.4e3f;


    //2-7. 다음 문장들의 출력 결과를 적으세요. 오류가 있는 문장의 경우, '오류' 라고 적으세요.
    System.out.println("1" + "2");  // 12
    System.out.println(true+"");  // true
    System.out.println('A' + 'B');  // AB
    System.out.println('1' + 2);  // 12
    System.out.println('1' + '2');  // 12
    System.out.println('J' +"ava");  // Java
    System.out.println(true + null);  // 오류 연산자를 boolean에 적용할 수 없다.


    //2-8. 아래는 변수 x, y, z의 값을 서로 바꾸는 예제이다. 결과와 같이 출력되도록 코드를 넣으세요.
    public class Exercise2_8{
        public static void main(String[] args){
            int x = 1;
            int y = 2;
            int z = 3;
           /*int tmp = x;
              x=y;
              y=z;
              z=tmp;
           */
            System.out.println("x="+x);
            System.out.println("y="+y);
            System.out.println("z="+z);
        }
    }
    //예상 결과 : x=2, y=3, z=1

<h3>Report2</h3>

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
        short s = (short)ch;  // 형변환을 생력할 수 없다. s는 short 타입의 숫자를 나타내고 ch는 char 타입의 문자이므로 형변환을 해주어야 한다.
    float f = (float)l;  // ❗️f는 float타입이고 l은 long타입인데 float타입의 범위가 더 넓으므로 float는 형변환 생략을 할 수 있다.
    i = (int)ch;  // ❗ i = (int)'A'에서 현재 디폴트 값이 int이므로 형변환을 생략할 수 있다.
    
    
    //3-2. 다음 연산의 결과와 그 이유를 적으세요.
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
