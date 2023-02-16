<h1>프로그래머스 알고리즘 문제 풀기</h1>
<h3>핸드폰 번호 가리기</h3>

    //내가 푼 방식
    class Solution {
        public String solution(String phone_number) {
            String answer = "";
            int len = phone_number.length();
            String hidden = "";

            String show = phone_number.substring(len - 4);
            for (int i=0; i < len-4; i++){
                hidden += "*";
            }

            answer = hidden + show;

            return answer;
        }
    
    // 깔끔하게 푼 방식
    class Solution {
      public String solution(String phone_number) {
         char[] ch = phone_number.toCharArray();
         for(int i = 0; i < ch.length - 4; i ++){
             ch[i] = '*';
         }
         return String.valueOf(ch);
      }
    }

<h3>부족한 금액 계산하기</h3>

    // 내가 푼 방시
    class Solution {
    public long solution(int price, int money, int count) {
        long answer = -1;
        long result = 0;

        int cost = count*price;
        long totalCost = 0;
        for (int i= 0; i < count; i++){
            totalCost += (i+1)*price;
        }
        
        result = money-totalCost;
        if (result >= 0){
            answer = 0;
        } else {
            answer = Math.abs(result);
        }
        return answer;
    }
}
    
    // 다른 풀이
    class Solution {
        public long solution(int price, int money, int count) {
            long answer = -1;
            answer = (long)price*count*(count+1)/2 - money;
            return answer<=0?0:answer;
        }
    }
    
   // 깔끔
    class Solution {
        public long solution(long price, long money, long count) {
            return Math.max(price * (count * (count + 1) / 2) - money, 0);
        }
<h3>2016</h3>


<h3>나누어 떨어지는 숫자 배열</h3>


<h3>내적</h3>
내적: 성분끼리 곱한 값

        // 내가 푼 방법
        class Solution {
            public int solution(int[] a, int[] b) {
                int answer = 0;
                
                for (int i = 0; i < a.length; i++){
                        answer += a[i]*b[i];
                    }
                System.out.println(answer);
                return answer;
            }
        }


        
