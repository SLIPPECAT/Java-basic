<h1>조건문과 반복문</h1>
플로우 차트<br>
1. 직선형: 시작부터 종료 명령까지 단계적으로 진행되는 순서<br>
2. 분기형: 조건에 따라 실행 순서를 달리하는 형태<br>
3. 반복형: 조건을 만족할 때까지 일정한 내용을 반복 수행하는 형태<br>
내가 그린 플로우 차트 => 블로그 참고<br>
<h2>IF</h2>
<h3>if</h3>

    if (조건식) { 조건식의 결과가 true일 때 실행하고자 하는 문장; }
<h3>if-else</h3>

    if (조건식) { 조건식의 결과가 true일 때 실행하고자 하는 문장; }<br>
      else { 조건식의 결과가 false일 때 실행하고자 하는 문장; }<br>
<h3>if-else if-else</h3>

    if (조건식1) { 조건식1의 결과가 true일 때 실행하고자 하는 문장; }<br>
      else if (조건식2) { 조건식 2의 결과가 true일 때 실행하고자 하는 문장; }<br>
        else { 조건식1의 결과도 false이고 조건식2의 결과도 false일 때 실행하고자 하는 문장; }<br>
    ⭐️ 여러 개의 조건식을 포함한 조건식, else if가 여러번 사용될 수 있다. 마지막 else 블럭은 생략 가능하다.
<h3>중첩 if</h3>

    if (조건식1) { 조건식1의 결과가 true일 때 실행하고자 하는 문장; <br>
      if (조건식2) { 조건식1과 조건식2의 결과가 모두 true일 때 실행하고자 하는 문장; } <br>}
          else { 조건식1의 결과가 true이고 조건식 2의 결과가 거짓일 때 실행하고자 하는 문장; <br>}}
      else { 조건식1의 결과가 false일 때 실행하고자 하는 문장; }
<h3>블록 {}</h3>

'여러 문장을 하나로 묶어주는 것'<br>
만약 if 조건문에서 실행할 문장이 하나라면 if(조건식) 명령문; 이렇게 {}가 생략될 수 있다.<br>
조건식 예시(str.equals("yes"), str.equalsIgnoreCase("yes")<br>
<h2>SWITCH</h2>
<h3>switch</h3>

        switch (조건식) {
            case값1:
                조건식의 결과가 값1과 같은 경우 수행할 문장;
                    break;
            case값2:
                조건식의 결과가 값22와 같을 경우 수행할 문장;
                    break;
            ......
            
            default: 
                조건식의 결과와 일치하는 case 문장이 없을 때 수행할 문장;
                }
처리해야 하는 경우의 수가 많을 때 유용한 조건문<br>               
break;를 작성해 주지 않으면 switch 문 끝까지 실행<br>
default 문은 생략 가능<br>
if는 조건식 결과에 true/false만 가능하고 switch는 정수나 문자열만 가능<br>
break;를 만나거나 switch 문이 끝나면 switch 문 전체를 빠져나간다.
<h3>switch문의 제약 조건</h3>
1. switch문의 조건식 결과가 정수 또는 문자열 이어야 한다.<br>
2. case문의 값은 정수 상수(문자 포함), 문자열만 가능하며, 중복되지 않아야 한다.<br>
<h2>FOR</h2>
<h3>for</h3>

        for (초기화;조건식;증감식){
            조건식의 결과가 참인 동안 반복적으로 실행하고자 하는 문장; }<br>
        실행순서 1. 초기화 2. 조건식 3. 조건식이 참일 경우 문장 수행 4. 증감식 5. 조건식이 거짓일 될 때까지 반복
        
        //초기화 할 때 변수 2개 사용 가능하지만 타입이 같아야 한다.
        for (int i = 1, j = 10; i <= 10; i++, j--) {
        System.out.println("i는 현재 " + (i) + "입니다.");
        System.out.println("j는 현재 " + (j) + "입니다."); }
        
        //초기화 할 때 변수 2개 사용 가능하지만 타입이 같아야 한다.
        for (int k = 1, t = 10; k <= 10 && t > 2; k++, t--) {
        System.out.println("k는 현재 " + (k) + "입니다.");
        System.out.println("t는 현재 " + (t) + "입니다."); }

        
<h3>중첩 for</h3>

        for (초기화;조건식1;증감식) {
            조건식1의 결과가 true인 동안 반복적으로 실행하고자 하는 문장;
            for (초기화;조건식2;증감식){
                조건식2의 결과가 true인 동안 반복적으로 실행하고자 하는 문장;}}
<h3>향상된 for</h3>

        for ('타입' '변수이름': 배열 or 컬렉션) {
            배열 or 컬렉션의 길이만큼 반복적으로 실행하고자 하는 문장; }
        
        int[] arr = new int[]{1, 2, 3, 4, 5};
        for (int e : arr) {
            System.out.print(e + " ");}
<h2>임의의 정수 만들기</h2>

        Math.random() -> 0.0과 1.0 사이의 임의의 double 값을 반환합니다.
        0.0 < Math.random() < 1.0
        
<h3>1부터 5사이의 random한 정수 값구하기</h3>
1. 0.0 * 5 <= Math.random() * 5 < 1.0 * 5<br>
2. (int)0.0 <= (int)(Math.random() * 5) < (int)5.0<br>
3. 0 + 1 <= (int)(Math.random() * 5) + 1 < 5 + 1<br>
4 <= (int)(Math.random() * 5) + 1 < 6<br>

<h2>WHILE</h2>
<h3>while</h3>

        while (조건식) {
            조건식의 결과가 true인 동안 반복적으로 실행하고자 하는 문장; }
        실행 순서 1. 조건식 2. 조건식이 참일 경우 문장 수행 3. 조건식이 거짓이 될 때까지 반복
<h3>do-while</h3>
        
        do { 조건식의 결과가 true인 동안 반복적으로 실행하고자 하는 문장;}
        while (조건식);
        실행 순서 1. 처음 한 번은 무조건 실행 2. 조건식 3. 조건식이 참일 경우 문장 수행 4. 조건식이 될 때가지 반복
❗️ while문과 do-while문의 차이점: while문은 한 번도 실행이 안될수도 있다. do-while문은 한 번은 꼭 실행한다.<br>
어떤 때 이런 걸 쓸 수 있을까? 쓰더라도 if문으로 대체할 수 있을 것 같은데

<h2>배열</h2>
<h3>배열의 길이와 초기화</h3>
자신이 포함된 하나의 반복문을 벗어납니다.
<h3>continue</h3>
자신이 포함된 반복문의 끝으로 이동<br>
그리고 다음 반복으로 넘어간다.<br>
전체 반복 중에서 특정 조건시 반복을 건너뛸 때 유용하다.
<h3>이름붙은 반복문</h3>
<h2>배열</h2>
<h3>배열</h3>
배열은 같은 타입의 여러 변수를 하나의 묶음으로 다루는 것
<h3>배열의 선언과 생성</h3>
배열의 선언: 배열을 다루기 위한 참조변수의 선언<br>
선언 방법: 아래 두가지 방법 모두 지원<br>
1. 타입[] 변수이름; ex. int[] age;, String[] name;<br>
2. 타입 변수이름[]: ex. int age[];, String name[];<br>
배열의 생성: 실제 저장공간을 생성<br>
타입[] 변수이름 = new 타입[길이];
int[] age;  :int 타입의 배열을 다루기 위한 참조변수 age 선언<br>
age = new int[5];  int 타입의 값 5개를 저장할 수 있는 배열을 생성(new)<br>
배열의 시작 주소(메모리 주소)가 참조변수 age에 저장되었습니다.<br>
age는 지정된 주소를 통해 해당 배열을 가리키고 있습니다.<br>
즉, 참조변수와 배열이 연결되었고 우리는 참조변수를 이용해 배열을 다룰 수 있습니다.<br>
<h3>배열의 인덱스</h3>
각 요소(저장공간)에 자동으로 붙는 일련 번호<br>
인덱스의 범위는 0부터 '배열길이-1'까지!<br>
요소는 저장공간이고 인덱스는 주소 저장공간의 주소 같은 것? <br>
age[3] = 28;, age의 4번째 요소에 28을 저장 <br>
int beatitudoAge = age[3];, 배열 age의 4번째 요소의 값을 읽어서 beautitudoAge 변수에 저장<br>
<h1>배열</h1>
<h2>배열의 길이와 초기화</h2>
<h3>배열의 길이</h3>
⭐️ 배열이름.length
배열의 길이: int 타입 상수<br>
int[] arr = new int[5];  : 배열의 길이가 5인 int 배열<br>
int len = arr.length;  : arr.lenght의 값은 5이고 len 변수에 저장된다.<br>
❗️ 배열은 한 번 생성되면 컴파일 후 실행되는 동안은 그 길이(크기)를 바꿀 수 없다.<br>
<h3>배열의 한계점</h3>
❓ 배열의 크기를 바꿀 수 없는 이유?<br>
new int[5];로 배열을 생성하면 intrk 4byte이기 때문에 총 20byte를 저장하기 위한 연속적인 메모리 공간을 찾고<br>
연속적인 공간을 찾아서 주소를 배정한다.<br>
배정이 끝난 후 크기를 5가 아닌 10으로 늘려야 한다고 가정하면, 배정받은 주소 뒤에 20byte를 추가적으로 배정해야 하는데<br>
뒤에 연속적인 메모리 공간이 존재한다는 보장이 없고 그래서 크기를 바꿀 수 없다.<br>
⭐️ 배열의 크기가 부족할 때의 방법<br>
필요한 만큼의 크기의 배열을 새롭게 만든다.<br>
새로 만든 배열에 기존 배열의 값을 복사해서 저장한다.(어떻게 구현되는 거지?)<br>
<h3>배열의 초기화</h3>
배열의 각 요소에 처음으로 값을 저장하는 것을 의미<br>
⭐️ 기본값: byte, short, int는 0, long은 0L, float은 0.0f, double은 0.0d, char는 \n0000, boolean은 false, 참조형은 null<br>
배열은 기본적으로 저장하려는 값의 타입의 기본값으로 자동 초기화해준다.<br>
⭐️ 초기화 방법<br>

        1. int[] num = new int[]{1,2,3,4,5,6,7,8,9}<br>
        2. int[] num = {1,2,3,4,5,6,7,8,9}  new int[]를 생략할 수 있다.<br>
        3.      int[] num4;
                num4 = new int[]{1,2,3,4,5,6,7,8,9};
        3과 같은 경우에는 new int[]를 생략할 수 없다.
<h2>배열 연습하기</h2>
<h3>배열의 출력</h3>

        int[] arr = {100, 90, 80, 70, 60, 50, 40, 30, 20, 10};
        //  배열을 가리키는 참조 변수 arr 을 출력
        System.out.println("arr = " + arr);
        // 메모리 주소와 비슷한 문자열이 출력 -> 실제 주소는 아닙니다.
        // [I@7a81197d -> [(배열을 뜻함), I(int 타입을 뜻함), @(위치를 뜻함)
        ❓ 만약에 arr를 모두 한 번에 보고 싶을 경우에는 어떻게 하지?
        
        System.out.println("arr = " + arr);        
        import java.util.Arrays;
        System.out.println("Arrays.toString(arr) = " + Arrays.toString(arr));
        // [100, 90, 80, 70, 60, 50, 40, 30, 20, 10] 
<h3>총합과 평균</h3>
평균을 구할 때, float avg = of; 초기화하고 시작하며 값은 소수점 6째자리 수까지 나왔다.
<h3>❗️❗️❗️랜덤으로 숫자 섞기 헷갈린다</h3>
<h2>String배열</h2>
<h3>String 클래스</h3>

        char[] 와 메서드(기능)를 결합한 것<br>
        기본형처럼 사용이 가능한 참조형<br>
                String str = "행복";<br>
                String str = new String("행복");<br>
        문자열을 많이 사용하기 때문에 특별하게 만들어진 클래스이다.<br>
        String 클래스는 내용을 변경할 수 없다. 새로운게 만들어진다.<br>
                String name = "choi";
                String firstname = "wb";
                name = name + firstname
<h3>스트링 클래스의 주요 메서드</h3>

        char charAt(index). 문자열에서 해당 위치(index)에 있는 문자를 반환
        int lenght()  문자열의 길이를 반환
        String substring(int from, int to)  문자열에서 해당 범위의 문자열을 반환(to는 포함 안됨)
                                            인덱스가 하나만 적혀있을 경우 해당 인덱스부터 마지막까지 반환
        boolean equals(Object obj)  문자열의 내용이 같은지 확인하여 같으면 true, 다르면 false
        char[] toCharArray()  문자열을 문자배열(char[])로 변환해서 반환
<h3>String 배열의 선언과 생성</h3>
        
        String[] name = new String[3];
        참조형 이기 대문에 기본값 null로 초기화
        지금까지 것과 관련 없는 3개의 문자열을 담을 수 있는 String 배열이 생성된 것이다.

<h2>2차원 배열</h2>
테이블 형태의 데이터를 저장하기 위한 배열
<h3>2차원 배열의 선언과 생성</h3>

    int[][] score = new int[4][3]
    score[0][0] = 88;
    배열 score의 1행 1열에 88을 저장한다.
<h3>2차원 배열의 초기화</h3>

int[][] score = new int[][]{{},{},{},{}};
int[][] score = {{},{},{},{}};
❗️ 향상된 for 부분 이해가 조금 어렵다.
        System.out.println();
        // 출력 예 3 : 향상된 for
        System.out.println("향상된 for");
        for (int[] ints : score) {
            for (int it : ints) {
                System.out.println("anInt = " + it);
            }
            System.out.println();
<h2>Arrays</h2>
<h3>문자열 비교와 출력</h3>
equals(), toString()

        Arrays.toString(num) = [0, 1, 2]
        Arrays.deepToString(score) = [[88, 35, 100], [84, 60, 55], [100, 99, 72], [33, 54, 77]]
        1차원 비교는 equals, 다차원 비교는 deepEquals
        
<h3>배열 복사</h3>
copyOf(), copyOfRange()

        int[] arr2 = Arrays.copyOf(arr, arr.length);
        System.out.println("Arrays.toString(arr2) = " + Arrays.toString(arr2));
        int[] arr3 = Arrays.copyOf(arr, 3);
        System.out.println("Arrays.toString(arr3) = " + Arrays.toString(arr3));
        int[] arr4 = Arrays.copyOf(arr, 7); // 범위가 넘어가는 복사는 초기화값이 들어간다.
        System.out.println("Arrays.toString(arr4) = " + Arrays.toString(arr4));
        int[] arr5 = Arrays.copyOfRange(arr, 2, 4);
        System.out.println("Arrays.toString(arr5) = " + Arrays.toString(arr5));
        int[] arr6 = Arrays.copyOfRange(arr, 0, 7);// 범위가 넘어가는 복사는 초기화값이 들어간다.
        System.out.println("Arrays.toString(arr6) = " + Arrays.toString(arr6));
<h3>정렬</h3>
sort()

        Arrays.sort(arr); // 오름차순으로 정렬됩니다.
