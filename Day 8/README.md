## Laporan 30 Days of Code
---
### Day 8 : Dictionaries and Maps
#### Tujuan
belajar tentang pemetaan pasangan Nilai-kunci menggunakan struktur data Peta atau Kamus.
#### Tugas
Diberikan `n` nama dan nomor telepon, kumpulkan buku telepon yang memetakan nama teman ke nomor telepon masing-masing. Anda kemudian akan diberi jumlah nama yang tidak diketahui untuk meminta buku telepon Anda. Untuk setiap nama yang ditanyakan, cetak entri yang terkait dari buku telepon Anda pada baris baru di form name = phoneNumber; jika entri untuk nama tidak ditemukan, cetak Bukan ditemukan sebagai gantinya.
Catatan: Buku telepon Anda harus berupa struktur data Kamus / Peta / HashMap.
#### Format masuk
Baris pertama berisi bilangan bulat, `n`, yang menunjukkan jumlah entri dalam buku telepon. Masing-masing `n` baris berikutnya menjelaskan entri dalam bentuk `2` nilai yang dipisahkan spasi pada satu baris. Nilai pertama adalah nama teman, dan nilai kedua adalah nomor telepon `8`-digit. Setelah baris `n` entri buku telepon, ada sejumlah baris pertanyaan yang tidak diketahui. Setiap baris (kueri) berisi nama untuk dicari, dan Anda harus terus membaca baris sampai tidak ada lagi input.
Catatan: Nama terdiri dari huruf kecil alfabet Inggris dan hanya nama depan.
#### Kendala
```
1 ≤ N ≤ 10^5
2 ≤ queries ≤ 10^5
```
#### Format keluar
Pada baris baru untuk setiap permintaan, cetak Tidak ditemukan jika nama tidak memiliki entri yang sesuai di buku telepon; jika tidak, cetak nama lengkap dan nomor telepon dalam format name = phoneNumber.
#### Contoh input
```
3
sam 99912222
tom 11122222
harry 12299933
sam
edward
harry
```
#### Contoh keluar
```
sam=99912222
Not found
harry=12299933
```
#### source code
```
class Solution{
    public static void main(String []argh){
        Scanner in = new Scanner(System.in);
        int n = in.nextInt();
        Map<String,String> mp=new HashMap<String,String>();
        for(int i = 0; i < n; i++){
            String name = in.next();
            int phone = in.nextInt();
            // Write code here
            mp.put(name,Integer.toString(phone));
        }
        while(in.hasNext()){
            String s = in.next();
            // Write code here

            if(mp.containsKey(s)){
                System.out.println(s+"="+mp.get(s));
            }
            else{
                System.out.println("Not found");
            }
        }
        in.close();
    }
```
