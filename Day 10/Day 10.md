## Laporan 30 Days of Code
---
### Day 10 : Binary Numbers
#### Tujuan
belajar tentang angka biner
#### Tugas
Diberikan integer basis-10, `n`, ubah menjadi biner (basis-2). Kemudian temukan dan cetak bilangan bulat basis-10 yang menunjukkan jumlah maksimum representasi biner 1 berturut-turut dalam n.
#### Format masuk
A single integer, `n`.
#### Kendala
`1 ≤ n ≤ 10^6`
#### Format keluar
Cetak bilangan bulat basis-10 tunggal yang menunjukkan jumlah maksimum 1 berturut-turut dalam representasi biner dari `n`.
#### Contoh input 1
`5`
#### Contoh keluar 1
`1`
#### Contoh input 2
`13`
#### Contoh keluar 2
`2`
#### Penjelasan
Contoh Kasus 1:
Representasi biner 5 dari adalah 101, jadi jumlah maksimum 1 berturut-turut adalah 1.

Contoh Kasus 2:
Representasi biner 13 dari 1101 adalah, jadi jumlah maksimum 1 berturut-turut adalah 2.
#### source code
```
public class Solution {

    public static void main(String[] args) {
        Scanner scanner =new Scanner(System.in);
        int n = scanner.nextInt(),m=0,num=0;

        String b=Integer.toString(n,2);
        char[] c=b.toCharArray();

        for(int i=0;i<c.length;i++)
        {
            if(c[i]=='1')
            {
                num++;
            }
            else
            {
                num=0;
            }

            if(m<num){
                m=num;
            }
        }
        System.out.println(m);
    }
}
```
