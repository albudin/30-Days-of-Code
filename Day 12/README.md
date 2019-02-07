## Laporan 30 Days of Code
---
### Day 12 : Inheritance
#### Tujuan
belajar tentang Inheritance
#### Tugas
Anda diberi dua kelas, Person dan Siswa, di mana Person adalah kelas dasar dan Siswa adalah kelas turunan. Kode lengkap untuk Orang dan pernyataan untuk Siswa disediakan untuk Anda di editor. Perhatikan bahwa Siswa mewarisi semua properti Person.
Lengkapi kelas Siswa dengan menulis yang berikut:
Konstruktor kelas siswa, yang memiliki 4 parameter:
String firstName dan lastName, dan Integer id dan score.
Metode kalkulasi char() yang menghitung rata-rata objek Siswa dan mengembalikan perwakilan karakter kelas dari rata-rata yang dihitung:
`Grading Scale`

| Letter | Average(a) |
| - | - |
| O | 90 ≤ a ≤ 100 |
| E | 80 ≤ a ≤ 90 |
| A | 70 ≤ a ≤ 80 |
| P | 55 ≤ a ≤ 70 |
| D | 40 ≤ a ≤ 55 |
| T | a < 40 |
#### Format masuk
Kode rintisan yang terkunci di editor Anda memanggil konstruktor kelas Siswa Anda dan meneruskannya dengan argumen yang diperlukan. Itu juga memanggil metode penghitungan (yang tidak membutuhkan argumen).
Anda tidak bertanggung jawab untuk membaca input berikut dari stdin:
Baris pertama masing-masing berisi firstName, lastName, dan id. Baris kedua berisi jumlah skor tes. Baris ketiga bilangan bulat bertingkat ruang menjelaskan skor.
#### Kendala
```
1 ≤ |firstName|,|lastName| ≤ 10
|id| ≡ 7
0 ≤ score,average ≤ 100
```
#### Format keluar
Ini ditangani oleh kode rintisan yang terkunci di editor Anda. Output Anda akan benar jika konstruktor kelas Siswa Anda dan metode menghitung () diimplementasikan dengan benar.
#### Contoh input
```
Heraldo Memelli 8135627
2
100 80
```
#### Contoh keluar
```
Name: Memelli, Heraldo
 ID: 8135627
 Grade: O
```
#### source code
```
class Student extends Person{
	private int[] testScores;
    private int sum=0;
    double avg;

    Student(String fn,String ln,int id,int []testScore){
        super(fn,ln,id);
        this.testScores=testScore;
    }

    char calculate(){
        for(int i=0;i<testScores.length;i++){
            sum+=testScores[i];
        }
        avg=sum/(testScores.length);

        if(avg>=90){
            return 'O';
        }
        else if(avg>=80){
            return 'E';
        }
        else if(avg>=70){
            return 'A';
        }
        else if(avg>=55){
            return 'P';
        }
        else if(avg>=40){
            return 'D';
        }
        else{
            return 'T';
        }
    }
}
```
