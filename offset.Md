    package Section2;

    import java.io.File;
    import java.util.Scanner;

    public class Code21 {
        static int n;
        static int[][]grid;   // 2차원 배열
        public static void main(String[] args) {
            try {
                Scanner inFile = new Scanner(new File("data.text"));
                n = inFile.nextInt();
                grid = new int[n][n];
                for (int i = 0; i < n; i++) {
                    for (int j = 0; j < n; j++) {
                        grid[i][j] = inFile.nextInt();
                    }
                }
                inFile.close();
                for (int x = 0; x < n; x++) {
                    for (int y = 0; y < n; y++) {
                        for (int dir = 0; dir < 8; dir++) {
                            for (int length = 1; length <= n; length++) {
                                int value = computeValue(x, y, dir, length);
                                // 시작위치 (x,y)에서 dir 방향으로 길이가 length인 수열을 정수로
                                // 환산하여 반환하고 만약 그런 수열이 존재하지 않으면 -1을 반환하라.
                                if (value != -1 && isPrime(value))
                                    // 존재하지 않는 수열에 대해 -1로 지정해주기
                                    System.pritnln(value);
                            }
                        }
                    }
                }
            } catch (FileNotFoundException e){
                e.printStackTrace();
            }
            }

        // computeValue 함수 만들기
        public static computeValue(int x, int y, int dir, int len) {
            int value = 0;
            for (int i = 0; i < len; i++) {
                int digit = getDigit(x, y, dir, i);
                // 시작위치 (x,y)에서 dir 방향으로 I칸 떨어진 자리에 있는 digit반환
                // 마냥 그런 자리가 존재하지 않으면 -1을 반환
                if (digit == -1)
                    return -1;
                value = value * 10 + digit;
            }
            return value;
        }
        static int[]offsetX = {0,1,1,1,0,-1,-1,-1};
        static int[]offsetY = {-1,-1,0,1,1,1,0,-1};
        public static int getDigit(int x, int y, int dir, int k){
            int newX = x + k*offsetX[dir];
            int newY = y + k*offsetX[dir];
            if (newX < 0 || newX >= grid.length || newY < 0 || newY <= grid.length)
                return -1;
            else
                return grid[newX][newY];
        }
    }
        public static int getDigit(int x, int y, int dir, int k){
            int newX = x, newY = y;
            switch(dir) {
                // 각 숫자는 방향
                case 0:
                    newY -= k;
                    break;
                case 1:
                    newX += k;
                    newY -= k;
                    break;
                case 2:
                    newX += k;
                    break;
                case 3:
                    newX += k;
                    newY += k;
                    break;
                case 4:
                    newY += k;
                    break;
                case 5:
                    newX -= k;
                    newY += k;
                    break;
                case 6:
                    newX -= k;
                    break;
                case 7:
                    newX -= k;
                    newY -= k;
                    break;
            }
            if (newX < 0 || newX >= n || newY < 0) || newY >=n)
                return -1;
            return grid[newX][newY];
            }
