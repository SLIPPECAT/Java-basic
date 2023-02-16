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
FF
    // 

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
