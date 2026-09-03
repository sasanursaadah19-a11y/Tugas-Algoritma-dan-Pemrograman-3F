# Tugas-Algoritma-dan-Pemrograman-3F
.

🧮 Menentukan Jenis Segitiga Berdasarkan Panjang Sisi
📝 Deskripsi Masalah

Diberikan tiga buah sisi segitiga, yaitu sisi a, b, dan c. Program akan menerima panjang ketiga sisi tersebut sebagai input, kemudian menentukan apakah ketiga sisi tersebut dapat membentuk segitiga.

Jika ketiga sisi dapat membentuk segitiga, program akan menentukan jenis segitiga berdasarkan panjang sisinya, yaitu segitiga sama sisi, segitiga sama kaki, atau segitiga sembarang.

Program ini digunakan untuk menerapkan operasi perbandingan, percabangan, dan logika matematika dalam sebuah program.

📥 Input-Proses-Output

Input:
Nilai panjang sisi a, b, dan c.

Proses:

Memeriksa apakah ketiga sisi dapat membentuk segitiga dengan menggunakan syarat:
a + b > c
a + c > b
b + c > a
Jika tidak memenuhi syarat tersebut, maka ketiga sisi tidak membentuk segitiga.
Jika memenuhi syarat:
Jika a = b = c, maka segitiga merupakan segitiga sama sisi.
Jika terdapat dua sisi yang sama panjang, maka merupakan segitiga sama kaki.
Jika ketiga sisi berbeda, maka merupakan segitiga sembarang.

Output:
Jenis segitiga berdasarkan panjang ketiga sisinya.

INPUT a
INPUT b
INPUT c

IF a + b <= c OR a + c <= b OR b + c <= a THEN
    OUTPUT "Ketiga sisi tidak membentuk segitiga."
ELSE
    IF a = b AND b = c THEN
        OUTPUT "Ketiga sisi membentuk segitiga sama sisi."
    ELSE IF a = b OR b = c OR a = c THEN
        OUTPUT "Ketiga sisi membentuk segitiga sama kaki."
    ELSE
        OUTPUT "Ketiga sisi membentuk segitiga sembarang."
    END IF
END IF


```mermaid
flowchart TD
    A([START]) --> B[/INPUT a, b, c/]
    B --> C{Apakah memenuhi syarat segitiga?}

    C -->|Tidak| D[/OUTPUT: Bukan segitiga/]
    C -->|Ya| E{Apakah a = b = c?}

    E -->|Ya| F[/OUTPUT: Segitiga sama sisi/]
    E -->|Tidak| G{Apakah ada 2 sisi sama?}

    G -->|Ya| H[/OUTPUT: Segitiga sama kaki/]
    G -->|Tidak| I[/OUTPUT: Segitiga sembarang/]

    D --> J([END])
    F --> J
    H --> J
    I --> J
```
