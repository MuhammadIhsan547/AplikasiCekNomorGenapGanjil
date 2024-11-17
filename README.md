# AplikasiCekNomorGenapGanjil
 Tugas 1 - Muhammad Ihsan - 2210010286

## 1. Deskripsi Program:
* GUI terdiri dari JTextField untuk input angka dan tombol Cek

* Saat tombol ditekan, program akan memvalidasi input dan
menampilkan hasilnya pada JLabel

## 2. Komponen GUI: 
JFrame, JPanel, JLabel, JTextField, JButton
- JTextField: Untuk input angka.
- JButton: Tombol untuk memeriksa angka.
- JLabel: Untuk menampilkan hasil pemeriksaan (Genap/Ganjil). 

## 3. Logika Program: 
Kondisional (if-else), Validasi input
- Implementasikan logika di tombol cekButton untuk memeriksa apakah angka yang dimasukkan adalah genap atau ganjil.
- Gunakan kondisional if-else untuk memisahkan angka genap dari ganjil.
- Tambahkan validasi untuk memastikan input hanya angka.

## 4. Events:
```
private void TombolCekActionPerformed(java.awt.event.ActionEvent evt) {                                          
    try {
        // Mendapatkan angka dari fieldangka (input dari pengguna)
        int angka = Integer.parseInt(fieldangka.getText());

        // Variabel untuk menyimpan hasil
        String hasil = "Angka " + angka;

        // Mengecek apakah angka genap atau ganjil
        if (angka % 2 == 0) {
            hasil += " adalah Genap";
        } else {
            hasil += " adalah Ganjil";
        }

        // Mengecek apakah angka adalah bilangan prima
        if (isPrime(angka)) {
            hasil += " dan bilangan prima";
        } else {
            hasil += " dan bukan bilangan prima";
        }

        // Menampilkan hasil pada komponen hasil (HasilGenapGanjil)
        HasilGenapGanjil.setText(hasil);

        // Menampilkan hasil dalam dialog pop-up
        JOptionPane.showMessageDialog(this, hasil, "Hasil", JOptionPane.INFORMATION_MESSAGE);

    } catch (NumberFormatException e) {
        // Menangani kesalahan jika input bukan angka
        JOptionPane.showMessageDialog(this, "Masukkan angka yang valid!", "Error", JOptionPane.ERROR_MESSAGE);
    }
}                                          

// Tombol keluar untuk menutup aplikasi
private void TombolKeluarActionPerformed(java.awt.event.ActionEvent evt) {                                             
    System.exit(0); // Menutup aplikasi
}

// Fungsi untuk mengecek apakah sebuah angka adalah bilangan prima
private boolean isPrime(int n) {
    if (n <= 1) return false; // Angka ≤ 1 bukan bilangan prima
    for (int i = 2; i <= Math.sqrt(n); i++) {
        if (n % i == 0) return false; // Jika habis dibagi angka lain, bukan prima
    }
    return true; // Jika tidak ada faktor lain, bilangan adalah prima
}
```

## Contoh Gambar Project Setelah di Run
![Tugas1](https://github.com/user-attachments/assets/93fc0ad0-0b9b-428e-b06f-8f8258eb4acb)


## Indikator Penilaian:

| No  | Komponen         |  Persentase  |
| :-: | --------------   |   :-----:    |
|  1  | Komponen GUI     |    20    |
|  2  | Logika Program   |    20    |
|  3  | Events           |    15    |
|  4  | Kesesuaian UI    |    15    |
|  5  | Memenuhi Variasi |    30    |
|     | TOTAL        | 100 |

## Pembuat

Nama   : Muhammad Ihsan
NPM    : 2210010286
Kelas : 5A Ti Reg Pagi BJM
