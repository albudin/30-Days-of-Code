## Laporan 30 Days of Code
---
### Day 7 : Arrays
#### Tujuan
Belajar tentang struktur data array.
#### Tugas
Diberikan array, `A`,` N` dari bilangan bulat, cetak elemen `A's` dalam urutan terbalik sebagai satu baris angka yang dipisahkan oleh spasi.
#### Format masuk
Baris pertama berisi bilangan bulat `N`, (ukuran array yang diberikan).
Baris kedua berisi `N` integer yang dipisahkan spasi yang menjelaskan elemen-elemen `A's` array.
#### Kendala
```
1 ≤ N ≤ 1000
2 ≤ Ai ≤ 10000, dimana Ai adalah intejer ke i di array.
```
#### Format keluar
Cetak elemen larik `A` dalam urutan terbalik sebagai satu baris angka yang dipisahkan oleh spasi.
#### Contoh input
```
4
1 4 3 2
```
#### Contoh keluar
`2 3 4 1`
#### source code
```
public class Solution {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int n = scanner.nextInt();
        int[] arr = new int[n];
        for(int i=0; i<n;i++){
            arr[i] = scanner.nextInt();
        }
        for(int j=n-1;j>=0;j--){
            System.out.print(arr[j]+" ");
        }
        scanner.close();
```
