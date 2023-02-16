<h1>변수, 배열, 반복문</h1>

<h3></h3>
    
    // 클래스와 변수
    public class Code01 {
        static int num;
        public static void main(String[] args){
            int anotherNum = 5;
            num  = 2;

            System.out.println(num + anotherNum);
            System.out.println("Num: " + num);
            System.out.println("AnotherNum: " + anotherNum);
            System.out.println("Sum " + num + anotherNum);  // left associativity
        }
    }

    // 입력 받는 법
    import java.util.Scanner;  // import 할 것들
        public class Code02
        {
            public static void main(String[] args){
                int number = 123;
                Scanner kb = new Scanner(System.in);  // kb라는 이름의 스캐너 생성
                System.out.print("Please enter an integer: ");
                int input = kb.nextInt();
                if(input == number ) {
                    System.out.println("numbers match! : -)");
                } else {
                    System.out.println("Numbers do not match! :-(");
                }
                kb.close();
            }
        }

    // input.next(), input.netxInt(), .equals (문자열비교)
    import java.util.Scanner;
    public class Code04 {
        public static void main(String[] args) {
            String name = null;
            int age;
            String gender;

            Scanner keyboard = new Scanner(System.in);

            System.out.print("Please type your name and your age and your gender: ");
            name = keyboard.next();
            age = keyboard.nextInt();
            gender = keyboard.next();

            if(gender.equalsIgnoreCase("male"))  //string literal
            {
                System.out.println(name + ", you're "+age+" years old man.");
            } else if (gender.equalsIgnoreCase("female")){
                System.out.println(name + ", you're "+age+" years old woman.");
            }
            keyboard.close();
        }
    }

    // 배열
    import java.util.Scanner;
    
    public class Code06 {
        public static void main(String[] args){
            int[] grades;
            grades = new int[5];  // variable length array

            Scanner kb = new Scanner(System.in);
            int n = kb.nextInt();
            int[] array = new int[n];

            grades[0] = 100;
            grades[1] = 76;
            grades[2] = 92;
            grades[3] = 95;
            grades[4] = 14;
            int i = 0;
            while(i < grades.length){
                System.out.println("Grade "+(i+1)+":"+grades[i]);
                i++;
            }
        }
    }

    // 사용자로부터 n개의 정수를 입력 받아 합과 최대값 구하기
    import java.util.Scanner;

    public class Code08 {
        public static void main(String[] args){
            Scanner kb = new Scanner((System.in));
            System.out.println("정수의 개수를 입력해주세요.");
            int n = kb.nextInt();
            int[]data = new int[n];
            for (int i = 0; i < n; i++)  // 왜 여기 중괄호 안치지?
                data[i] = kb.nextInt();
                kb.close();

            int sum = 0;
            int max = data[0];  // data[0]처럼 하나를 지정해주는 것!
            for (int i = 0; i < n; i++){
                sum += data[i];
                if (data[i] > max)
                max = data[i];
            }
            System.out.println(max);
            System.out.println("The sum is: "+sum);
            }
        }

    // n개의 정수를 입력받아 순서대로 배열에 저장하기, 
    // 그 다음 모든 정수들을 오른쪽으로 한 칸씩 이동 마지막 정수는 배열의 첫 칸으로 이동(Circular shift)
    // ❗️ 순서를 표현식으로 최대한 구현하려고 해보자, 꼭 앞에서부터 시작하지 않아도 된다.
    // ❗️ for문에 조건을 달아서 빠져나오게 할 수도 있다.
    import java.util.Scanner;

    public class Code09 {
        public static void main(String[] args) {
            Scanner kb = new Scanner(System.in);
            System.out.println("n개의 정수를 입력해주세요.");
            int n = kb.nextInt();
            int[] arr = new int[n];
            for (int i = 0; i < n; i++) {
                arr[i] = kb.nextInt();
            }
            kb.close();

            int tmp = arr[n-1];
            for (int i = n-2; i >= 0; i--) {
                arr[i+1] = arr[i];
                System.out.println(arr[i]);
            }
            arr[0] = tmp;
            System.out.println(arr[0]);
        }
    }
    
    // 1~10만 사이의 모든 소수들을 찾아서 출력하기
    // ❗️ 소수(prime)에 대한 개념, 어디까지 나눠줄 수 있는가... i*i표현
    // ❗️ for문을 끝까지 돌지 않아도 된다.
    public class Code10 {
        public static void main(String[] args) {
            // 소수인지 아닌지 검사, 굉장히 중요한 문제 중의 하나!
            // 2, 3, ..., n-1
            // n-1까지 안가도 n/2까지만 가도 된다.
            // n/2까지도 안가도 되고 root(n) sqrt(n)까지만 가도 된다.
            // i < sqrt(n) 이건 계산이 어려우니까
            // i제곱 < n
            for (int n = 2; n <= 100000; n++){
                boolean isPrime = true;
                for (int i =2; i*i <= n && isPrime ; i++){
                    if(n % i == 0){
                        isPrime = false;  //not prime
    //                break;
                    }
                }
                if(isPrime){
                    System.out.println(n+"은 소수입니다.");
                }
            }
        }
    }

    // n개의 정수를 받고, 중복된 쌍의 개수를 출력하기
    // ❗️ 모든 쌍을 검사, 쌍으로 검사할 때는 중첩 for문을 이용하자!
    import java.util.Scanner;

    public class Code11 {
        public static void main(String[] args){  //main method (=function)
            Scanner kb = new Scanner(System.in);
            int n = kb.nextInt();
            int[]data = new int[n];

            for (int i = 0; i < n; i++){
                data[i] = kb.nextInt();
            }
            kb.close();

            int count = 0;
            for (int i =0; i < n; i++){
                for (int j = i+1; j < n; j++){
                    if(data[i] == data[j]){
                        count ++;
                    }
                }
            }
            System.out.println(count);
        }
    }
    
    // 문제: n개의 정수를 입력받아 배열에 저장하고 0개 이상의 연속된 정수들을 더하여 얻을 수 있는 최대값 구하기
<h3></h3>

<h3></h3>

<h3></h3>

<h3></h3>

<h3></h3>

<h3></h3>

<h3></h3>

<h3></h3>



<h1></h1> 
<h1></h1>
<h1></h1>
