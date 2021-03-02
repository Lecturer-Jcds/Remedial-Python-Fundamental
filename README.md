# Remedial Ujian Python Data Science Fundamental



[![logopwdk.png](https://i.postimg.cc/66VC3Rgx/logopwdk.png)](https://postimg.cc/s1XMHB3T)


<hr>



### **Soal 1 - Leap year**

__*Tahun kabisat*__ merupakan tahun yang mengalami penambahan satu hari dengan tujuan untuk menyesuaikan penanggalan dengan tahun astronomi. Dalam satu tahun tidak secara persis terdiri dari 365 hari, tetapi __*365 hari 5 jam 48 menit 45,1814 detik*__. Jika hal ini tidak dihiraukan, maka setiap empat tahun akan kekurangan hampir 1 hari. Maka untuk mengkompensasi hal ini, setiap 4 tahun sekali, diberi 1 hari ekstra: __29 Februari__. 

Buatlah sebuah **Return Function** dengan **1 Argumen** serta dapat menerima inputan dari user yang dapat menentukan suatu input dari user tergolong tahun kabisat atau tidak. Saat file dieksekusi, user diminta memasukkan angka tahun tertentu, kemudian akan muncul hasil yang menyatakan input user tersebut tergolong tahun kabisat atau tidak. Contoh hasil yang diharapkan:
**(Gunakan Sistem Penanggalan Gregorian)**

```bash
Input tahun : 2019
Hasil : BUKAN TAHUN KABISAT

Input tahun : 2020
Hasil : TAHUN KABISAT
```


✅ Commit & push source code jawaban soal ini, beserta file JSON hasilnya ke __Github__ Anda, buatlah repo dengan nama __Leap_Year__, kemudian lampirkan __url link repo Github__ Anda via email ke _khumaeni@purwadhika.com!_ dan _operational_jkt@purweadhika.com_. Subject Email : **Remedial Modul 1 - JCDS12 - Nama**


#

### **Soal 2 - Credit Card Validation**

Disediakan __sebuah List yg berisi Dictionary__ (_ccNasabah_), List ini berisi data nomor kartu kredit nasabah sebuah bank, yang belum diverifikasi validitas kartu kreditnya. Buatlah __sebuah file python__ (*.py*) yang memiliki **Return Function** dan **1 Buah Argumen**, Function tersebut akan memisahkan antara nasabah dengan nomor kartu kredit valid & invalid, lalu menyimpan hasilnya dalam **Dictionary** terpisah (_ccValid_ dan _ccInvalid_).

# 

Adapun kriteria nomor kartu kredit yang valid adalah sebagai berikut:

- Diawali dengan angka __4__, **5** atau __6__.
- Terdiri atas tepat __16 digit__ angka.
- Hanya mengandung angka __0-9__.
- Boleh dituliskan berupa grup __4 digit__ yang dipisahkan dengan tanda hubung __"-"__
- Tidak boleh terdapat 1 angka yang diulang __>3x__ & tertulis secara beruntun, misal: 3333.

__Contoh__:
- ✅ Nomor kartu kredit __*valid*__:
    - __4253625879615781__
    - __4424424424442442__
    - __5122-2368-7954-3213__
    - __4123456789123454__
    - __5123-4567-8912-3455__
    - __4123356789123456__

- ❌ Nomor kartu kredit __*invalid*__:
    - __0525362587961578__ &nbsp;&nbsp;&nbsp;(tidak diawali dengan 4, 5 atau 6)
    - __42536258796157867__ &nbsp;&nbsp;&nbsp;(terdiri atas __17 digit__ angka)
    - __44244z4424442444__ &nbsp;&nbsp;&nbsp;(terdapat karakter __'z'__ yang bukan angka)
    - __5122.2368.7954.3214__ &nbsp;&nbsp;&nbsp;(dipisahkan bukan dengan tanda hubung)
    - __4424444424442444__ &nbsp;&nbsp;&nbsp;(terdapat angka yang diulang __>3x__ & tertulis secara beruntun, yaitu: __44444__)
    - __61234-123-8912-3456__ &nbsp;&nbsp;&nbsp;(terdapat grup yang tidak hanya terdiri atas 4 digit angka)
    - __5199-9967-7912-3457__  &nbsp;&nbsp;&nbsp;(terdapat angka yang diulang __>3x__ & tertulis secara beruntun, yaitu: __9999__)
    - __5123 - 4567 - 8912 - 3456__ &nbsp;&nbsp;&nbsp;(dipisahkan dengan tanda hubung & spasi)

__Input Berupa List yg berisi Dictionary Nasabah__  :

    ```
    ccNasabah = [
    {"nama": "Joni", "noCreditCard": "4253625879615781"},
    {"nama": "Andre", "noCreditCard": "5123-4567-8912-3455"},
    {"nama": "Adam", "noCreditCard": "0525362587961578"},
    {"nama": "Chris", "noCreditCard": "42536258796157867"},
    {"nama": "Chandra", "noCreditCard": "4424424424442442"},
    {"nama": "Desi", "noCreditCard": "44244z4424442444"},
    {"nama": "Lady", "noCreditCard": "5122.2368.7954.3214"},
    {"nama": "Mike", "noCreditCard": "4424444424442444"},
    {"nama": "John", "noCreditCard": "5122-2368-7954-3213"},
    {"nama": "Kopi", "noCreditCard": "61234-123-8912-3456"},
    {"nama": "Richard", "noCreditCard": "5199-9967-7912-3457"},
    {"nama": "Rick", "noCreditCard": "1111222233334444"},
    {"nama": "Mira", "noCreditCard": "5123 - 4567 - 8912 - 3456"},
    {"nama": "Dean", "noCreditCard": "4123356789123456"},
    {"nama": "Sam", "noCreditCard": "4123456789123454"}
    ]
    ```

__Function Initialization__

    ```python
    def ccValidation(..) :
        ....
    ```

__Use Function__

    ```
    ccValid, ccInvalid = ccValidation(ccNasabah)
    print(ccValid)
    print(ccInvalid)
    ```

__Output__ yang diharapkan:
- List __*ccValid*__ berisi data nasabah dengan nomor kartu kredit yang valid:
    ```json
    ccValid = [
        {"nama": "Joni", "noCreditCard": "4253625879615781"},
        {"nama": "Andre", "noCreditCard": "5123-4567-8912-3455"},
        {"nama": "Chandra", "noCreditCard": "4424424424442442"},
        {"nama": "John", "noCreditCard": "5122-2368-7954-3213"},
        {"nama": "Dean", "noCreditCard": "4123356789123456"},
        {"nama": "Sam", "noCreditCard": "4123456789123454"}
    ]
    ```
- List __*ccInvalid*__ berisi data nasabah dengan nomor kartu kredit yang tidak valid:
    ```json
    [
        {"nama": "Adam", "noCreditCard": "0525362587961578"},
        {"nama": "Chris", "noCreditCard": "42536258796157867"},
        {"nama": "Desi", "noCreditCard": "44244z4424442444"},
        {"nama": "Lady", "noCreditCard": "5122.2368.7954.3214"},
        {"nama": "Mike", "noCreditCard": "4424444424442444"},
        {"nama": "Kopi", "noCreditCard": "61234-123-8912-3456"},
        {"nama": "Richard", "noCreditCard": "5199-9967-7912-3457"},
        {"nama": "Rick", "noCreditCard": "1111222233334444"},
        {"nama": "Mira", "noCreditCard": "5123 - 4567 - 8912 - 3456"}
    ]
    ```

_**Catatan:**_ 


✅ Commit & push source code jawaban soal ini, beserta file JSON hasilnya ke __Github__ Anda, buatlah repo dengan nama __CC_Validation__, kemudian lampirkan __url link repo Github__ Anda via email ke _khumaeni@purwadhika.com!_ dan _operational_jkt@purweadhika.com_. Subject Email : **Remedial Modul 1 - JCDS12 - Nama**



<hr>

### *__#HappyCoding__* 
