```
import java.util.*;

public class Main {
    public static void main(String[] args) {
        // 自分の得意な言語で
        // Let's チャレンジ！！
        Scanner sc = new Scanner(System.in);
        int buy = sc.nextInt();
        int sale = sc.nextInt();
        int free = sc.nextInt();
        List<Integer> cart = new ArrayList<>();
        int total = 0;

        for (int i = 0; i < buy; i++) {
            int price = sc.nextInt();
            total += price;
            cart.add(price);
        }

        if (buy >= sale) {
            for (int i = 0; i < free; i++) {
                int minPrice = Collections.min(cart);
                total -= minPrice;
                cart.remove((Integer) minPrice);
            }
        }
        System.out.println(total);
    }
}
```
