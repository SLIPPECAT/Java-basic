<h1>Report8</h1>
7-1.<br>
섯다카드 20장을 포함하는 섯다카드 한 벌(SutdaDeck클래스)을 정의한 것이다. <br>
섯다카드 20장을 담는 SutdaCard배열을 초기화하시오.<br>
단, 섯다카드는 1부터 10까지의 숫자 가 적힌 카드가 한 쌍씩 있고, 숫자가 1, 3, 8인 경우에는 둘 중의 한 장은 광(Kwang)이 어야 한다. <br>
즉, SutdaCard의 인스턴스변수 isKwang의 값이 true이어야 한다.<br>

    class SutdaDeck {
        final int CARD_NUM = 20;
        SutdaCard[] cards = new SutdaCard[CARD_NUM];

        SutdaDeck() {
            // (구현) 배열 SutdaCard를 적절히 초기화 하시오.
        }
    }

    class SutdaCard {
        int num;
        boolean isKwang;

        SutdaCard() {
            this(1, true);
        }

        SutdaCard(int num, boolean isKwang) {
            this.num = num;
            this.isKwang = isKwang;
        }

        // info()대신 Object클래스의 toString()을 오버라이딩했다. 
        public String toString() {
            return num + ( isKwang ? "K":""); 
        }
    }

    class Exercise7_1 {
        public static void main(String args[]) {
            SutdaDeck deck = new SutdaDeck();

            for (int i = 0; i < deck.cards.length; i++)
                System.out.print(deck.cards[i] + ",");
        }
    }
    // 예상결과) 1K,2,3K,4,5,6,7,8K,9,10,1,2,3,4,5,6,7,8,9,10,
    
7-2. 연습문제 7-1. 의 SutdaDeck클래스에 다음에 정의된 새로운 메서드를 추가하고 테스트 하시오.<br>
[주의] Math.random()을 사용하는 경우 실행결과와 다를 수 있음.<br>
메서드명 : shuffle<br>
기 능 : 배열 cards에 담긴 카드의 위치를 뒤섞는다.(Math.random()사용)<br>
반환타입 : 없음<br>
매개변수 : 없음<br>
메서드명 : pick<br>
기 능 : 배열 cards에서 지정된 위치의 SutdaCard를 반환한다. <br>
반환타입 : SutdaCard<br>
매개변수 : int index - 위치<br>
메서드명 : pick<br>
기 능 : 배열 cards에서 임의의 위치의 SutdaCard를 반환한다.(Math.random()사용) <br>
반환타입 : SutdaCard<br>
매개변수 : 없음<br>
        class SutdaDeck {
            final int CARD_NUM = 20;
            SutdaCard[] cards = new SutdaCard[CARD_NUM];

            SutdaDeck() {
                 // 연습문제 7-1 의 답이므로 내용생략
            }

            void shuffle() {
                 // (구현)
            }

            SutdaCard pick(int index) {
                 // (구현)
            }

            SutdaCard pick() {
                 // (구현)
            }
        } // SutdaDeck

        class SutdaCard { 
            int num;
            boolean isKwang;

            SutdaCard() { 
                this(1, true);
            }

            SutdaCard(int num, boolean isKwang) { 
                this.num = num;
                this.isKwang = isKwang; 
            }

            public String toString() {
                return num + ( isKwang ? "K":"");
            } 
        }

        class Exercise7_2 {
            public static void main(String args[]) {
                SutdaDeck deck = new SutdaDeck();

                System.out.println(deck.pick(0)); 
                System.out.println(deck.pick()); 
                deck.shuffle();

                for(int i=0; i < deck.cards.length;i++) 
                    System.out.print(deck.cards[i]+",");

                System.out.println();
                System.out.println(deck.pick(0)); 
            }
        }
        //예상결과) 
        // 1K
        // 7 
        // 2,6,10,1K,7,3,10,5,7,8,5,1,2,9,6,9,4,8K,4,3K, 
        // 2

7-3. 다음의 코드는 컴파일하면 에러가 발생한다. 그 이유를 설명하고 에러를 수정하기 위해서는 코드를 어떻게 바꾸어야 하는가?
    <br>
7-4. MyTv클래스의 멤버변수 isPowerOn, channel, volume을 클래스 외부에서 접근할 수 없도록 제어자를 붙이고 대신 이 멤버변수들의 값을 어디서나 읽고 변경할 수 있도록 getter와 setter메서드를 추가하라.

7-5. 문제7-4에서 작성한 MyTv2클래스에 이전 채널(previous channel)로 이동하는 기능 의 메서드를 추가해서 실행결과와 같은 결과를 얻도록 하시오.<br>
[Hint] 이전 채널의 값을 저장할 멤버변수를 정의하라.<br>
메서드명 : gotoPrevChannel <br>
기 능 : 현재 채널을 이전 채널로 변경한다. <br>
반환타입 : 없음 <br>
매개변수 : 없음 <br>
    
