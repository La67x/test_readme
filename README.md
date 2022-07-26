###### Nama : Bagus Rachmad Aditya Wicaksono
###### Kelas : XII RPL 1/18


# MODUL 1

Soal.
1. Lakukan proses instalasi Framework Laravel ke dalam folder dengan nama masing-masing.

   Pertama kita akan merubah title nama seperti gambar di bawah ini.
   
   ## Langkah Kedua.
   
   Kita akan memasukkan Command Prompt atau CMD.
![image](https://user-images.githubusercontent.com/109930395/180905905-d73e53d4-cd0f-44e9-af4e-8bbae364ab05.png)

 
```
composer create-project laravel/laravel_penjualan
```
# MODUL 2 
Soal 1

Buatlah migration tabel kategori dengan menggunakan teknik yang telah di pelajari dalam modul ini.

## Langkah Pertama.

Kita akan membuat suatu folder model kategori, gunakan perintah artisan pada terminal Visual Studio Code sebagai berikut.

```
php artisan make:model kategori
```

## Langkah kedua.

lalu edit isi kategori menjadi berikut 

```
<?php

namespace App\Models;
use Illuminate\DataBase\Eloquent\Factories\HasFactory;
use Illuminate\DataBase\Eloquent\Model;

class kategori extends Model
{
use HasFactory;

protected $table = 'kategori';
}

```
![image](https://user-images.githubusercontent.com/109930395/180912299-9b7e44d6-af42-47ba-8144-acd56cc70952.png)

## Langkah Ketiga.

Selanjutnya membuat createKategoriTable, dan gunakan perintah artisan di terminal Visual Studio Code

```
php artisan make:migration create_kategori_table
```

## Langkah Keempat.

Setelah itu, kita isi folder tersebut seperti ini.
```
<?php

use Illuminate\Database\Migrations\Migration;
use Illuminate\Database\Schema\Blueprint;
use Illuminate\Support\Facades\Schema;

return new class extends Migration
{
    /**
     * Run the migrations.
     *
     * @return void
     */
    public function up()
    {
        Schema::create('katagori', function (Blueprint $table) {
            $table->id();
            $table->string('name');
            $table->timestamps();
        });
    }

    /**
     * Reverse the migrations.
     *
     * @return void
     */
    public function down()
    {
        Schema::dropIfExists('katagori');
    }
};
```
## Langkah Kelima.

Setelah kalian isi, selanjutnya adalah membuat kategoriTableSeeder dengan menggunakan perintah artisan di terminal Visual Studio Code. 

```
php artisan make:seeder kategoriTableSeeder
```

## Langkah Ke enam.

Kita tambahkan use DB; agar program nya bisa di jalankan, dan isi kategoriTableSeeder sebagai berikut.

![image](https://user-images.githubusercontent.com/109930395/180917128-c9bc3c22-0c54-47f9-bb36-0c6f1fe3a4f8.png)

## Langkah Ke Tujuh.

Lalu tambahkan Codingan di modul DatabaseSeeder seperti berikut.

![image](https://user-images.githubusercontent.com/109930395/180917290-8afba112-fdb1-4a90-9cf2-0814440d6e7f.png)

Soal 2

 2.Berikan data dengan menggunakan seeder yang telah di pelajari sebelumnya pada modul ini.
 
 Seeder digunakan untuk membuat contoh data pada data base. Fitur ini sangat bermanfaat saat melakukan pengembangan suatu sistem yang dimana kita memerlukan suatu contoh data. Apalagi ketika membutuhkan contoh data yang banyak, fitur ini dapat membantu dari pada memasukkan data satu persatu secara manual melalui PhpMyAdmin.


