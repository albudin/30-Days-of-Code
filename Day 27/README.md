## Laporan 30 Days of Code
---
### Day 27 : Testing
#### Masalah ini adalah tentang pengujian unit.

Perusahaan Anda membutuhkan fungsi yang memenuhi persyaratan berikut:
    * Untuk array yang diberikan n bilangan bulat, fungsi mengembalikan indeks elemen dengan nilai minimum dalam array. Jika ada lebih dari satu elemen dengan nilai minimum, indeks yang dikembalikan harus yang terkecil.
    * Jika array kosong dilewatkan ke fungsi, itu harus memunculkan Pengecualian.
Catatan: Array diindeks dari 0.

Seorang kolega telah menulis fungsi itu, dan tugas Anda adalah merancang 3 unit test yang terpisah, menguji apakah fungsi tersebut berperilaku dengan benar. Implementasi dengan Python tercantum di bawah ini (Implementasi dalam bahasa lain dapat ditemukan dalam templat kode):
```
def minimum_index(seq):
    if len(seq) == 0:
        raise ValueError("Cannot get the minimum value index from an empty sequence")
    min_idx = 0
    for i in range(1, len(seq)):
        if a[i] < a[min_idx]:
            min_idx = i
    return min_idx
```
Rekan kerja lain telah menyiapkan fungsi yang akan melakukan pengujian dan memvalidasi hasil yang dikembalikan dengan harapan. Tugas Anda adalah mengimplementasikan 3 kelas yang akan menghasilkan data uji dan hasil yang diharapkan untuk fungsi pengujian. Lebih khusus: function get_array () di kelas TestDataEmptyArray dan fungsi get_array () dan get_expected_result () di kelas TestDataUniqueValues ​​dan TestDataExactlyTwoDifferentMinimums mengikuti spesifikasi di bawah ini:
    * Metode get_array () di kelas TestDataEmptyArray harus mengembalikan array kosong.
    * Metode get_array () di kelas TestDataUniqueValues ​​harus mengembalikan array ukuran minimal 2 dengan semua elemen unik, sedangkan metode get_expected_result () dari kelas ini harus mengembalikan indeks nilai minimum yang diharapkan untuk array ini.
    * Metode get_array () di kelas TestDataExactlyTwoDifferentMinimums harus mengembalikan array di mana ada dua nilai minimum yang berbeda, sementara metode get_expected_result () dari kelas ini harus mengembalikan indeks nilai minimum yang diharapkan untuk array ini.
Lihatlah templat kode untuk melihat penerapan fungsi yang tepat yang sudah diterapkan rekan Anda.

#### source code
```
import java.util.*;

public class Solution {

    public static int minimum_index(int[] seq) {
        if (seq.length == 0) {
            throw new IllegalArgumentException("Cannot get the minimum value index from an empty sequence");
        }
        int min_idx = 0;
        for (int i = 1; i < seq.length; ++i) {
            if (seq[i] < seq[min_idx]) {
                min_idx = i;
            }
        }
        return min_idx;
    }

    static class TestDataEmptyArray {
        // membuat array kosong
        public static int[] get_array(){
            int[] a=new int [0];
            return a;
        }
    }

    static class TestDataUniqueValues {
        public static int[] get_array(){
            int [] array = arrayWithNum();
            //check jika element unik
            for (int i=0;i<array.length;i++){
                for(int j=i+1;j<array.length;j++){
                    if(array[i]==array[j]){get_array();}
                }   
            }
            return array;
        }

        //buat array dengan nomor acak
        public static int[] arrayWithNum(){
                int[] array=new int [3];
                for(int i=0;i<array.length;i++){
                    array[i]=random();
                }
                //sort array untuk proper jawaban
                Arrays.sort(array);
                return array;
            }

            //random numbers
            public static int random(){
                int random =(int)(Math.random()*100)+1;
                return random;
            }

            public static int get_expected_result(){
                int[] array = get_array();
                int minValue = minNumber(array);
                return minValue;

            }

            public static int minNumber(int[] array){
                //untuk mendapatkan minimum index dalam array
                int min_idx=0;
                for(int i=1;i<array.length;i++){
                    if(array[i]<array[min_idx]){
                        min_idx=i;
                    }
                }
                return min_idx;
            }
        }

        static class TestDataExactlyTwoDifferentMinimums{
            //bla..
            private TestDataUniqueValues testDataUniqueValues;
            public TestDataExactlyTwoDifferentMinimums(TestDataUniqueValues testDataUniqueValues){
                this.testDataUniqueValues=testDataUniqueValues;
            }
            public static int[] get_array(){
                int[] array=arrayWithNum();
                //check jika element sama
                for(int i=0;i<array.length;i++){
                    for(int j = i+1;j<array.length;j++){
                        if(!(array[i]==array[j])){get_array();}
                    }
                }
                return array;
            }


            //create an array with
            public static int[] arrayWithNum(){
                int[] array =new int[]{1,1};
                return array;
            }

            //random numbers
            public static int random(){
                int num=TestDataUniqueValues.get_expected_result();
                return num;
            }

            public static int get_expected_result(){
                int[] array=get_array();
                int minValue=minNumber(array);
                return minValue;
            }

            public static int minNumber(int[] array){
                //kode ini akan menemukan min index objek
                int min_idx=0;
                for(int i=1;i<array.length;i++){
                    if(array[i]<array[min_idx]){
                    min_idx=i;
                    }
                }
                return min_idx;
            }
        }

    
```
