## Laporan 30 Days of Code
---
### Day 28 : RegEx, Patterns, and Intro to Databases
#### Tujuan
belajar regular expressions.
#### Tugas
Pertimbangkan tabel basis data, Email, yang memiliki atribut Nama Depan dan ID Email. Diberikan sejumlah baris data yang mensimulasikan tabel Email, cetak daftar orang-orang yang dipesan secara alfabet yang alamat emailnya diakhiri dengan @gmail.com.
#### Format masuk
* Baris pertama berisi bilangan bulat, N, jumlah baris dalam tabel.
* Masing-masing dari N baris berikutnya berisi 2 string yang dipisahkan spasi yang menunjukkan nama depan dan ID email seseorang.
#### Kendala
* 1 ≤ N ≤ 30
- Setiap nama depan terdiri dari huruf kecil [a-z] hanya.
- Setiap ID email terdiri dari huruf kecil [a-z], @ dan . hanya.
- Panjang nama depan tidak lebih dari 20.
- Panjang ID email tidak lebih dari 50.
#### Format keluar
Cetak daftar nama depan yang disusun menurut abjad untuk setiap pengguna dengan akun gmail. Setiap nama harus dicetak pada baris baru.
#### Contoh input
```
6
riya riya@gmail.com
julia julia@julia.me
julia sjulia@gmail.com
julia julia@gmail.com
samantha samantha@gmail.com
tanya tanya@gmail.com
```
#### Contoh keluar
```
julia
julia
riya
samantha
tanya
```
#### source code
```
public class Solution {

    public static void main(String[] args) {
        Scanner sc=new Scanner(System.in);
        int N = sc.nextInt();
        String str=".@gmail\\.com$";//give pattern
        Pattern ptrn=Pattern.compile(str);//will compile pattern

        List<String> lst=new ArrayList();

        for (int a0 = 0; a0 < N; a0++) {
            String firstName = sc.next();

            String emailID = sc.next();
            Matcher matcher=ptrn.matcher(emailID);

            if(matcher.find()){
                //System.out.println(firstName);
                lst.add(firstName);
            }
        }
        Collections.sort(lst);//Sort all name
        for(String name:lst){
            System.out.println(name);
        }
    }
}
```
