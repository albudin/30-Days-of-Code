## Laporan 30 Days of Code
---
### Day 25 : Running Time and Complexity
#### Tugas
Prime adalah bilangan alami yang lebih besar dari 1 yang tidak memiliki pembagi positif selain dan itu sendiri. Diberi nomor, n, tentukan dan cetak apakah itu Prime atau Not prime.
#### Format masuk
Baris pertama berisi bilangan bulat, T, jumlah kasus uji.
Setiap T baris berikutnya berisi bilangan bulat, n, untuk diuji primality.
#### Kendala
```
1 ≤ T ≤ 30
1 ≤ n ≤ 2 x 10^9
```
#### Format keluar
kasus test, cetak n adalah Prime atau Not prime dalam satu baris
#### Contoh input
```
3
12
5
7
```
#### Contoh keluar
```
Not prime
Prime
Prime
```
#### Penjelasan
uji kasus 0: n = 12.
12 dapat dibagi dengan angka selain 1 dan dia sendiri (mis:2,3,6), jadi kami mencetak Not prime pada baris baru.
uji kasus 1: n = 5.
5 hanya dapat dibagi 1 dan dia sendiri, jadi cetak prime dalam baris baru
uji kasus 2: n = 7.
7 hanya dapat dibagi 1 dan dia sendiri, jadi cetak prime dalam baris baru 
#### source code
```
public class Solution {

    public static boolean isPrime(int n){
        for (int i=2;i<=Math.sqrt(n);i++){
            if(n%i==0){
            return false;
            }
        }
        return true;
    }

    public static void main(String[] args){
        Scanner in=new Scanner(System.in);
        int T=in.nextInt();

        for (int i=0;i<T;i++) {
            int n=in.nextInt();

            if (n>=2 && isPrime(n))
                System.out.println("Prime");
            else
                System.out.println("Not prime");
        }

        in.close();
    }
}
```
