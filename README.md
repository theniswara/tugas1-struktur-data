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
while (true) { ... }
```
Memulai loop tak terbatas untuk memvalidasi input jumlah politeknik.

```java
System.out.print("Masukkan Jumlah Politeknik: ");
```
Menampilkan pesan untuk user agar memasukkan jumlah jumlah Politeknik.

```java
if (sc.hasNextInt()) { ... }
```
Memeriksa apakah input adalah integer