<h1>Report3</h1>

    //4-1. 다음의 문장들을 조건식으로 표현해보세요.
    //int형 변수 x가 10보다 크고 20보다 작을 때 true인 조건식  ❗️10 < x && x <20
    //char형 변수 ch가 공백이나 탭이 아닐 때 true인 조건식  ❗!(ch==' ' && ch=='\t')
    //char형 변수 ch가 'x' 또는 'X'일 때 true인 조건식  ❗ch=='x' || ch=='X'
    //char형 변수 ch가 숫자('0'~'9')일 때 true인 조건식  ❗'0'<= ch && ch <='9'
    //char형 변수 ch가 영문자(대문자 또는 소문자)일 때 true인 조건식  ❗('a' <= ch && ch <= 'z') || ('A' <= ch && ch <= 'Z')
    //int형 변수 year가 400으로 나눠떨어지거나 또는 4로 나눠떨어지고 100으로 나눠떨어지지 않을때 true인 조건식  ❗(year%400 == 0 || year%4 == 0) && year%100 != 0
    //boolean형 변수 powerOn이 false일 때 true인 조건식  ❗ powerOn == false
    //문자열 참조변수 str이 "yes"일 때 true인 조건식  ❗  str=="yes"
        
        
        //4-2. 1부터 20까지의 정수중에서 2 또는 3의 배수가 아닌 수의 총합을 구하세요.
        class Exercise4_2 {
            public static void main(String[] args) {
                int sum = 0;
                for (int i = 1; i < 21; i++)
                    if (i % 2 != 0 && i % 3 != 0)
                        sum += i;
                System.out.println("sum=" + sum);
            }
        }
        
        //4-3. 1+(1+2)+(1+2+3)+(1+2+3+4)+...+(1+2+3+...+10)의 결과를 계산하세요.
        class Exercise4_3 {
            public static void main(String[] args) {
                int sum = 0;
                int totalSum = 0;
                for (int i = 1; i <= 10; i++) {
                    sum += i;
                    totalSum += sum;
                    System.out.println("Sum=" + sum);
                    System.out.println("totalSum=" + totalSum);
                }
            }
        }
        
        
        //4-4. 1+(-2)+3+(-4)+...과 같은 식으로 계속 더해나갔을 때,
        //몇까지 더해야 총합이 100 이상이 되는지 구하세요.
        class Exercise4_4 {
        public static void main(String[] args) {
        int sum = 0; // 총합을 저장할 변수
        int s = 0; // 값의 부호를 바꿔주는데 사용할 변수
        int num =0;

        for (int i = 0; i <1000; i++) {
            num += 1;
            if (num % 2 == 0) {
                s = -num;
            } else {
                s = num;
            }
            sum += s;
            if (sum == 100) {
                System.out.println("num=" + num);
                System.out.println("sum=" + sum);
            }
        }
        }
        }
        
        
        //4-5. 다음의 for문을 while문으로 변경하세요.
        class Exercise4_5 {
            public static void main(String[] args) {
                int i = 0;
                while(i <= 10) {
                    int j = 0;
                    while (j <= i) {
                        System.out.print("*");
                        j += 1;
                    }
                    i += 1;
                    System.out.println();
                }
            }//end of main
        } // end of class
        
        //4-6. 두 개의 주사위를 던졌을 때, 눈의 합이 6이 되는 모든 경우의 수를 출력하는 프로그램을 작성하세요.
        class Exercise4_6 {
            public static void main(String[] args) {
                    int result = 0;
                    for (int a=1; a<=6; a++){
                        for (int b=1; b<=6; b++){
                            result = a+b;
                            if (result == 6){
                                System.out.println("a는"+a+"b는"+b+"입니다.");
                            }
                    }
                     }
                }
            }

        
       
        //4-7. 숫자로 이루어진 문자열 str이 있을 때, 각 자리의 합을 더한 결과를 출력하는 코드를 완성하세요.
        //만일 문자열이 "12345"라면, ‘1+2+3+4+5’의 결과인 15를 출력이 출력되어야 합니다.
        class Exercise4_7 {
            public static void main(String[] args) {
                String str = "12345";
                int sum = 0;
                for (int i = 0; i < str.length(); i++) {
                    sum += (str.charAt(i)-'0');
                    System.out.println("sum=" + sum);
                }
            }
        }//예상 결과 : sum=15
        
        //4-8. Math.random()을 이용해서 1부터 6 사이의 임의의 정수를 변수 value에 저장하는 코드를 완성하세요.
        class Exercise4_8{
            public static void main(String[] args) {
                for (int i = 0; i < 20; i++) {
                    int value = (int) (Math.random() * 6 + 1);
                    System.out.println("value:" + value);
                }
            }
        }
        
        //4-9. int 타입의 변수 num이 있을 때, 각 자리의 합을 더한 결과를 출력하는 코드를 완성하세요.
        //만일 변수 num의 값이 12345라면, ‘1+2+3+4+5’의 결과인 15를 출력하세요.
        //문자열로 변환하지 말고 숫자로만 처리하세요.
        class Exercise4_9 {
            public static void main(String[] args) {
                int num = 12345;
                int sum = 0;
                for (int i = 0; i <5; i++){
                    sum += num/(int)(Math.pow(10, i))%10;
                }
                System.out.println("sum="+sum);
            }
        }//예상 결과 : sum=15
        
        ❗️교재에서 이용한 방법.깔끔하다..
        //4-9. int 타입의 변수 num이 있을 때, 각 자리의 합을 더한 결과를 출력하는 코드를 완성하세요.
        //만일 변수 num의 값이 12345라면, ‘1+2+3+4+5’의 결과인 15를 출력하세요.
        //문자열로 변환하지 말고 숫자로만 처리하세요.
        class Exercise4_9 {
            public static void main(String[] args) {
                int num = 0 ,sum = 0;
                while(num != 0) {
                    sum += num%10;
                    num /= 10;
                }
                System.out.println("각 자리수의 합: "+sum);
            }
        }//예상 결과 : sum=15
        
        //4-10. 다음은 숫자맞추기 게임을 작성한 것이다. 1과 100사이의 값을 반복적으로 입력해서
        //컴퓨터가 생각한 값을 맞추면 게임이 끝난다.
        //사용자가 값을 입력하면, 컴퓨터는 자신이 생각한 값과 비교해서 결과를 알려준다.
        //사용자가 컴퓨터가 생각한 숫자를 맞추면 게임이 끝나고 몇 번 만에 숫자를 맞췄는지 알려준다.
         class Exercise4_10 {
            public static void main(String[] args) {
                // 1~100사이의 임의의 값을 얻어서  answer에 저장한다.

                int answer = (int)(Math.random()*100+1);
                int input = 0; //사용자입력을 저장할 공간
                int count = 0; //시도횟수를 세기위한 변수
                System.out.println(answer);
                // 화면으로 부터 사용자입력을 받기 위해서 Scanner클래스 사용
                java.util.Scanner s = new java.util.Scanner(System.in);
                do {
                    count++;
                    System.out.print("1과 100사이의 값을 입력하세요 : ");
                    input = s.nextInt(); //입력받은 값을 변수 input에 저장한다.
                } while(input != answer); //무한반복문
                System.out.println(count);
            } // end of main
        } // end of class
        

<h1>Report4</h1>

        ////5-1. 다음은 배열을 선언하거나 초기화한 것이다. 잘못된 것을 고르고 그 이유를 설명하세요.
        int[] arr[];  ❗️변수 arr이 선이되지 않았다.
        int[] arr = {1,2,3,};  
        int[] arr = new int[5];  
        int[] arr = new int[5]{1,2,3,4,5};  ❗new int[]의 5를 비워줘야 하거나 {1,2,3,4,5}를 뺴야한다.
        int arr[5];  ❗ 이렇게 하면 변수 arr이 초기화되지 않는다.
        int[] arr[] = new int[3][];  ❗변수 선언을 이렇게 할 수 없다.
        
        //////5-2. 다음과 같은 배열이 있을 때, arr[3].length의 값은?
        int[][]arr ={
        {5,5,5,5,5},
        {10,10,10},
        {20,20,20,20},  ❗️arr에서 3번째 값을 가져오는 것이므로 {20,20,20,20}이고 그 lengths는 4이다.
        {30,30}
        };

        class Exercise5_3 {
            public static void main(String[] args) {
                int[] arr = {10, 20, 30, 40, 50};
                int sum = 0;

                for (int i = 0; i <arr.length; i++){
                    sum += arr[i];
                }
                System.out.println("sum="+sum);
            }
        }
        //}//예상 결과 : sum=150
        
        
        //////5-4. 2차원 배열 arr에 담긴 모든 총합과 평균을 구하는 프로그램을 완성하세요.
        class Exercise5_4 {
            public static void main(String[] args) {
                int[][] arr = {
                        { 5, 5, 5, 5, 5 },
                        { 10, 10, 10, 10, 10 },
                        { 20, 20, 20, 20, 20 },
                        { 30, 30, 30, 30, 30 }
                };
                int total = 0;
                float average = 0;
                for (int i = 0; i < arr.length; i++) {

                    for (int j =0; j < arr[i].length; j++){
                        total += arr[i][j];
                    }
                    average = total/(float)arr[i].length;
                }
                System.out.println("total=" + total);
                System.out.println("average=" + average);
            } // end of main*/
        } // end of class
        
        //5-5. 다음은 1과 9 사이의 중복되지 않은 숫자로 이루어진 3자리 숫자를 만들어내는 프로그램이다.
        //코드를 완성하세요. 다만 Math.random()을 사용했기 때문에 실행 결과 예시와 다를 수 있습니다.
        class Exercise5_5{
            public static void main(String[] args) {
                int[] ballArr = { 1, 2, 3, 4, 5, 6, 7, 8, 9 };
                int[] ball3 = new int[3];

                // 배열 ballArr의 임의의 요소를 골라서 위치를 바꾼다
                for (int i = 0; i < ballArr.length; i++) {
                    int j = (int) (Math.random() * ballArr.length);
                    int tmp = ballArr[0];
                    ballArr[0] = ballArr[j];
                    ballArr[j] = tmp;
                    ball3 = Arrays.copyOf(ballArr, 3);
                }
                    for (int i = 0; i < ball3.length; i++) {
                        System.out.print(ball3[i]);
                }
            }//end of main
        }//end of class
        
        
        //5-6. 단어의 글자위치를 섞어서 보여주고 원래의 단어를 맞추는 예제이다.
        //실행결과와 같이 동작하도록 빈 칸을 채우세요.
        import java.util.Scanner;

        class Exercise5_13 {
            public static void main(String args[]) {
                String[] words = { "television", "computer", "mouse", "phone" };

                Scanner scanner = new Scanner(System.in);

                for (int i = 0; i < words.length; i++) {
                    char[] question = words[i].toCharArray(); // String을 char[]로 변환
                    int n = (int)(Math.random()*question.length);
                    char tmp = question[0];
                    question[0] = question[n];
                    question[n] = tmp;

                    System.out.printf("Q%d. %s의 정답을 입력하세요 .>", i + 1, new String(question));
                    String answer = scanner.nextLine();

                    // trim()으로 answer의 좌우 공백을 제거한 후, equals로 word[i]와 비교
                    if (words[i].equals(answer.trim()))
                        System.out.printf("맞았습니다.%n%n");
                    else
                        System.out.printf("틀렸습니다.%n%n");
                }
            } //end of main
        }//end of class
