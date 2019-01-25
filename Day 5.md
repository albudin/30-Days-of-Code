## Laporan 30 Days of Code

### Day 5 : Loops
#### Tujuan
menggunakan loop untuk membantu menyelesaiakan matematika sederhana.
#### Tugas
diberikan bilangan bulat, `n`, cetak kelipatan `10` pertamanya. setiap kelipatan `n x i(dimana 1 ≤ i ≤ 10)` harus dicetak dibaris baru dalam bentuk: `n x i = hasil`
#### Format masuk
bilangan bulat tunggal, `n`
#### Kendala
`2 ≤ n ≤ 20`
#### Format keluar
cetak `10` baris keluaran; setiap baris `i (dimana 1 ≤ i ≤ 10  )` berisi dari dalam bentuk `n x i` dalam form:`n x i = hasil`
#### Contoh input
`2`

#### Contoh keluar
```
2 x 1 = 2
2 x 2 = 4
2 x 3 = 6
2 x 4 = 8
2 x 5 = 10
2 x 6 = 12
2 x 7 = 14
2 x 8 = 16
2 x 9 = 18
2 x 10 = 20
```
#### source code
```
import java.io.*;
import java.math.*;
import java.security.*;
import java.text.*;
import java.util.*;
import java.util.concurrent.*;
import java.util.regex.*;

public class Solution {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int n = scanner.nextInt();
        //scanner.skip("(\r\n|[\n\r\u2028\u2029\u0085])?");
        for(int i=1;i<=10;i++){
            System.out.println(n+" x "+i+" = "+n*i);
        }

        //scanner.close();
    }
}
```
