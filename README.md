## Gambaran Umum

Kode ini berfungsi untuk membuat kalkulator.

Fitur-fitur:
1️⃣ Mampu melakukan operasi aritmatika, meliputi penjumlahan, pengurangan, perkalian, pembagian, dan modulus.

2️⃣ Dapat melakukan operasi aritmatika secara berulang kali, setelah menampilkan hasil suatu perhitungan.

## Bahasa Pemrograman

Kode proyek ini ditulis menggunakan bahasa pemrograman C++.

## Software Pendukung

Proyek ini dikembangkan menggunakan [Dev-C++ v5.11](https://sourceforge.net/projects/orwelldevcpp/). Pastikan Anda memiliki Dev-C++ terpasang sebelum menjalankan proyek.

## Cara Penggunaan

1. Buka proyek menggunakan Dev-C++.
2. Jalankan aplikasi dengan melakukan compile dan Run (shortcut F11).
4. Ikuti petunjuk untuk menggunakan kalkulator.

## Contoh Penggunaan Program

```cpp
// Library yang digunakan
#include <iostream>
#include <cmath> // Menambahkan header cmath
using namespace std;

int main() {
    cout << "Selamat datang, saat ini anda menggunakan Kalkulator digital by Dedad Fajar." << endl;
    cout << "Tekan enter untuk melanjutkan ke proses memasukkan perhitungan." << endl;
    cin.get(); // Menunggu pengguna menekan enter

    int choice;
    float num1, num2;

    do {
        cout << "Pilih operasi matematika yang diinginkan:" << endl;
        cout << "1. Penjumlahan" << endl;
        cout << "2. Pengurangan" << endl;
        cout << "3. Perkalian" << endl;
        cout << "4. Pembagian" << endl;
        cout << "5. Modulus" << endl;
        cout << "Masukkan pilihan (1/2/3/4/5): ";
        cin >> choice;

        switch(choice) {
            case 1:
                cout << "Masukkan dua angka untuk penjumlahan: ";
                cin >> num1 >> num2;
                cout << "Hasil perhitungan dari " << num1 << " + " << num2 << " = " << num1 + num2 << endl << endl;
                break;
            case 2:
                cout << "Masukkan dua angka untuk pengurangan: ";
                cin >> num1 >> num2;
                cout << "Hasil perhitungan dari " << num1 << " - " << num2 << " = " << num1 - num2 << endl << endl;
                break;
            case 3:
                cout << "Masukkan dua angka untuk perkalian: ";
                cin >> num1 >> num2;
                cout << "Hasil perhitungan dari " << num1 << " * " << num2 << " = " << num1 * num2 << endl << endl;
                break;
            case 4:
                cout << "Masukkan dua angka untuk pembagian: ";
                cin >> num1 >> num2;
                if(num2 != 0)
                    cout << "Hasil perhitungan dari " << num1 << " / " << num2 << " = " << num1 / num2 << endl << endl;
                else
                    cout << "Error! Pembagian dengan nol tidak diperbolehkan." << endl << endl;
                break;
            case 5:
                cout << "Masukkan dua angka untuk modulus: ";
                cin >> num1 >> num2;
                if(num2 != 0)
                    cout << "Hasil perhitungan dari " << num1 << " % " << num2 << " = " << fmod(num1, num2) << endl << endl;
                else
                    cout << "Error! Pembagian dengan nol tidak diperbolehkan." << endl << endl;
                break;
            default:
                // Jika pilihan yang dimasukkan salah
                cout << "Error! Pilihan yang dimasukkan tidak valid." << endl << endl;
                break;
        }

        char cont_choice;
        cout << "Lakukan operasi lagi? (y/n): ";
        cin >> cont_choice;
        if (cont_choice != 'y' && cont_choice != 'Y') {
            break;
        }
    } while (true);

    return 0;
}
