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
    // ❗️ 순서를 표현식으로 최대한 구현하려고 해보자
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
