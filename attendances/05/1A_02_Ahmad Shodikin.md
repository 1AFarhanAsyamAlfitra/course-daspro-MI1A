## JOBSHEET 5

## PEMILIHAN 1

### Tujuan

Mahasiswa mampu menyelesaikan permasalahan/studi kasus menggunakan sintaks pemilihan 1 dan mengimplemantasikannya dalam bahasa pemrogaman java.

### Alat dan Bahan
+ PC/laptop
+ Browser(chrome, firefox, safari)
+ Koneksi internet

### Praktikum

#### Percobaan 1 : Penggunaan if

#### Waktu percobaan : 40 menit

1. Perhatikan flowchart dibawah ini!

    <p align="left">
    <img width="351" height="460" src="images/01.png">
    </p>
    

> Flowchart diatas digunakan untuk menentukan bilangan ganjil/genap, selanjutnya kita akan membuat programnya berdasarkan
> flowchart di atas!

2. Tambahkan library Scanner, deklarasi Scanner, dan buat variabel bil untuk menampung data yang diinput melalui keyboard

    ![](images/03.png)


```Java
// Ketik kode program di atas di bawah sini
import java.util.Scanner;
Scanner input = new Scanner(System.in);
int bil;
System.out.print("Masukkan sebuah bilangan: ");
bil = input.nextInt();
```

    Masukkan sebuah bilangan: 20


3. Buatlah struktur kondisi untuk mengecek apakah bilangan tersebut merupakan bilangan genap atau ganjil

    ![](images/04.png)


```Java
// Ketik kode program di atas di bawah sini
if(bil%2 == 0){
    System.out.println("Bilangan Genap");
} else {
    System.out.println("Bilangan Ganjil");
}
```

    Bilangan Genap


##### Pertanyaan
1. Modifikasi program diatas dibagian struktur pemilihannya sehingga menjadi sebagai berikut:

    ![](images/05.png)


```Java
// Ketik kode program di atas di bawah sini
String output = (bil % 2 == 0) ? "Bilangan Genap" : "Bilangan Ganjil";
System.out.println(output);
```

    Bilangan Genap


2. Jalankan dan amatilah hasilnya!
3. Jelaskan mengapa output program yang dimodifikasi sama dengan output program sebelum dimodifikasi!

#### Percobaan 2 : Penggunaan if else

#### Waktu percobaan : 40 menit

### Jawaban 
3.karena program hanya dijadikan lebih efisien dengan ternary operator, jadi hasilnya akan sama dengan program yang diatas


+ Buatlah sebuah variabel nilai untuk menyimpan inputan dari keyboard

    ![](images/06.png)


```Java
// Ketik kode program di atas di bawah sini
int nilai1, nilai2, rata2;
System.out.print("Masukkan sebuah bilangan 1: ");
nilai1 = input.nextInt();
System.out.print("Masukkan sebuah bilangan 2: ");
nilai2 = input.nextInt();

rata2 = (nilai1+nilai2)/2;
System.out.print("Hasil rata-rata nilai: " +rata2)
```

    Masukkan sebuah bilangan 1: 100
    Masukkan sebuah bilangan 2: 100
    Hasil rata-rata nilai: 100

+ Tambahkan sebuah kondisi untuk mengecek input pada variabel nilai

    ![](images/07.png)


```Java
// Ketik kode program di atas di bawah sini
if(rata2 >= 100){
    rata2 -= 5;
}
System.out.println("Hasil akhir nilai adalah " +rata2);
```

    Hasil akhir nilai adalah 95


+ Jalankan program. Amati apa yang terjadi!

##### Pertanyaan
1. Jelaskan fungsi kode program berikut:
    
    ```
    nilai+=10;
    nilai-=10;
    ```

2. Modifikasilah program diatas dimana inputannya yang awalnya hanya satu kemudian diganti 2 inputan (misal : nilai1 dan nilai2), lakukan perhitungan rata-rata kedua nilai tersebut jika nilainya lebih dari sama dengan 100 maka dikurangi 5, sedangkan jika nilai rata-rata tersebut kurang dari 100 maka akan langsung dicetak!

### jawaban 
    1. merupakan operator gabungan yang berfungsi menjadikan operator lebih efisien penulisannya. += adalah aslinya a+a=b menjadi +=a,dan -= juga sama dengan a-a=b menjadi -=b
 

#### Percobaan 3 : Penggunaan if else-if else

#### Waktu percobaan : 40 menit

+ Tambahakan library `Scanner`
+ Buatlah deklarasi `Scanner`
+ Buat variabel umur bertipe `int`

    ![](images/08.png)


```Java
// Ketik kode program di atas di bawah sini
import java.util.Scanner;
Scanner input = new Scanner(System.in);

int umur;
System.out.print("Masukkan umur Anda: ");
umur = input.nextInt();
```

    Masukkan umur Anda: 18


+ Kode untuk melakukan pengecekan variabel `umur`

    ![](images/09.png)


```Java
// Ketik kode program di atas di bawah sini
if(umur > 60)  {
    System.out.println("Lansia"); 
} else if (umur > 45) {
    System.out.println("Tua");
}else if (umur > 17){
    System.out.println("Dewasa");
}else if (umur>5){
    System.out.println("Anak-Anak");
}else {
    System.out.println("Balita");
}
```

    Dewasa


+ Jalankan program dan amati apa yang terjadi!

##### Percobaan 4 : Penggunaan switch-case

#### Waktu percobaan : 40 menit

1. Deklarasikan Scanner
1. Buatlah variabel-variabel berikut

    ![](images/10.png)


```Java
// Ketik kode program di atas di bawah sini
import java.util.Scanner;
Scanner sc = new Scanner(System.in);
double angka1, angka2, hasil;
char operator; 
```

3. Kode program untuk meminta inputan dari keyboard

    ![](images/11.png)


```Java
// Ketik kode program di atas di bawah sini
System.out.print("Masukkan angka pertama: ");
angka1 = sc.nextDouble();
System.out.print("Masukkan angka kedua: ");
angka2 = sc.nextDouble();
System.out.print("Masukkan operator (+ -* /): ");
operator = sc.next().charAt(0);
```

    Masukkan angka pertama: 20
    Masukkan angka kedua: 20
    Masukkan operator (+ -* /): +


4. Kode di bawah ini untuk melakukan pengecekan operator yang digunakan sebelum dilakukan operasi aritmatika

    ![](images/12.png)


```Java
// Ketik kode program di atas di bawah sini
switch(operator){
case '+':
hasil = angka1 + angka2;
System.out.println(angka1 + "+" + angka2 + "=" + hasil);
break;
case '-':
hasil = angka1 - angka2;
System.out.println(angka1 + "-" + angka2 + "=" + hasil);
break;
case '*':
hasil = angka1 * angka2;
System.out.println(angka1 + "*" + angka2 + "=" + hasil);
break;
case '/':
hasil = angka1 / angka2;
System.out.println(angka1 + "/" + angka2 + "=" + hasil);
break;
default:
System.out.println("Operator yang Anda masukkan salah");
}
```

    20.0+20.0=40.0


5. Jalankan program. Amati apa yang terjadi!

##### Pertanyaan
1. Jelaskan fungsi dari break dan default pada percobaan 4 diatas!
2. Jelaskan fungsi perintah kode program dibawah ini pada percobaan 4!

    ```
    operator = sc.next().chartAt(0);
    ```

### jawaban
    1. fungsi break adalah menghentikan case agar tidak melanjutkan ke case yang berikutnya, sedangkan default adalah case/pilihan yang akan dijalankan jika tidak ada case yang cocok/ditemukan.
    2.fungsi program operator = sc.next().chartAt(0); adalah merubah pengeluaran menjadi char/karakter

### Tugas

#### Waktu pengerjaan Tugas: 140 menit

1. Buatlah program untuk menginputkan dua buah bilangan bulat, kemudian mencetak salah satu bilangan yang nilainya terbesar.
```Java
// Ketik kode program di atas di bawah sini
import java.util.Scanner;
Scanner input = new Scanner(System.in);
int bil1,bil2;
System.out.print("Masukkan bilangan 1: ");
bil1 = input.nextInt();
System.out.print("Masukkan bilangan 2: ");
bil2 = input.nextInt();

if(bil1>bil2){
    System.out.print(bil1 + " Adalah bilangan terbesar");
} else {
    System.out.print(bil2 + " Adalah bilangan terbesar");
}
```
2. Perhatikan flowchart berikut ini:
![](images/02.png)

```Java
// Ketik kode program di atas di bawah sini
import java.util.Scanner;
Scanner input = new Scanner(System.in);
int umur;
System.out.print("Masukkan umur Anda: ");
umur = input.nextInt();

if(umur >=17){
    System.out.print("Anda boleh Berkendara");
} else {System.out.print("Anda tidak boleh berkendara"); }
```
> Buatlah program sesuai dengan flowchart diatas!


3. Pada akhir semester seorang dosen menghitung nilai akhir dari mahasiswa yang terdiri dari nilai uas, uts, kuis, dan tugas. Nilai akhir didapatkan dari 40% nilai uas, 30% nilai uts, 10% nilai kuis, dan 20% nilai tugas. Jika nilai akhir dari mahasiswa dibawah 65 maka mahasiswa tersebut akan mendapatkan remidi. Buatlah program untuk membantu mengetahui mahasiswa yang mendapatkan remidi berdasarkan nilai akhir yang didapatkannya!

```Java
// Ketik kode program di atas di bawah sini
import java.util.Scanner;
Scanner input = new Scanner(System.in);
double nilai;
System.out.print("Masukkan akhir mahasiswa : ");
nilai = input.nextDouble();

if(nilai <65){
    System.out.print("Anda remidi");
} System.out.print("Anda tidak tidak remidi");
```

4. Sebuah toko memberikan diskon kepada pelanggannya dengan ketentuan sebagai berikut:

| Total Belanja     | Potongan |
|-------------------|----------|
| >Rp. 200.000,00   | 2%       |
| >Rp. 500.000,00   | 5%       |
| >Rp. 1.000.000,00 | 10%      |

> Total belanja diperoleh dari pembelian tiga barang yaitu barang A, barang B, dan barang C. Ketika menginputkan harga barang juga menginputkan jumlah barang yang dibeli.

Contoh outputnya
```
Masukkan harga barang A   :100000
Masukkan jumlah barang A  :10
Masukkan harga barang B   :250000
Masukkan jumlah barang B  :5
Masukkan harga barang C   :150000
Masukkan jumlah barang C  :1
---------------------------------------------
                Struk total
---------------------------------------------
Nama Barang 	| 	Harga 	| 	Jumlah 	| 	Total
Barang A            100000         10        1000000   
Barang B            250000         5         1250000   
Barang C            150000         1         150000    
Total       :2400000
Diskon      :240000.0
Total Bayar :2160000.0
```


```Java
// Ketik kode program di atas di bawah sini
import java.util.Scanner;
Scanner input = new Scanner(System.in);
double hargaA,hargaB,hargaC,totalBarang,jumlahA,jumlahB,jumlahC,totalA,totalB,totalC,totalBayar;
double diskon = 0;

System.out.print("Masukkan harga barang A : ");
hargaA = input.nextDouble();
System.out.print("Masukkan jumlah barang A :");
jumlahA = input.nextDouble();
System.out.print("Masukkan harga barang B : ");
hargaB = input.nextDouble();
System.out.print("Masukkan jumlah barang B :");
jumlahB = input.nextDouble();
System.out.print("Masukkan harga barang C : ");
hargaC = input.nextDouble();
System.out.print("Masukkan jumlah barang C :");
jumlahC = input.nextDouble();

totalA = hargaA * jumlahA;
totalB = hargaB * jumlahB;
totalC = hargaC * jumlahC;

System.out.println("---------------------------------");
System.out.println("\tStruk Total");
System.out.println("---------------------------------");
System.out.println("Nama Barang" + "\t\t\t" + "Harga" + "\t\t" + "Jumlah" + "\t\t" + "Total");
System.out.println("Barang A" + "\t\t" + hargaA + "\t\t" + jumlahA + "\t\t" + totalA);
System.out.println("Barang A" + "\t\t" + hargaB + "\t\t" + jumlahB + "\t\t" + totalB);
System.out.println("Barang A" + "\t\t" + hargaC + "\t\t" + jumlahC + "\t\t" + totalC);

totalBarang = totalA + totalB + totalC;
System.out.println("Total : " + totalBarang);

if (totalBarang > 1000000) {
	diskon = totalBarang * 10/100;
	System.out.println("Diskon : " + diskon);
    } else if (totalBarang > 500000){
    	diskon = totalBarang * 5/100;
    	System.out.println("Diskon : " + diskon);
    } else if (totalBarang > 200000){
    	diskon = totalBarang * 2/100;
    	System.out.println("Diskon : " + diskon);
    } 
 totalBayar = totalBarang - diskon;
 System.out.print("Total Bayar :" + totalBayar);

```