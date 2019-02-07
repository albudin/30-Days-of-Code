## Laporan 30 Days of Code
---
### Day 4 : Class vs. Instance
#### Tujuan
Dalam tantangan ini diajarkan tentang perbedaan class dan Instance; karena ini adalah konsep OOP, itu hanya digunakan dalam bahasa tertentu.
#### Tugas
blablabla....
#### Format masuk
Masukkan diberikan editor.
baris pertama berisi bilangan bulat, `T`(jumlah kasus uji), dan `T` baris berikutnya masing-masing berisi bilangan bulat yang menunjukan usia Instance orang.  
#### Kendala
```
1 ≤ T ≤ 4
-5 ≤ age ≤ 30
```
#### Format keluar
Lengkapi definisi metode yang disediakan di editor sehingga memenuhi spesifikasi yang diuraikan di atas; kode untuk menguji pekerjaan Anda sudah ada di editor. Jika metode Anda diterapkan dengan benar, setiap test case akan dicetak 2 atau 3 baris (tergantung pada apakah valid diteruskan ke konstruktor) atau tidak.#### Contoh input
#### Contoh input
```
4
-1
10
16
18
```
#### Contoh keluar
```
Age is not valid, setting age to 0.
You are young.
You are young.

You are young.
You are a teenager.

You are a teenager.
You are old.

You are old.
You are old.
```
#### Penjelasan
uji kasus 0: initialAge = -1
karena initialAge < 0, code diatur batas 0 dan cetak "Age is not valid..."
dan selanjutnya...
#### Souce Code
```
public class Person {
    private int age;

	public Person(int initialAge) {
  		// Add some more code to run some checks on initialAge
          age = initialAge;
	}

	public void amIOld() {
  		// Write code determining if this person's age is old and print the correct statement:
          if(age<0){
              System.out.println("Age is not valid, setting age to 0.");
              age=0;
              System.out.println("You are young.");
          }
          else if(age<13){
              System.out.println("You are young.");
          }
          else if(age>=13 && age<18){
              System.out.println("You are a teenager.");
          }
          else{
              System.out.println("You are old.");
          }

	}

	public void yearPasses() {
  		// Increment this person's age.
        age++;
}
```
