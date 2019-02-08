## Laporan 30 Days of Code
---
### Day 26 : Nested Logic
#### Tujuan
Menguji pemahaman tentang pernyataan bersyarat yang bersarang
#### Tugas
Perpustakaan lokal membutuhkan bantuan untuk mengingat tanggal pengembalian yang diharapkan dan aktual untuk buku perpustakaan, buat program yang menghitung denda (jika ada). Struktur biaya adalah sebagai berikut:
1. Jika buku dikembalikan pada atau sebelum tanggal pengembalian yang diharapkan, tidak ada denda yang akan dikenakan (yaitu: denda=0).
2. Jika buku dikembalikan setelah hari pengembalian yang diharapkan tetapi masih dalam bulan dan tahun kalender yang sama dengan tanggal pengembalian yang diharapkan, denda = 15 hackos x berapa hari terlambat.
3. Jika buku dikembalikan setelah bulan pengembalian yang diharapkan tetapi masih dalam tahun kalender yang sama dengan tanggal pengembalian yang diharapkan, denda = 500 hackos x berapa bulan terlambat.
4. Jika buku dikembalikan setelah tahun kalender yang diharapkan, ada denda tetap sebesar 10000 hackos.
#### Format masuk
Baris pertama berisi 3 bilangan bulat pisah ruang yang menunjukkan masing-masing hari, bulan, dan tahun di mana buku itu benar-benar dikembalikan.
Baris kedua berisi 3 bilangan bulat pisah ruang yang menunjukkan masing-masing hari, bulan, dan tahun di mana buku itu diharapkan akan dikembalikan (tanggal jatuh tempo).
#### Kendala
```
1 ≤ D ≤ 31
1 ≤ M ≤ 12
1 ≤ Y ≤ 3000
dijamin bahwa tanggal tersebut akan menjadi tanggal kalender gregorian yang valid.
```
#### Format keluar
Cetak bilangan bulat tunggal yang menunjukkan denda perpustakaan untuk buku yang diterima sebagai input.
#### Contoh input
```
9 6 2015
6 6 2015
```
#### Contoh keluar
`45`
#### Penjelasan
Diberikan tanggal pengembalian berikut:
Sekarang  :9-6-2015
Diharapkan:6-6-2015
Karena tahunnya sama, kita tahu itu kurang dari satu tahun terlambat.
Karena bulannya sama, kita tahu itu terlambat kurang dari sebulan.
Karena harinya berbeda, kata tahu bahwa itu dikembalikan terlambat (tetapi masih dalam bulan dan tahun yang sama).
Sesuai struktur biaya perpustakaan, kami tahu bahwa denda kami akan menjadi 15 hackos x perhari terlambat. Kami kemudian mencetak hasil 15 x jumlah hari terlambat = 15 x (9 - 6) = 45 sebagai output kami.
#### source code
```
public class Solution {
    public static void main(String[] args) {
        Scanner sc=new Scanner(System.in);

        int d1 = sc.nextInt();
        int m1 = sc.nextInt();
        int y1 = sc.nextInt();
        int d2 = sc.nextInt();
        int m2 = sc.nextInt();
        int y2 = sc.nextInt();

        int fine;
        if (y1 > y2) {
            fine = 10000;
        } else if (m1 > m2 && (y1 >= y2)) {
            fine = 500 * (m1 - m2);
        } else if (d1 > d2 && (m1 >= m2) && (y1 >= y2)) {
            fine = 15 * (d1 - d2);
        } else {
            fine = 0;
        }
        System.out.println(fine);

        sc.close();
    }
}
```
