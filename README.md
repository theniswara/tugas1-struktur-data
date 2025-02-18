# Penjelasan Kode

```java
import java.util.Scanner;
```
Mengimport kelas Scanner untuk dapat membaca input dari user.

```java
public class UAS_DASPRO {
```
Deklarasi kelas utama.

```java
public static void main(String[] args) {
```
Main method, titik awal eksekusi dan semua kode di dalam sini akan dieksekusi.

```java
Scanner sc = new Scanner(System.in);
```
Membuat objek scanner, untuk membaca input dari user.

```java
int jmlPoliteknik = 0;
```
Mendeklarasi variabel jmlPoliteknik dengan tipe data int dan nilai awal 0, digunakan untuk menyimpan jumlah inputan dari pengguna.

```java
while (true) {  }
```
Memulai loop tak terbatas untuk memvalidasi input jumlah politeknik.

```java
System.out.print("Masukkan Jumlah Politeknik: ");
```
Menampilkan pesan untuk user agar memasukkan jumlah jumlah Politeknik.

```java
if (sc.hasNextInt()) {  }
```
Memeriksa apakah input adalah integer.

```java
jmlPoliteknik = sc.nextInt();
```
Membaca input integer dari user dan menyimpan ke variabel jmlPoliteknik.

```java
sc.nextLine();
```
Membersihkan buffer / menghapus karakter "Enter" agar input berikutnya dapat dibaca.

```java
if (jmlPoliteknik > 0) { 
    break; }
```
Memeriksa apakah jumlah politeknik lebih besar dari 0, maka akan keluar dari loop.

```java
else { 
    System.out.println("Jumlah politeknik harus lebih dari nol. Silakan masukkan kembali."); 
}
```
JIka jumlah politeknik kurang dari / sama dengan 0, akan muncul pesan untuk masukkan kembali.

```java
else { System.out.println("Input tidak valid. Masukkan angka yang benar."); sc.nextLine(); }
```
Jika input bukan integer, akan muncul pesan input tidak valid.

```java
String[][][] atlet = new String[3][jmlPoliteknik][3];
```
Mendeklarasi array 3D bernama atlet untuk menyimpan nama atlet. Dengan dimensi: ```[3]``` Untuk 3 cabor, [jmlPoliteknik] untuk jumlah politeknik,  ```[]``` tiga atlet per politeknik setiap cabor.

```java
String[] cabor = {"Badminton", "Basket", "Bola Voli"};
```
Array cabor untuk menyimpan nama-nama cabor.

```java
for (int i = 0; i < cabor.length; i++) { ... }
```
Loop melalui setiap cabor (3 cabang).

```java
System.out.println("Masukkan nama atlet untuk cabang " + cabor[i] + ":");
```
Pesan untuk input nama atlet berdasarkan cabornya.

```java
for (int j = 0; j < jmlPoliteknik; j++) { ... }
```
Loop melalui setiap politeknik.
    
```java
System.out.println("Politeknik " + (j + 1) + ":");
```
Menampilkan nomor politeknik.

```java
for (int k = 0; k < 3; k++) { ... }
```
Loop untuk mengiput 3 atlet per politeknik.

```java
System.out.print("Atlet " + (k + 1) + ": ");
```
Mencetak nomor atlet yang sedang diproses.

```java
String namaAtlet = sc.nextLine();
```
Membaca input dari user dan menyimpan dalam variabel.

```java
if (namaAtlet.isEmpty()) { }
```
Jika nama kosong, tampilkan pesan kesalahan dan ulangi input.

```java
else { atlet[i][j][k] = namaAtlet; }
```
Jika tidak kosong, simpan nama ke dalam array.

```java
System.out.println("\n-----------------------");
```
Garis pemisah untuk memperjelas output.

```java
System.out.println("Informasi Nama Atlet:");
```
Menampilkan output judul untuk informasi nama atlet.

```java
for (int olahraga = 0; olahraga < cabor.length; olahraga++) { }
```
Loop untuk setiap cabang olahraga.

```java
System.out.println("Cabang " + cabor[olahraga] + ":");
```
Menampilakan cabang olahraga.

```java
for (int politeknik = 0; politeknik < jmlPoliteknik; politeknik++) { }
```
Loop untuk setiap politeknik pada proses output.

```java
System.out.println("Politeknik " + (politeknik + 1) + ":");
```
Menampilkan nomor politeknik.

```java
for (int nama = 0; nama < 3; nama++) { ... }
```
Loop untuk menampilkan 3 atlet per politeknik.

```java
System.out.println("Atlet " + (nama + 1) + ": " + atlet[olahraga][politeknik][nama]);
```
Menampilkan nama atlet untuk cabor, Politeknik.

```java
sc.close();
```
Menutup objek scanner.