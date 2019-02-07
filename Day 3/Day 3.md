## Laporan 30 Days of Code
---
### Day 3 : Intro to Conditional Statements
#### Tujuan
Dalam tantangan ini diajarkan tentang
#### Tugas
blablabla....
#### Format masuk
blablabla....
#### Kendala
blablaba...
#### Format keluar
blablaba...
#### Contoh input
blablabla...
#### Contoh keluar
blablaba...
#### Souce Code
```
import java.io.*;
import java.math.*;
import java.security.*;
import java.text.*;
import java.util.*;
import java.util.concurrent.*;
import java.util.regex.*;

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
