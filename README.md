# Pemrograman Web 2

**Nama :** Anggita Risqi Nur Clarita

**NIM :** 312210450

**Kelas :** TI.22.A.4

**Dosen Pengampu :** Agung Nugroho, S.Kom., M.Kom.

## DAFTAR ISI <br>

| No  | Description | Link                       |
| --- | ----------- | -------------------------- |
| 1   | Praktikum 1 | [Click Here](#praktikum-1) |
| 2   | Praktikum 2 | [Click Here](#praktikum-2) |
| 3   | Praktikum 3 | [Click Here](#praktikum-3) |
| 4   | Praktikum 4 | [Click Here](#praktikum-4) |

## Praktikum 1-4

> ### Instruksi Praktikum
>
> 1. Persiapkan text editor misalnya **VSCode**.
>
> 2. Buat folder baru dengan nama _lab11_ci_ pada docroot webserver **(htdocs)**
>
> 3. Ikuti langkah-langkah praktikum yang akan dijelaskan berikutnya 😉.

## Praktikum 1

### Instalasi dan Penggunaan CodeIgniter 4

Untuk melakukan instalasi **Codeigniter 4** dapat dilakukan dengan dua cara, yaitu cara _manual_ dan menggunakan _composer_. Pada praktikum ini kita menggunakan cara **manual** _(tapi kalau mau pakai composer juga boleh kok)_ 😸.

- Unduh Codeigniter dari website https://codeigniter.com/download
- Extrak file zip Codeigniter ke direktori htdocs/_(folder kalian)_.
- Ubah nama direktory **framework-4.x.xx** menjadi **ci4**.

1. **Aktifkan Extension di XAMPP Control Panel**

   Untuk mengaktifkan extension tersebut, melalui **XAMPP Control Panel**, pada bagian apache klik **_config_**. Setelah itu lanjut dengan mengklik **PHP (php.ini)**

   ![1](https://github.com/AnggitaRisqiNC/WebProgram_ci4/assets/115614419/82bcfbbe-a74d-4dda-9e10-45040d0a7435)

   Pada bagian extension, hilangkan tanda **; _(titik koma)_** pada ekstensi yang akan diaktifkan. Kemudian save atau simpan kembali filenya dan restart **Apache web server**.

   Extension yang perlu diaktifkan :

   - **php-json** extension untuk bekerja dengan JSON.

   - **php-mysqlnd** native driver extension untuk MySQL.

   - **php-xml** extension untuk bekerja dengan XML.

   - **php-intl** extension untuk membuat aplikasi multibahasa.

   - **libcurl** (opsional), jika ingin pakai Curl.

   ![2](https://github.com/AnggitaRisqiNC/WebProgram_ci4/assets/115614419/7a74570d-60cb-4f36-88ef-250cd651f293)

   Setelah melakukan restart **Apache web server**, silahkan nyalakan kembali Apache _(pastikan tidak ada yang error!)_ 😸.

   Kalian dapat membuka browser dengan alamat http://localhost/lab11_ci/ci4/public

   ![3](https://github.com/AnggitaRisqiNC/WebProgram_ci4/assets/115614419/19b98d1b-8a87-499c-b873-67b049b8f6b9)

2. **Menjalankan CLI _(Command Line Interface)_**

   Kalian dapat membuka atau menjalankan **CLI _(Command Line Interface)_**, Codeigniter 4 menyediakan CLI untuk mempermudah proses development. Untuk mengakses CLI buka _terminal/command prompt_ yang telah disediakan **XAMPP**.

   Selanjutnya arahkan lokasi directory sesuai dengan directory project yang kalian buat **(xampp/htdocs/lab11_ci/ci4)**

   Kemudian jalankan perintah untuk memanggil CLI Codeigniter dengan script ini :

   ```cs
   php spark
   ```

   **spark** adalah program atau script yang berfungsi untuk menjalankan server, generate kode, dll.

   ![4](https://github.com/AnggitaRisqiNC/WebProgram_ci4/assets/115614419/22eda02b-793c-4142-9999-bf74d71233a1)

3. **Mengaktifkan Mode Debugging**

   Codeigniter 4 menyediakan fitur **debugging** untuk memudahkan developer untuk mengetahui pesan error apabila terjadi kesalahan dalam membuat kode program.

   Untuk memudahkan mengetahui jenis errornya, maka perlu mengaktifkan mode debugging dengan cara mengubah nilai konfigurasi pada environment variable **CI_ENVIRONMENT** menjadi **development** pada file **env** lalu ubah **env** menjadi **.env**.

   **.env** adalah file yang berisi variabel environment yang dibutuhkan oleh aplikasi.

   ![5](https://github.com/AnggitaRisqiNC/WebProgram_ci4/assets/115614419/3cdc5dd9-11a2-4305-8f20-10e4c3d10a5f)

4. **Membuat Routes Baru**

   Kalian dapat menambahkan script ini ke dalam file Routes :

   ![6](https://github.com/AnggitaRisqiNC/WebProgram_ci4/assets/115614419/ce4caa5c-f3e8-4ee7-80fd-5eddf9777b30)

   Untuk mengetahui routes yang ditambahkan sudah benar, buka **CLI _(Command Line Interface)_** dan jalankan perintah berikut :

   ```cs
   php spark routes
   ```

   ![7](https://github.com/AnggitaRisqiNC/WebProgram_ci4/assets/115614419/93370be5-b3f1-4cff-8a8e-03cabda87c7f)

   Selanjutnya coba kalian akses routes yang telah dibuat dengan mengakses alamat http://localhost/lab11_ci/ci4/public/about pasti hasilnya seperti ini :

   ![8](https://github.com/AnggitaRisqiNC/WebProgram_ci4/assets/115614419/81177d35-1b95-4755-b78e-8ec55278d57e)

   Ketika kita akses dan muncul tampilan **_404 Controller or its method is not found_**, itu artinya file/page tersebut tidak ada 😔. Untuk dapat mengakses halaman tersebut, harus dibuat terlebih dahulu Controller yang sesuai dengan routing yang dibuat yaitu di Controller Page 😀.

5. **Membuat Controller**

   Selanjutnya adalah membuat **Controller Page**. Buat file baru dengan nama **page.php** pada direktori Controllers, kemudian isi scriptnya seperti berikut.

   ![9](https://github.com/AnggitaRisqiNC/WebProgram_ci4/assets/115614419/544452da-80c3-4509-9c00-51d2a31ed936)

   Kemudian coba kalian akses kembali routes yang telah dibuat dengan mengakses alamat http://localhost/lab11_ci/ci4/public/about pasti hasilnya akan tampil seperti ini 😼 :

   ![10](https://github.com/AnggitaRisqiNC/WebProgram_ci4/assets/115614419/314bdee2-7877-438f-9a4d-8eeec57f9097)

6. **Membuat Auto Routing**

   Secara default fitur **_autoroute_** pada Codeiginiter itu sudah aktif. Untuk mengubah status autoroute dapat mengubah nilai variabelnya. Untuk menonaktifkan ubah nilai **true** menjadi **false**.

   Tambahkan method baru pada **Controller Page** seperti berikut.

   ![11](https://github.com/AnggitaRisqiNC/WebProgram_ci4/assets/115614419/4a80af82-85c7-43ab-83e1-985785a8a88f)

   Kemudian coba kalian check http://localhost/lab11_ci/ci4/public/page/tos pasti hasilnya akan tampil seperti ini 🙀 :

   ![12](https://github.com/AnggitaRisqiNC/WebProgram_ci4/assets/115614419/93f66ccc-c3f7-4770-b150-5ad228ffa118)

7. **Membuat Views**

   Selanjutnya adalah membuat views untuk tampilan web agar lebih menarik. Buat file baru dengan nama **about.php** pada direktori view **(app/Views/About.php)** kemudian kalian isi scriptnya seperti berikut :

   ![13](https://github.com/AnggitaRisqiNC/WebProgram_ci4/assets/115614419/078eadbe-ed83-4cc3-ae51-bf8cbcc168f9)

   Untuk script code **method about** pada class **Controller Page** seperti berikut:

   ```php
   public function about()
   {
       return view('about', [
           'title' => 'Halaman About',
           'content' => 'Ini adalah halaman abaut yang menjelaskan tentang isi halaman ini.'
       ]);
   }
   ```

   Kemudian coba kalian refresh routes http://localhost/lab11_ci/ci4/public/about pasti hasilnya akan tampil seperti ini 🙀 :

   ![14](https://github.com/AnggitaRisqiNC/WebProgram_ci4/assets/115614419/e7b578ed-63ed-4fff-832b-a6f0805d1a5c)

   **_Yippie!_** Sekarang kalian bisa menggunakan framework Codeigniter 4 untuk project kalian! Untuk **tugas selanjutnya** silahkan lakukan caranya sama seperti tadi. 🥳

8. **Membuat Layout Web dengan CSS**

   Buat _file css_ pada direktori public dengan nama **style.css** (copy file dari praktikum **lab4_layout**.) Kita akan gunakan layout yang pernah dibuat pada praktikum 4.

   ![15](https://github.com/AnggitaRisqiNC/WebProgram_ci4/assets/115614419/d44087da-9a72-46c7-8bb1-5eb3df8c3f99)

   Kemudian buat folder template pada direktori view kemudian buat file **header.php** dan **footer.php** pada direktori view **(app/view/template/)**

   ![16](https://github.com/AnggitaRisqiNC/WebProgram_ci4/assets/115614419/b04c1e1d-5a24-4fd5-8649-d0ac8a5a67e6)

   Kemudian coba kalian refresh routes http://localhost:8080/about pasti hasilnya akan tampil seperti ini 🙀 :

   ![17](https://github.com/AnggitaRisqiNC/WebProgram_ci4/assets/115614419/86d5f404-bc03-45aa-8e50-a251a066e601)

## Praktikum 2

### Framework Lanjutan (CRUD)

Untuk memulai membuat aplikasi CRUD sederhana, yang perlu disiapkan adalah database server menggunakan MySQL. Pastikan MySQL Server sudah dapat dijalankan melalui
XAMPP 😸.

1. **Membuat Database: Studi Kasus Data Artikel**

   ```sql
   CREATE DATABASE lab_ci4;
   ```

   ```sql
   CREATE TABLE artikel (
   id INT(11) auto_increment,
   judul VARCHAR(200) NOT NULL,
   isi TEXT,
   gambar VARCHAR(200),
   status TINYINT(1) DEFAULT 0,
   slug VARCHAR(200),
   PRIMARY KEY(id)
   );
   ```

   ![18](https://github.com/AnggitaRisqiNC/WebProgram_ci4/assets/115614419/ff027f9d-4e65-40be-960b-52042d0a70e0)

2. **Konfigurasi koneksi database**

   Selanjutnya membuat konfigurasi untuk menghubungkan dengan database server. Konfigurasi dapat dilakukan dengan du acara, yaitu pada **file app/config/database**.php atau menggunakan file **.env**. Pada praktikum ini kita gunakan konfigurasi pada file **.env**.

   ![19](https://github.com/AnggitaRisqiNC/WebProgram_ci4/assets/115614419/8b6b6639-079f-4c3a-95cc-d4c699694f94)

3. **Membuat Model dan Controllers**

   Selanjutnya adalah membuat Model untuk memproses data Artikel. Buat file baru pada direktori **app/Models** dengan nama **ArtikelModel.php** dan membuat Controller baru dengan nama Artikel.php pada direktori **app/Controllers**.

   ![20](https://github.com/AnggitaRisqiNC/WebProgram_ci4/assets/115614419/847126ea-6009-477c-af30-e817e3e904f6)

4. **Membuat View**

   Untuk membuat View maka buat direktori baru dengan nama artikel pada direktori **app/views**, kemudian buat file baru dengan nama **index.php**.

   ![21](https://github.com/AnggitaRisqiNC/WebProgram_ci4/assets/115614419/085b5e46-c9c4-4cde-8fbf-8a0c446ae8b9)

   Selanjutnya buka browser kembali, dengan mengakses url http://localhost:8080/artikel 😉.

   ![22](https://github.com/AnggitaRisqiNC/WebProgram_ci4/assets/115614419/c5fa4613-8c00-48e0-a21a-5aec987a7b35)

   Ketika kita akses dan muncul tampilan **Belum Ada Data**, itu artinya datanya belum kita isi pada database tersebut 😔. Agar dapat melihat datanya, harus ditambah terlebih dahulu data pada database agar datanya dapat ditampilkan 😀.

   ![23](https://github.com/AnggitaRisqiNC/WebProgram_ci4/assets/115614419/dd47c01e-5be1-44ca-a67b-dfee79967b3a)

5. **Membuat Tampilan Detail Artikel**

   Tampilan pada saat judul berita di klik maka akan diarahkan ke halaman yang berbeda. Tambahkan fungsi baru pada Controller Artikel dengan nama view().

   ```php
   public function view($slug)
       {
           $model = new ArtikelModel();
           $artikel = $model->where(['slug' => $slug])->first();

           // Menampilkan error apabila data tidak ada.
           if (!$artikel) {
               throw PageNotFoundException::forPageNotFound();
           }
           $title = $artikel['judul'];
           return view('artikel/detail', compact('artikel', 'title'));
       }
   ```

   Buat view baru untuk halaman detail dengan nama app/views/artikel/detail.php.

   ```php
   <?= $this->include('template/header'); ?>

    <article class="entry">
        <h2><?= $artikel['judul']; ?></h2>
        <img src="<?= base_url('/gambar/' . $artikel['gambar']); ?>" alt="<?= $artikel['judul']; ?>">
        <p><?= $artikel['isi']; ?></p>
    </article>

    <?= $this->include('template/footer'); ?>
   ```

   ![24](https://github.com/AnggitaRisqiNC/WebProgram_ci4/assets/115614419/d3a51a48-2a42-4599-9999-43f551d7a262)

   Selanjutnya, buka kembali file app/config/Routes.php, kemudian tambahkan routing untuk artikel detail.

   ```php
   $routes->get('/artikel/(:any)', 'Artikel::view/$1');
   ```

   ![25](https://github.com/AnggitaRisqiNC/WebProgram_ci4/assets/115614419/c0e0e1eb-4219-4cd9-8333-1b44d49d5c36)

6. **Membuat Menu Admin**

   Menu admin adalah untuk proses CRUD data artikel. Buat method baru pada Controller Artikel dengan nama **admin_index()**. Dan jangan lupa tambahkan routing untuk menu admin seperti berikut.

   ![26](https://github.com/AnggitaRisqiNC/WebProgram_ci4/assets/115614419/bf02a470-f33f-4be2-8bd7-f04d03686f2f)

   Buat file untuk style bagian admin dengan nama **Admin.css** dan **admin_header.php** dan juga **admin_footer.php**

   ![27](https://github.com/AnggitaRisqiNC/WebProgram_ci4/assets/115614419/1fdc78eb-847e-4f6c-bb62-c330a66150ef)

   Selanjutnya coba kalian akses routes yang telah dibuat dengan mengakses alamat http://localhost:8080/admin/artikel pasti hasilnya seperti ini :

   ![28](https://github.com/AnggitaRisqiNC/WebProgram_ci4/assets/115614419/4577d734-c355-48e3-abdc-eaf6899c0db7)

7. **Menambah Data Artikel**

   Tambahkan fungsi/method baru pada **Controller Artikel** dengan nama **add()**.

   ```php
   public function add()
   {
       // validasi data.
       $validation = \Config\Services::validation();
       $validation->setRules(['judul' => 'required']);
       $isDataValid = $validation->withRequest($this->request)->run();

       if ($isDataValid) {
           $artikel = new ArtikelModel();
           $artikel->insert([
               'judul' => $this->request->getPost('judul'),
               'isi' => $this->request->getPost('isi'),
               'slug' => url_title($this->request->getPost('judul')),
           ]);
           return redirect('admin/artikel');
       }
       $title = "Tambah Artikel";
       return view('artikel/form_add', compact('title'));
   }
   ```

   Kemudian buat view untuk form tambah dengan nama **form_add.php**

   ```php
   <?= $this->include('template/admin_header'); ?>

   <h2><?= $title; ?></h2>
   <form action="" method="post">
       <p>
           <input type="text" name="judul">
       </p>
       <p>
           <textarea name="isi" cols="50" rows="10"></textarea>
       </p>
       <p><input type="submit" value="Kirim" class="btn btn-large"></p>
   </form>

   <?= $this->include('template/admin_footer'); ?>
   ```

   Selanjutnya coba kalian akses routes yang telah dibuat dengan mengakses alamat http://localhost:8080/admin/artikel/add pasti hasilnya seperti ini :

   ![29](https://github.com/AnggitaRisqiNC/WebProgram_ci4/assets/115614419/0499f140-463c-4bd9-aab6-27ed299e2281)

8. **Menambah Data Artikel**

   Tambahkan fungsi/method baru pada **Controller Artikel** dengan nama **edit()**.

   ```php
   public function edit($id)
   {
       $artikel = new ArtikelModel();

       // validasi data.
       $validation = \Config\Services::validation();
       $validation->setRules(['judul' => 'required']);
       $isDataValid = $validation->withRequest($this->request)->run();

       if ($isDataValid) {
           $artikel->update($id, [
               'judul' => $this->request->getPost('judul'),
               'isi' => $this->request->getPost('isi'),
           ]);
           return redirect('admin/artikel');
       }

       // ambil data lama
       $data = $artikel->where('id', $id)->first();
       $title = "Edit Artikel";
       return view('artikel/form_edit', compact('title', 'data'));
   }
   ```

   Kemudian buat view untuk form tambah dengan nama **form_edit.php**

   ```php
   <?= $this->include('template/admin_header'); ?>

   <h2><?= $title; ?></h2>
   <form action="" method="post">
       <p><input type="text" name="judul" value="<?= $data['judul']; ?>"></p>
       <p><textarea name="isi" cols="50" rows="10"><?= $data['isi']; ?></textarea></p>
       <p><input type="submit" value="Kirim" class="btn btn-large"></p>
   </form>

   <?= $this->include('template/admin_footer'); ?>
   ```

   Selanjutnya coba kalian akses routes yang telah dibuat dengan mengakses alamat http://localhost:8080/admin/artikel/edit pasti hasilnya seperti ini :

   ![30](https://github.com/AnggitaRisqiNC/WebProgram_ci4/assets/115614419/3e5a2c67-06ab-40f1-ad40-1a6805c3650e)

9. **Menghapus Data**

   Tambahkan fungsi/method baru pada Controller Artikel dengan nama **delete()**.

   ```php
   public function delete($id)
   {
       $artikel = new ArtikelModel();
       $artikel->delete($id);
       return redirect('admin/artikel');
   }
   ```

   ![31](https://github.com/AnggitaRisqiNC/WebProgram_ci4/assets/115614419/81645381-392e-4af2-940a-e00ac9948166)

## Praktikum 3

### Framework Lanjutan (Modul Login)

Untuk memulai membuat modul Login, yang perlu disiapkan adalah database server menggunakan MySQL. Pastikan MySQL Server sudah dapat dijalankan melalui XAMPP 😸.

![32](https://github.com/AnggitaRisqiNC/WebProgram_ci4/assets/115614419/b55daaa1-dab2-43c8-affa-746f69bd92a0)

1. **Membuat Tabel: User Login**

   Selanjutnya adalah membuat Model untuk memproses data Login. Buat file baru pada direktori **app/Models** dengan nama **UserModel.php**

   ```php
   <?php

   namespace App\Models;

   use CodeIgniter\Model;

   class ArtikelModel extends Model
   {
       protected $table = 'artikel';
       protected $primaryKey = 'id';
       protected $useAutoIncrement = true;
       protected $allowedFields = ['judul', 'isi', 'status', 'slug', 'gambar'];
   }
   ```

2. **Membuat Controller User**

   Buat Controller baru dengan nama **User.php** pada direktori a**pp/Controllers**. Kemudian tambahkan method **index()** untuk menampilkan daftar user, dan method **login()** untuk proses login.

   ```php
   <?php

   namespace App\Controllers;

   use App\Models\UserModel;

   class User extends BaseController
   {
       public function index()
       {
           $title = 'Daftar User';
           $model = new UserModel();
           $users = $model->findAll();
           return view('user/index', compact('users', 'title'));
       }

       public function login()
       {
           helper(['form']);
           $email = $this->request->getPost('email');
           $password = $this->request->getPost('password');
           if (!$email) {
               return view('user/login');
           }
           $session = session();
           $model = new UserModel();
           $login = $model->where('useremail', $email)->first();
           if ($login) {
               $pass = $login['userpassword'];
               if (password_verify($password, $pass)) {
                   $login_data = [
                       'user_id' => $login['id'],
                       'user_name' => $login['username'],
                       'user_email' => $login['useremail'],
                       'logged_in' => TRUE,
                   ];
                   $session->set($login_data);
                   return redirect('admin/artikel');
               } else {
                   $session->setFlashdata("flash_msg", "Password salah.");
                   return redirect()->to('/user/login');
               }
           } else {
               $session->setFlashdata("flash_msg", "email tidak terdaftar.");
               return redirect()->to('/user/login');
           }
       }
   }
   ```

3. **Membuat View Login**

   Buat direktori baru dengan nama user pada direktori app/views, kemudian buat file baru dengan nama login.php.

   ```php
   <!DOCTYPE html>
   <html lang="en">

   <head>
       <meta charset="UTF-8">
       <title>Login</title>
       <link rel="stylesheet" href="<?= base_url('/style.css'); ?>">
   </head>

   <body>
       <div id="login-wrapper">
           <h1>Sign In</h1> <?php if (session()->getFlashdata('flash_msg')) : ?> <div class="alert alert-danger"><?= session()->getFlashdata('flash_msg') ?></div> <?php endif; ?> <form action="" method="post">
               <div class="mb-3"> <label for="InputForEmail" class="form-label">Email address</label> <input type="email" name="email" class="form-control" id="InputForEmail" value="<?= set_value('email') ?>"> </div>
               <div class="mb-3"> <label for="InputForPassword" class="form-label">Password</label><input type="password" name="password" class="form-control" id="InputForPassword"> </div> <button type="submit" class="btn btn-primary">Login</button>
           </form>
       </div>
   </body>

   </html>
   ```

4. **Membuat Database Seeder**

   Database seeder digunakan untuk membuat data dummy. Untuk keperluan ujicoba modul login, kita perlu memasukkan data user dan password kedaalam database. Untuk itu buat database seeder untuk tabel user. Buka CLI, kemudian tulis perintah berikut:

   ![33](https://github.com/AnggitaRisqiNC/WebProgram_ci4/assets/115614419/5d600839-7844-4dc4-a508-02297372ad2e)

   Selanjutnya, buka file **UserSeeder.php** yang berada di lokasi direktori **/app/Database/Seeds/UserSeeder.php** kemudian isi dengan kode berikut:

   ```php
   <?php

   namespace App\Database\Seeds;

   use CodeIgniter\Database\Seeder;

   class UserSeeder extends Seeder
   {
       public function run()
       {
           $model = model('UserModel');
           $model->insert([
               'username' => 'admin',
               'useremail' => 'admin@email.com',
               'userpassword' => password_hash('admin123', PASSWORD_DEFAULT),
           ]);
       }
   }
   ```

   Selanjutnya buka kembali CLI dan ketik perintah berikut:

   ![34](https://github.com/AnggitaRisqiNC/WebProgram_ci4/assets/115614419/aa2dda35-05d4-4b82-9f50-1358c58ce76e)

5. **Menambahkan Auth Filter**

   Selanjutnya membuat filer untuk halaman admin. Buat file baru dengan nama Auth.php pada direktori **app/Filters**.

   ![35](https://github.com/AnggitaRisqiNC/WebProgram_ci4/assets/115614419/622702ed-2179-4540-bdbb-b335575483f1)

   Selanjutnya buka file **app/Config/Filters.php** dan app/Config/Routes.php dan tambahkan kode berikut:

   ![36](https://github.com/AnggitaRisqiNC/WebProgram_ci4/assets/115614419/7bdd4d90-4d24-4e91-808b-c36b451ed0b0)

6. **Percobaan Akses Menu Admin**

   Buka url dengan alamat http://localhost:8080/admin/artikel ketika alamat tersebut diakses maka, akan dimunculkan halaman login.

   ![37](https://github.com/AnggitaRisqiNC/WebProgram_ci4/assets/115614419/981477dc-e89e-4f0c-a4ff-aceeec148a8d)

   ![38](https://github.com/AnggitaRisqiNC/WebProgram_ci4/assets/115614419/a32cbc93-a8c3-4f09-8750-0f92192c5d61)

7. **Fungsi Logout**

   Tambahkan method logout pada Controller User seperti berikut:

   ```php
   public function logout()
       {
           session()->destroy();
           return redirect()->to('/user/login');
       }
   ```

   ![39](https://github.com/AnggitaRisqiNC/WebProgram_ci4/assets/115614419/d82493a3-6bd9-467d-af5a-727029f64cbc)

## Praktikum 4

### Pagination dan Pencarian

1. **Membuat Pagination**

   Untuk membuat pagination, buka Kembali **Controller Artikel**, kemudian modifikasi kode pada method **admin_index** seperti berikut 😀.

   ```php
   public function admin_index()
   {
       $title = 'Daftar Artikel';
       $model = new ArtikelModel();
       $data = [
           'title' => $title,
           'artikel' => $model->paginate(10), #data dibatasi 10 record
           per halaman
           'pager' => $model->pager,
       ];
       return view('artikel/admin_index', $data);
   }
   ```

   Kemudian buka file v**iews/artikel/admin_index.php** dan tambahkan kode berikut dibawah deklarasi tabel data.

   ```php
   <?= $pager->links(); ?>
   ```

   Selanjutnya buka kembali menu daftar artikel, tambahkan data lagi untuk melihat hasilnya.

   ![40](https://github.com/AnggitaRisqiNC/WebProgram_ci4/assets/115614419/12c0be33-8088-4627-8a54-37a824f524c0)

2. **Membuat Pencarian**

   Untuk membuat pencarian data, buka kembali **Controller Artikel**, pada method **admin_index** ubah kodenya seperti berikut 😀.

   ```php
       public function admin_index()
       {
           $title = 'Daftar Artikel';
           $q = $this->request->getVar('q') ?? '';
           $model = new ArtikelModel();
           $data = [
               'title' => $title,
               'q' => $q,
               'artikel' => $model->like('judul', $q)->paginate(2), # data dibatasi 2 record per halaman
               'pager' => $model->pager,
           ];
           return view('artikel/admin_index', $data);
       }
   ```

   Kemudian buka kembali **file views/artikel/admin_index.php** dan tambahkan form pencarian sebelum deklarasi tabel seperti berikut:

   ```php
   <form method="get" class="form-search">
       <input type="text" name="q" value="<?= $q; ?>" placeholder="Cari data">
       <input type="submit" value="Cari" class="btn btn-primary">
   </form>
   ```

   Dan pada link pager ubah seperti berikut.

   ```php
   <?= $pager->only(['q'])->links(); ?>
   ```

   Selanjutnya buka kembali menu daftar artikel, tambahkan data lagi untuk melihat hasilnya.

   ![41](https://github.com/AnggitaRisqiNC/WebProgram_ci4/assets/115614419/ec765a10-5967-4121-8873-364e4c05f3c1)

## Finish 🥳
