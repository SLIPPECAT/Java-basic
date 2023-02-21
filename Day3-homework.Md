<h1>Report5</h1>

    //6-1. 다음과 같은 멤버 변수를 갖는 Student 클래스를 정의하세요.
    //타입 : String, 변수명 : name, 설명 : 학생 이름
    //타입 : int, 변수명 : ban, 설명 : 반
    //타입 : int, 변수명 : no, 설명 : 번호
    //타입 : int, 변수명 : kor, 설명 : 국어 점수
    //타입 : int, 변수명 : eng, 설명 : 영어 점수
    //타입 : int, 변수명 : math, 설명 : 수학 점수

    class Student{
        String name;  // 학생이름
        int ban;  // 반
        int no;  // 번호
        int kor;  // 국어 점수
        int eng;  // 영어 점수
        int math;  // 수학 점수
    }
    // 설명 어떻게 해야하는지 몰라서 주석처리로 적어두었습니다..
    
    class Exercise6_2 {
            public static void main(String[] args) {
                Student s = new Student("홍길동", 1, 1, 100, 60, 76);

                String str = s.info();
                System.out.println(str);
            }// 예상 결과 : 홍길동, 1, 1, 100, 60, 76, 236, 78.7
        }
        class Student {
            String name;  // 학생이름
            int ban;  // 반
            int no;  // 번호
            int kor;  // 국어 점수
            int eng;  // 영어 점수
            int math;  // 수학 점수

            String info() {
                return name + ", " + ban + ", " + no + ", " + kor + ", " + eng + ", " + math+", "+getTotal()+", "+getAverage();
            }

            Student(String name, int ban, int no, int kor, int eng, int math) {
                this.name = name;
                this.ban = ban;
                this.no = no;
                this.kor = kor;
                this.eng = eng;
                this.math = math;
            }
            int getTotal(){
                return this.kor+this.eng+this.math;
            }
            float getAverage(){
                return (float) Math.round(getTotal()*10/3f)/10;
            }
        }
        
    class Exercise6_3 {
            public static void main(String args[]) {
                Student s = new Student();
                s.name = "홍길동";
                s.ban = 1;
                s.no = 1;
                s.kor = 100;
                s.eng = 60;
                s.math = 76;
                System.out.println("이름 :"+s.name);
                System.out.println("총점 :"+s.getTotal());
                System.out.println("평균 :"+s.getAverage());
            }//예상 결과 : 이름 : 홍길동, 총점 : 236, 평균 : 78.7
        }
        class Student {
            String name;  // 학생이름
            int ban;  // 반
            int no;  // 번호
            int kor;  // 국어 점수
            int eng;  // 영어 점수
            int math;  // 수학 점수

            int getTotal(){
                return this.kor+this.eng+this.math;
            }
            float getAverage(){
                return (float) Math.round(getTotal()*10/3f)/10;
            }
        }
        
    //6-5. 다음의 코드에 정의된 변수들을 종류별(클래스 변수,인스턴스 변수, 지역변수)로 구분해서 적으세요.
        class PlayingCard {
            int kind;  ❗️인스턴스 변수
            int num;  ❗️인스턴스 변수
            static int width;  ❗클래스 변수️
            static int height;  ❗️클래스 변수
            PlayingCard(int k, int n) {
                kind = k;  ❗️지역변수
                num = n;  ❗️지역변수
            }
            public static void main(String args[]) {
                PlayingCard card = new PlayingCard(1,1);
            }
        }
        
    //6-7. 다음은 컴퓨터 게임의 병사(marine)를 클래스로 정의한 것이다.
        //이 클래스의 멤버 중에 static을 붙여야 하는 것은 어떤 것들이고 그 이유는 무엇인가?
        //(단, 모든 병사의 공격력과 방어력은 같아야 한다.)
        class Marine {
            int x=0, y=0; //Marine의 위치좌표 (x,y)
            int hp = 60; //현재 체력
            int weapon = 6; //공격력
            int armor = 0; //방어력
            void weaponUp() {
                weapon++;
            }
            void armorUp() {
                armor++;
            }
            void move(int x, int y) {
                this.x = x;
                this.y = y;
            }
        }
        ❗️ static int weapon, static int armor 일 것 같습니다. 
         생성될 때부터 모든 Marine들의 공격력과 방어력이 동일한 값을 갖고 시작해야하기 때문입니다.
