# Tugas 2 PBO - Konsep Obyek

# Kelas
Berikut contoh penerapan kelas :
```
// Definisi kelas
public class Mobil {

    // Variabel instance (atribut)
    private String warna;
    private String merk;
    private int tahunProduksi;

    // Konstruktor
    public Mobil(String warna, String merk, int tahunProduksi) {
        this.warna = warna;
        this.merk = merk;
        this.tahunProduksi = tahunProduksi;
    }

    // Metode (fungsi)
    public void nyalakanMesin() {
        System.out.println("Mesin menyala...");
    }

    public void matikanMesin() {
        System.out.println("Mesin mati...");
    }

    // Metode akses (getter)
    public String getWarna() {
        return warna;
    }

    // Metode mutator (setter)
    public void setWarna(String warna) {
        this.warna = warna;
    }
}
```
### Penjelasan Singkat:
1. ***Kelas*** : Mobil adalah cetak biru (blueprint) untuk objek yang akan dibuat. Kelas ini berisi atribut dan metode yang menggambarkan perilaku dan keadaan dari objek.
2. ***Atribut (Variabel Instance)*** : warna, merk, dan tahunProduksi adalah atribut yang menyimpan data atau keadaan dari objek yang dibuat dari kelas ini.
3. ***Konstruktor*** : Metode khusus Mobil digunakan untuk menginisialisasi objek saat pertama kali dibuat dengan nilai-nilai tertentu.
4. ***Metode*** : nyalakanMesin, matikanMesin, getWarna, dan setWarna adalah fungsi yang menggambarkan perilaku dari objek, seperti menyalakan mesin atau mengubah warna mobil.
5. ***Getter dan Setter*** : Digunakan untuk mengakses atau memodifikasi nilai atribut secara aman.

# Objek
Berikut contoh penerapan objek :
```
class Mobil {
    // Atribut (properties atau fields)
    String merk;
    String model;
    int tahun;

    // Konstruktor (constructor) untuk inisialisasi objek
    Mobil(String merk, String model, int tahun) {
        this.merk = merk;
        this.model = model;
        this.tahun = tahun;
    }

    // Metode (methods) untuk menggambarkan perilaku
    void nyalakanMesin() {
        System.out.println(merk + " " + model + " mesinnya menyala.");
    }

    void matikanMesin() {
        System.out.println(merk + " " + model + " mesinnya mati.");
    }
}

public class Main {
    public static void main(String[] args) {
        // Membuat objek Mobil
        Mobil mobilku = new Mobil("Toyota", "Camry", 2021);

        // Mengakses atribut dan metode dari objek
        System.out.println("Mobil: " + mobilku.merk + " " + mobilku.model + ", Tahun: " + mobilku.tahun);
        mobilku.nyalakanMesin();
        mobilku.matikanMesin();
    }
}
```
### Penjelasan Singkat:
1. ***Atribut*** : String merk, String model, dan int tahun adalah contoh atribut yang dimiliki oleh kelas Mobil. Atribut ini merepresentasikan data atau properti dari sebuah objek.
2. ***Konstruktor*** : Mobil(String merk, String model, int tahun) adalah konstruktor yang digunakan untuk menginisialisasi objek dengan nilai-nilai awal saat objek dibuat.
3. ***Metode*** : nyalakanMesin() dan matikanMesin() adalah metode yang merepresentasikan perilaku atau tindakan yang dapat dilakukan oleh objek Mobil.
4. ***Objek*** : Mobil mobilku = new Mobil("Toyota", "Camry", 2021); adalah cara membuat objek baru dari kelas Mobil.
Pada kode ini, objek mobilku dari kelas Mobil memiliki atribut merk, model, dan tahun, serta metode nyalakanMesin() dan matikanMesin() yang dapat digunakan untuk mengoperasikan objek tersebut.

# Abstraksi
Berikut contoh penerapan abstraksi :
```
// Abstract class
abstract class Mobil{
    String merk;
    String model;
    // Constructor
    Mobil(String merk, String model){
        this.merk = merk;
        this.model = model;}
    // Abstract method (tidak memiliki implementasi)
    abstract void startEngine();
    // Non-abstract method (memiliki implementasi)
    void displayInfo(){
        System.out.println("Merk: " + merk + ", Model: " + model);}
}

// Subclass (Turunan dari Mobil)
class Sedan extends Mobil{
    Sedan(String merk, String model){
        super(merk, model);}
    // Implementasi dari abstract method
    @Override
    void startEngine(){
        System.out.println("Mesin " + merk + " " + model + " menyala dengan tombol start.");}
}

public class Main{
    public static void main(String[] args){
        Sedan sedan = new Sedan("Toyota", "Camry");
        sedan.displayInfo();
        sedan.startEngine();}
}
```
### Penjelasan:
1. ***Abstract Class (Mobil)*** : Kelas ini tidak dapat diinstansiasi secara langsung dan mengandung satu atau lebih metode abstrak. Kelas abstrak digunakan untuk mewakili konsep umum (seperti "Mobil").
2. ***Abstract Method (startEngine)*** : Ini adalah metode tanpa implementasi. Kelas yang mewarisi kelas abstrak harus memberikan implementasi untuk metode ini.
3. ***Subclass (Sedan)*** : Ini adalah kelas konkret yang mengimplementasikan metode abstrak dari kelas Mobil.
4. ***Main Method*** : Digunakan untuk menguji konsep abstraksi dengan membuat objek dari kelas Sedan dan memanggil metode yang ada.
Dengan abstraksi, kita bisa menyembunyikan detail spesifik dari bagaimana mesin dinyalakan (startEngine), sehingga pengguna cukup tahu bahwa mobil bisa dinyalakan tanpa perlu tahu cara kerjanya.

# Enkapsulasi
Berikut contoh penerapan enkapsulasi :
```
public class Mobil {
    // Atribut private (tidak dapat diakses langsung dari luar kelas)
        private String merek;
        private int kecepatan;
    // Constructor
        public Mobil(String merek, int kecepatan){
            this.merek = merek;
            this.kecepatan = kecepatan;}
    // Getter untuk mendapatkan nilai merek
        public String getMerek(){
            return merek;}
    // Setter untuk mengubah nilai merek
        public void setMerek(String merek){
            this.merek = merek;}
    // Getter untuk mendapatkan nilai kecepatan
        public int getKecepatan(){
            return kecepatan;}
    // Setter untuk mengubah nilai kecepatan
        public void setKecepatan(int kecepatan){
            // Validasi sederhana
            if (kecepatan > 0){
                this.kecepatan = kecepatan;}}
    // Metode untuk menampilkan informasi mobil
        public void tampilkanInfo() {
            System.out.println("Merek: " + merek);
            System.out.println("Kecepatan: " + kecepatan + " km/h");}
}

// Kelas utama untuk menjalankan program
public class Main {
    public static void main(String[] args){
        Mobil mobil1 = new Mobil("Toyota", 120);
        // Menggunakan metode getter untuk mengambil nilai
        System.out.println("Merek mobil: " + mobil1.getMerek());
        // Menggunakan metode setter untuk mengubah nilai
        mobil1.setKecepatan(150);
        // Menampilkan informasi mobil
        mobil1.tampilkanInfo();}
}
```
### Penjelasan Singkat :
1. Enkapsulasi adalah konsep OOP yang membungkus data (atribut) dan metode dalam satu unit, yaitu kelas, serta menyembunyikan detail implementasi dari luar kelas. Atribut merek dan kecepatan dalam contoh ini dideklarasikan sebagai private, sehingga hanya dapat diakses melalui metode getter dan setter yang bersifat public.
2. Dengan enkapsulasi, Anda dapat mengontrol bagaimana data dimodifikasi atau diakses. Misalnya, di dalam metode setKecepatan, ada validasi sederhana yang memastikan bahwa kecepatan hanya dapat diatur ke nilai yang positif.
Ini membantu menjaga integritas data dan mencegah akses langsung yang bisa menyebabkan inkonsistensi.

# Inheritance
Berikut contoh penerapan inheritance :
```
// Superclass (Parent Class)
class Mobil {
    String merk;
    int tahun;
    void infoMobil(){
        System.out.println("Merk: " + merk + ", Tahun: " + tahun);}
}

// Subclass (Child Class) yang mewarisi dari kelas Mobil
class MobilSport extends Mobil {
    int kecepatanMaks;
    void infoMobilSport(){
        // Memanggil metode dari superclass
        infoMobil();
        System.out.println("Kecepatan Maksimum: " + kecepatanMaks + " km/jam");}
}

public class Main {
    public static void main(String[] args){
        // Membuat objek dari subclass
        MobilSport ferrari = new MobilSport();
        ferrari.merk = "Ferrari";
        ferrari.tahun = 2023;
        ferrari.kecepatanMaks = 350;
        // Memanggil metode pada subclass
        ferrari.infoMobilSport();}
}
```
### Penjelasan Singkat:
1. Pada contoh di atas, MobilSport adalah subclass yang mewarisi properti merk dan tahun, serta metode infoMobil() dari superclass Mobil.
2. MobilSport juga dapat memiliki properti atau metode tambahan, seperti kecepatanMaks dan infoMobilSport(), yang spesifik untuk subclass tersebut.

# Polimorfisme Statis - _Metode Overloading_
Berikut penerapan polimorfisme metode overloading :
```
class Calculator {
    // Metode overload untuk penjumlahan dua bilangan integer
    int add(int a, int b){
        return a + b;}

    // Metode overload untuk penjumlahan tiga bilangan integer
    int add(int a, int b, int c){
        return a + b + c;}

    // Metode overload untuk penjumlahan dua bilangan double
    double add(double a, double b){
        return a + b;}
}

public class Main {
    public static void main(String[] args){
        Calculator calc = new Calculator();
        System.out.println("Hasil penjumlahan dua integer: " + calc.add(5, 10));
        System.out.println("Hasil penjumlahan tiga integer: " + calc.add(5, 10, 15));
        System.out.println("Hasil penjumlahan dua double: " + calc.add(5.5, 10.5));}
}
```
### Penjelasan Singkat :
1. ***Polimorfisme Statis*** : Terjadi pada saat compile-time dan disebut juga metode overloading.
2. ***Metode Overloading*** : Dalam contoh ini, metode add di dalam kelas Calculator di-overload untuk menerima berbagai kombinasi tipe dan jumlah parameter yang berbeda.
3. Saat program dijalankan, metode yang dipanggil akan ditentukan berdasarkan jumlah dan tipe argumen yang diberikan saat pemanggilan.

# Polimorfisme Dinamis - _Metode Overriding_
Berikut penerapan polimorfisme metode overriding :
```
// Kelas induk
class Hewan {
    void suara(){
        System.out.println("Hewan mengeluarkan suara");}
}

// Kelas turunan
class Anjing extends Hewan {
    @Override
    void suara(){
        System.out.println("Anjing menggonggong");}
}

// Kelas turunan lainnya
class Kucing extends Hewan {
    @Override
    void suara(){
        System.out.println("Kucing mengeong");}
}

public class Main {
    public static void main(String[] args){
        // Polimorfisme dinamis terjadi di sini
        Hewan hewan1 = new Anjing(); // Referensi kelas induk, objek kelas turunan
        Hewan hewan2 = new Kucing(); // Referensi kelas induk, objek kelas turunan
        // Metode yang dipanggil ditentukan pada runtime
        hewan1.suara(); // Output: Anjing menggonggong
        hewan2.suara(); // Output: Kucing mengeong
    }
}
```
### Penjelasan Singkat :
1. ***Polimorfisme Dinamis*** : Ini terjadi ketika metode yang dipanggil pada objek ditentukan saat runtime, bukan saat kompilasi. Dalam contoh ini, metode suara() dipanggil berdasarkan tipe objek yang sebenarnya (Anjing atau Kucing), meskipun referensi objek adalah dari tipe Hewan.
2. ***Metode Overriding*** : Kelas turunan (Anjing dan Kucing) mengoverride (menggantikan) implementasi metode suara() dari kelas induk Hewan, memberikan perilaku yang spesifik sesuai dengan tipe objeknya.
Melalui polimorfisme dinamis, Java memungkinkan penggunaan metode yang sesuai dengan tipe objek yang sebenarnya, meskipun kita menggunakan referensi dari kelas induknya.
