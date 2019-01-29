## Laporan 30 Days of Code
---
### Day 6 : Let's Review
#### Tujuan
perluas penggunaan String dan loop yang telah dipelajari
#### Tugas
Diberikan string, `S`, dengan panjang` N` yang diindeks dari `0` ke `N-1`, mencetak karakter yang diindeks genap dan diindeks ganjil sebagai 2 string yang dipisahkan oleh ruang pada satu baris (lihat Contoh di bawah untuk lebih detail).

Catatan: `0` dianggap sebagai indeks genap.
#### Format masuk
Baris pertama berisi bilangan bulat, `T` (jumlah kasus uji). Setiap baris `i` dari `T` baris berikutnya berisi String, `S`.
#### Kendala
```
1 ≤ T ≤ 10
2 ≤ length of S ≤ 10000
```
#### Format keluar
Untuk setiap String `Sj (di mana 0 j T-1)`, cetak karakter `Sj's` diindeks genap, diikuti oleh spasi, diikuti oleh karakter` Sj's` yang diindeks ganjil.
#### Contoh input
```
2
Hacker
Rank
```
#### Contoh keluar
```
Hce akr
Rn ak
```
#### Penjelasan
Test Case `0`: `S = "Hacker"`
```
S[0] = "H"
S[1] = "a"
S[2] = "c"
S[3] = "k"
S[4] = "e"
S[5] = "r"
```
Indeks genap adalah `0`,` 2`, dan `4`, dan indeks ganjil adalah` 1`, `3`, dan `5`. Kami kemudian mencetak satu baris string yang dipisahkan oleh ruang; string pertama berisi karakter yang diurutkan dari `S's` indeks genap (Hce), dan string kedua berisi karakter yang diurutkan dari `S's` indeks ganjil (akr).

Test Case `1`: `S = "Rank"`
```
S[0] = "R"
S[1] = "a"
S[2] = "n"
S[3] = "k"
```
Indeks genap adalah `0` dan `2`, dan indeks ganjil adalah `1` dan `3`.Kami kemudian mencetak satu baris string `2` yang dipisahkan spasi; string pertama berisi karakter yang diurutkan dari indeks `S's` genap (Rn), dan string kedua berisi karakter yang diurutkan dari indeks ganjil `S's` (ak).
#### source code
```
public class Solution {

    public static void main(String[] args) {
        /* Enter your code here. Read input from STDIN. Print output to STDOUT. Your class should be named Solution. */
        Scanner sc = new Scanner(System.in);
        int i,t,l,j;
        String e="",o="";

        t=sc.nextInt();

        String[]s= new String[t];

        for(i=0;i<t;i++)
        {
            s[i]=sc.next();
            l=s[i].length();
            char c[]=s[i].toCharArray();
            for(j=0;j<l;j++)
            {
                if(j%2==0)
                {
                    e+=c[j];
                }
                else
                {
                    o+=c[j];
                }
            }
            System.out.println(e+" "+o);
            e="";o="";
        }
    }
}
```
