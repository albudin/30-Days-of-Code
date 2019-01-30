## Laporan 30 Days of Code
---
### Day 9 : Recursion 3
#### Tujuan
mempelajari dan mempraktikkan konsep algoritmik yang disebut Rekursi
#### Metode Rekursif untuk Menghitung Faktorial
```
factorial(N)={1                     N≤1
              N x factorial(N-1)    otherwise
```
#### Tugas
Tulis fungsi faktorial yang mengambil bilangan bulat positif, `N` sebagai parameter dan mencetak hasil dari` N! (N faktorial) .`
Catatan: Jika Anda gagal menggunakan rekursi atau gagal menyebutkan fungsi rekursif faktorial atau Faktorial, Anda akan mendapatkan skor `0`.
#### Format masuk
Integer tunggal, `N` (argumen untuk diteruskan ke faktorial).
#### Kendala
```
2 ≤ N ≤ 12
Kiriman Anda harus mengandung fungsi rekursif bernama faktorial.
```
#### Format keluar
Cetak bilangan bulat tunggal yang menunjukkan `N!`.
#### Contoh input
`3`
#### Contoh keluar
`6`
#### source code
```
public class Solution {

    public static void main(String[] args){
        Scanner scanner =new Scanner(System.in);

        int n = scanner.nextInt();
        int result = factorial(n);
        System.out.println(result);
    }
    public static int factorial(int n){
        if(n==0){
            return 1;
        }else{
            return n*factorial(n-1);
        }
    }

}
```
