# Tugas 2 PBO - Konsep Obyek

# Kelas
Berikut contoh penerapan kelas :
```// Definisi kelas
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
