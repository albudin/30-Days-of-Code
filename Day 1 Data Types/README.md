## Laporan 30 Days of Code
---
### Day 1 : Data Types
#### Tujuan
pembahasan tentang tipe data
#### Tugas
Lengkapi kode di editor di bawah ini. Variabel i,d, dan s sudah dinyatakan dan diinisialisasi. Kamu harus:
1. Menyatakan 3 variabel: satu tipe int, satu double, dan satu tipe String.
2. Baca baca 3 baris input dari stdin (sesuai dengan urutan yang diberikan di bagian Format Input di bawah) dan inisialisasi Anda
variabel.
3. Menggunakan + operator untuk melakukan operasi berikut:
  1. Cetak jumlah i ditambah variabel int Anda di baris baru.
  2. Cetak jumlah d ditambah variabel ganda Anda ke skala satu tempat desimal pada baris baru.
  3. Menggabungkan s dengan string yang Anda baca sebagai input dan cetak hasilnya pada baris baru.
#### Format masuk
Baris pertama berisi bilangan bulat yang harus dijumlahkan dengan i.
Baris kedua berisi double yang harus dijumlahkan dengan d.
Baris ketiga berisi string yang harus Anda gabungkan dengan s.
#### Format keluar
Cetak jumlah dari kedua bilangan bulat pada baris pertama, jumlah dari kedua dobel (diskalakan 1 ke tempat desimal) pada baris kedua, dan kemudian dua string bersambung pada baris ketiga.
#### Contoh input
```
12
4.0
is the best place to learn and practice coding!
```
#### Contoh keluar
```
16
8.0
HackerRank is the best place to learn and practice coding!
```
#### Penjelasan
Ketika kita menjumlahkan bilangan bulat 4 dan 12, kita mendapatkan bilangan bulat 16.
Ketika kita menjumlahkan angka floating-point 4.0 dan 4.0, kita dapatkan 8.0.
Ketika kami menggabungkan HackerRank dengan adalah tempat terbaik untuk belajar dan berlatih coding !, kami mendapatkan HackerRank adalah tempat terbaik untuk belajar dan berlatih coding!.
#### Souce Code
```
    public static void main(String[] args) {
        int i = 4;
        double d = 4.0;
        String s = "HackerRank ";

        Scanner scan = new Scanner(System.in);

        /* Declare second integer, double, and String variables. */
        int i2;
        double d2;
        String s2;

        /* Read and save an integer, double, and String to your variables.*/
        i2=scan.nextInt();
        d2=scan.nextDouble();
        s2=scan.next();
        s2+=scan.nextLine();
        // Note: If you have trouble reading the entire String, please go back and review the Tutorial closely.

        /* Print the sum of both integer variables on a new line. */
        System.out.println(i+i2);

        /* Print the sum of the double variables on a new line. */
        System.out.println(d+d2);

        /* Concatenate and print the String variables on a new line;
        	the 's' variable above should be printed first. */
        System.out.println(s+s2);

        scan.close();
    }
}
```
