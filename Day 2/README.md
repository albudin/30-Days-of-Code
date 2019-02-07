## Laporan 30 Days of Code
---
### Day 2 : Operators
#### Tujuan
Belajar tentang operasi aritmatik
#### Tugas
Mengingat harga makanan (biaya pokok makanan), tip persen (persentase harga makanan ditambahkan sebagai tip), dan persen pajak (persentase harga makanan ditambahkan sebagai pajak) untuk makanan, menemukan dan mencetak total biaya makan.
Catatan: Pastikan untuk menggunakan nilai yang tepat untuk perhitungan Anda, atau Anda mungkin berakhir dengan hasil yang salah!
#### Format masuk
Ada 3 garis input numerik:
Baris pertama memiliki dobel, mealCost (biaya makan sebelum pajak dan tip).
Baris kedua memiliki bilangan bulat, tipPercent(persentase mealCost ditambahkan sebagai tip).
Baris ketiga memiliki bilangan bulat, taxPercent(persentase mealCost ditambahkan sebagai pajak).
#### Format keluar
Cetak total biaya makan, di mana totalCost adalah hasil bulat dari seluruh tagihan (mealCost dengan tambahan pajak dan tip).
#### Contoh input
```
12.00
20
8
```
#### Contoh keluar
`15`
#### Penjelasan
diberikan:
mealCost = 12, tipPercent = 20, taxPercent = 8
kalkulasi:
tip = 12 X 20/100 = 2.4
tax = 12 X 8/100 = 0.96
totalCost = mealCost + tip + tax = 12 + 2.4 + 0.96 = 15.36
round(totalCost) = 15
#### Souce Code
```
public class Day2 {
  // Complete the solve function below.
  static void solve(double meal_cost, int tip_percent, int tax_percent){
      int totalCost = 0;
      double tip , tax;
      tip = meal_cost * tip_percent / 100;
      tax = meal_cost * tax_percent / 100;
      totalCost = (int)(meal_cost + tip +tax);
      System.out.println("The total meal cost is "+totalCost+" dollars.");
      }

  private static final Scanner scanner = new Scanner(System.in);

  public static void main(String[] args) {
      double meal_cost = scanner.nextDouble();
      scanner.skip("(\r\n|[\n\r\u2028\u2029\u0085])?");

      int tip_percent = scanner.nextInt();
      scanner.skip("(\r\n|[\n\r\u2028\u2029\u0085])?");

      int tax_percent = scanner.nextInt();
      scanner.skip("(\r\n|[\n\r\u2028\u2029\u0085])?");

      solve(meal_cost, tip_percent, tax_percent);

      scanner.close();
  }
}
```
