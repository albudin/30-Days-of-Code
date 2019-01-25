## Laporan 30 Days of Code

### Day 2 : 
#### Tujuan
Dalam tantangan ini diajarkan tentang
#### Tugas
blablabla....
#### Format masuk
blablabla....
#### Kendala
blablaba...
#### Format keluar
blablaba...
#### Contoh input
blablabla...
#### Contoh keluar
blablaba...
#### Souce Code
```
package DaysCode30;

/**
 *
 * @author 1413101039
 */
import java.io.*;
import java.math.*;
import java.security.*;
import java.text.*;
import java.util.*;
import java.util.concurrent.*;
import java.util.regex.*;
public class Day2 {

  // Complete the solve function below.
  static void solve(double meal_cost, int tip_percent, int tax_percent){
      int totalCost = 0;
      double tip , tax;
      tip = meal_cost * tip_percent / 100;
      tax = meal_cost * tax_percent / 100;
      totalCost = (int)(meal_cost + tip +tax);
      System.out.println("The total meal cost is "+totalCost+" dollars.");
      }

  private static final Scanner scanner = new Scanner(System.in);

  public static void main(String[] args) {
      double meal_cost = scanner.nextDouble();
      scanner.skip("(\r\n|[\n\r\u2028\u2029\u0085])?");

      int tip_percent = scanner.nextInt();
      scanner.skip("(\r\n|[\n\r\u2028\u2029\u0085])?");

      int tax_percent = scanner.nextInt();
      scanner.skip("(\r\n|[\n\r\u2028\u2029\u0085])?");

      solve(meal_cost, tip_percent, tax_percent);

      scanner.close();
  }
}
```
