## Laporan 30 Days of Code
---
### Day 3 : Intro to Conditional Statements
#### Tujuan
belajar tentang conditional Statements
#### Tugas
diberikan bilangan bulat n dengan kondisi:
* jika n adalah ganjil, cetak Weired
* jika n adalah genap dan dalam rentang inklusif 2 sampai 5, cetak Not Weired
* jika n adalah genap dan dalam rentang inklusif 6 sampai 20, cetak Weired
* jika n adalah genap dan lebih dari 20, cetak Not Weired
selainnya cetak Weired
#### Format masuk
satu baris yang mengandung bilangan bulat positif n
#### Kendala
`1 ≤ n ≤ 100`
#### Format keluar
cetak Weired jika nomor Weired; selainnya cetak Not Weired
#### Contoh input 0
`3`
#### Contoh keluar 0
`Weired`
#### Contoh input 1
`24`
#### Contoh keluar 1
`Not Weired`
#### Penjelasan
contoh kasus 0: n = 3
n ganjil dan ganjil adalah Weired, jadi cetak Weired
contoh kasus 1: n = 24
n > 20 dan n adalah genap, jadi bukan Weired. maka cetak Not Weired
#### Souce Code
```
public class Solution {

    //private static final Scanner scanner = new Scanner(System.in);

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int N = scanner.nextInt();
        //scanner.skip("(\r\n|[\n\r\u2028\u2029\u0085])?");
        if(N%2==0){
            if(N>=2 && N<=5){
                System.out.println("Not Weird");
            }
            else if(N>=6 && N<=20){
                System.out.println("Weird");
            }
            else{
                System.out.println("Not Weird");
            }
        }
        else{
            System.out.println("Weird");
        }

        //scanner.close();
    }
}
```
