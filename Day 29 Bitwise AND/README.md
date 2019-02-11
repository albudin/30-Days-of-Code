## Laporan 30 Days of Code
---
### Day 29 : Bitwise AND
#### Tujuan
belajar tentang operasi Bitwise
#### Tugas
Diberikan set *S* = {1,2,3,...,*N*}. Temukan dua bilangan bulat, *A* dan *B* (di mana *A < B*), dari set *S* sedemikian rupa sehingga nilai *A&B* maksimum yang mungkin dan juga kurang dari bilangan bulat yang diberikan, *K*. Dalam hal ini, mewakili bitwise AND operator.
#### Format masuk
* Baris pertama berisi bilangan bulat,*T*, jumlah kasus uji.
* Masing-masing baris *T* berikutnya mendefinisikan kasus uji sebagai bilangan bulat yang dipisahkan oleh 2 ruang, *N* dan *K*, masing-masing.
#### Kendala
```
1 ≤ T ≤ 10^3
2 ≤ N ≤ 10^3
2 ≤ K ≤ N
```
#### Format keluar
Cetak nilai maximum yang mungkin dari *A & B* dalam baris baru.
#### Contoh input
```
3
5 2
8 5
2 2
```
#### Contoh keluar
```
1
4
0
```
#### Penjelasan
*N* = 5, *K* = 2, *S* = {1,2,3,4,5}
semua nilai yang mungkin A dan B adalah:
1. A = 1, B = 2; A&B = 0
2. A = 1, B = 3; A&B = 1
3. A = 1, B = 4; A&B = 0
4. A = 1, B = 5; A&B = 1
5. A = 2, B = 3; A&B = 2
6. A = 2, B = 4; A&B = 0
7. A = 2, B = 5; A&B = 0
8. A = 3, B = 4; A&B = 0
9. A = 3, B = 5; A&B = 1
10. A = 4, B = 5; A&B = 4
maximum yang mungkin A&B juga <(K = 2) adalah 1, jadi kita cetak 1 dalam baris baru.
#### source code
```
public class Solution {

    public static void main(String[] args) {
        Scanner sc=new Scanner(System.in);
        int t = sc.nextInt();
        int max;
        for (int a0 = 0; a0 < t; a0++) {
            int n = sc.nextInt();
            int k = sc.nextInt();
            max=0;

            for(int i=1;i<=n;i++){
                for(int j=i+1;j<=n;j++){
                    if((i&j)<k){
                        if((i&j)>max){
                            max=(i&j);
                        }
                    }
                }
            }System.out.println(max);
        }
    }
}
```
