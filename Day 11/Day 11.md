## Laporan 30 Days of Code
---
### Day 11 : 2D Arrays
#### Tujuan
belajar tentang Array dengan menambahkan dimensi lain.
#### Konteks
diberikan 6 x 6 2D Array, A:
```
1 1 1 0 0 0
0 1 0 0 0 0
1 1 1 0 0 0
0 0 0 0 0 0
0 0 0 0 0 0
0 0 0 0 0 0
```
Kami mendefinisikan hourglass menjadi bagian dari nilai dengan indeks jatuh dalam pola ini dalam representasi A grafis:
```
a b c
  d
e f g
```
Ada 16 hourglass dalam A, dan jumlah hourglass adalah jumlah nilai-nilai hourglass.
#### Tugas
Hitung jumlah hourglass untuk setiap hourglass di A, lalu cetak jumlah hourglass maksimum.
#### Format masuk
Ada 6 baris input, di mana setiap baris berisi bilangan bulat yang dipisahkan oleh ruang yang menggambarkan 2D Array A; setiap nilai dalam A akan berada dalam kisaran inklusif -9 hingga 9.
#### Kendala
```
-9 ≤ A[i][j] ≤ 9
0 ≤ i,j ≤ 5
```
#### Format keluar
Print the largest (maximum) hourglass sum found in `A`.
#### Contoh input
```
1 1 1 0 0 0
0 1 0 0 0 0
1 1 1 0 0 0
0 0 2 4 4 0
0 0 0 2 0 0
0 0 1 2 4 0
```
#### Contoh keluar
`19`
#### Penjelasan
 `A` contains the following hourglasses:
```
1 1 1   1 1 0   1 0 0   0 0 0
  1       0       0       0
1 1 1   1 1 0   1 0 0   0 0 0

0 1 0   1 0 0   0 0 0   0 0 0
  1       1       0       0
0 0 2   0 2 4   2 4 4   4 4 0

1 1 1   1 1 0   1 0 0   0 0 0
  0       2       4       4
0 0 0   0 0 2   0 2 0   2 0 0

0 0 2   0 2 4   2 4 4   4 4 0
  0       0       2       0
0 0 1   0 1 2   1 2 4   2 4 0
```
The hourglass with the maximum sum (19) is:
```
2 4 4
  2
1 2 4
```
#### source code
```
public class Solution {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int arr[][] = new int[6][6];
        for (int i = 0; i < 6; i++) {
            for (int j = 0; j < 6; j++) {
                arr[i][j] = scanner.nextInt();
            }
        }

        int sum = 0;
        int maxSum = Integer.MIN_VALUE;

        for (int i = 0; i < arr.length - 2; i++) {
            for (int j = 0; j < arr[0].length - 2; j++) {
                sum = arr[i][j] + arr[i][j + 1] + arr[i][j + 2] + arr[i + 1][j + 1] + arr[i + 2][j] + arr[i + 2][j + 1]
                        + arr[i + 2][j + 2];
                if (sum > maxSum) {
                    maxSum = sum;
                }
            }
        }
        scanner.close();
        System.out.println(maxSum);
    }
}
```
