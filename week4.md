# JavaScript Intermediate

- ## Apa itu Server?
  Server adalah sistem komputer yang memiliki layanan khusus berupa penyimpanan data. Data yang disimpan di dalam server adalah informasi. Layanan tersebut ditujukan khusus untuk client yang berkebutuhan dalam menyediakan informasi untuk usernya. User akan mengetikkan, mengklik atau menyorot apa yang mereka inginkan (request) melalui Web Apps, maka server akan mengecek apakah data yang diminta ada atau tidak di dalam database, jika ada maka server menerima request tersebut dan menyediakan apa yang user inginkan (response).
  Mengambil data dari server akan lebih efektif dan efisien daripada mengubabh konten secara langsung melalui file HTML.
  Website dinamis sekarang akan berkomunikasi dengan server melalui API.
- ## Asynchronus Async Await

  Async Await merupakan salah satu Asynchronus yang mirip dengan Promise, namun berbada dari segi syntax dan cara penggunaannya. Di dalam Async Await, terdapat 2 (dua) kata kunci, yaitu :

  - `async` untuk mengubah function synchronus menjadi asynchronus.
  - `await` untuk menunda eksekusi hingga proses asynchronus selesai.

  Sebuah async function bisa tidak berisi await sama sekali atau lebih dari satu await. Keyword await hanya bisa digunakan didalam async function, jika digunakan di luar async function maka akan terjadi error.

  - Async <br>
    Berikut contoh penggunaan async

    ```javascript
    // async menggunakan keyword function
    async function tesAsyncAwait() {
      return "Fulfilled";
    }
    consolle.log(tesAsyncAwait());

    // async menggunakan arrow function
    let tesAsyncAwait = async () => {
      return "Fulfilled";
    };
    console.log(tesAsyncAwait());
    ```

  - Await <br>
    `await` hanya bisa digunakan di dalam `async` dan `await` adalah keyword dalam `async` yang digunakan untuk menunda hingga proses asynchronous selesai.
    Berikut adalah cara penulisan async/awai:

    ```javascript
    async function tesAsyncAwait() {
      await "Fulfilled";
    }
    ```

    Kita bisa melakukan error handling dengan menggunakan `try` dan `catch`.

    ```javascript
    // Definisikan dahulu promise yang ingin digunakan
    let condition = true;
    let tesAsyncAwait = async (condition) => {
      if (condition) {
        return "Condition is fulfilled!";
      } else {
        throw "Condition is rejected!";
      }
    };

    // Membuat fungsi run menjadi asynchronous menggunakan async/await
    const run = async (condition) => {
      try {
        const message = await tesAsyncAwait(condition);
        console.log(message); // Output: Condition is fulfilled!
        console.log("After condition is fulfilled"); // Output: After condition is fulfilled
      } catch (error) {
        console.log(error);
      }
    };

    run(true);
    ```

- ## Asynchronus Fetch

  Fetch dalam JavaScript adalah salah satu Asynchronus yang memungkinkan kita untuk mangambil data dari internet (API). Fetch API adalah kegiatan meminta/request layana ke endpoint/letak url yang akan menerima request pada website secara lokal maupun public, untuk mengambil response atau source berupa data berformat json atau text yang basa dilakukan programmer untuk membangun website yang membutuhkan data dari website lain.
  Asynchronus Fetch dapat digunakan dengan promise dan async await.

  - Fetch dengan Promise <br>

    ```javascript
    fetch("https://jsonplaceholder.typicode.com/posts") //menghubungkan dengan api melalui url
      .then(function (response) {
        return response.json(); // .json() untuk unboxing data json
      })
      .then(function (post) {
        console.log(post);
      });
    ```

  - Fetch dengan async await
    ```javascript
    const tesFetchAsync = async () => {
      let response = await fetch("https://jsonplaceholder.typicode.com/posts");
      response = await response.json();
      console.log(response);
    };
    tesFetchAsync();
    ```

<br><br><br>

- ## Git dan GitHub Lanjutan
  Dengan Git dan GitHub kita bisa melakukan kolaborasi atau bekerja di dalam sebuah tim saat pengerjaan sebuah tim.
  Beberapa perintah yang digunakan untuk melakukan kolaborasi :
  1. `git colone` untuk menyalin repository GitHub ke dalam komputer kita. Dengan Git Clone, kita bisa mendapatkan seluruh isi suatu repositori dan mendapatkan perubahan terbaru pada repositori tersebut secara praktis.
  2. `git switch [nama-branch]` untuk berpindah ke dalam branch yang diinginkan.
  3. `git pull` untuk update kode/perbahan terbaru
  4. `git branch [nama-branch]` untuk membuat branch baru dimana setiap anggota kelompok akan mengerjakan tugasnya masing-masing.
  5. `git merge [nama-branch]` untuk menggabungkan branch yang aktif dan branch yang dipilih.
  6. Beberapa command dasar seperti `git commit`, `git add .`, `git push`, dll.

<br><br><br>

- ## Responsive Web Design

  Responsive Web Design bertujuan untuk membuat desain website dapat diakses dalam device apapun dengan baik dan rapih. <br>
  Terdapat beberapa cara agar wesbite kita menjadi responsive :

  1. Add Viewport in HTML <br>
     Ini adalah Meta Viewport yang ada di dalam HTML.
  2. Use Max-Width element <br>
     Max-width biasanya digunakan untuk gambar sehingga gambar akan memiliki ukuran yang sama sesuai dengan device yang digunakan.
  3. Media Query <br>
     Kita bisa menggunakan max-width dan max-height untuk media query.
     Media query digunakan untuk membuat beberapa styles tergantung pada jenis device yang digunakan. Kita bisa membuatnya di file css yang berbeda untuk masing-masing device, atau menggunakan 1 file css saja untuk semua device.
  4. Breakpoint <br>
     Perubahan yang terjadi pada tampilan saat berganti device atau ukuran widthnya disebut **breakpoint**
  5. CSS Relative Unit <br>
  6. Flexbox dan grid <br>
     <br><br><br>

- ## Bootstarp 5

  Bootstrap adalah framework CSS yang berfungsi untuk mendesain website responsive dengan cepat dan mudah. Framework open source ini diciptakan pada tahun 2011 oleh Mark Otto dan Jacob Thornton dari Twitter. Itulah kenapa dulunya Bootstrap dinamakan Twitter Blueprint. Bootstrap memiliki banyak kelas yang tinggal kita panggil jika kita ingin menggunakannya. Bootstrap bersifat responsive berkat grid system yang digunakan. Sistem grid pada bootstrap menggunakan rangkaian containers, baris, dan kolom untuk menyesuaikan bentuk layout dan konten website. <br>
  Bootstrap memiliki banyak kegunaan yang membuat kita menjadi lebih cepat untuk membuat sebuah komponen website, seperti saat ingin membuat navigasi bar, kita tinggal melihat **Components**, pilih **Navbar**, selanjutnya adalah tinggal pilih navigasi bar yang sesuai dengan kebutuhan kita, setelah itu tinggal copy source codenya dan paste ke dalam file HTML kita dan kita bisa modifikasi konten dari navigasi tersebut sesuai dengan kebutuhan kita. <br>
  Hal yang harus diperhatikan dalam membuat website kita menjadi responsive adalah terdapat dalam menu **Layout**. Di dalam menu **Layout** terdapat beberapa pilihan seperti:

  1. Breakpoints <br>
  Breakpoint adalah lebar yang dapat disesuaikan yang menentukan bagaimana tata letak responsive di seluruh perangkat atau ukuran viewport. Terdapat beberapa breakpoints yang tersedia :
  <table>
    <tr>
      <th>Breakpoints<th>
      <th>Class Infix<th>
      <th>Dimensions<th>
    </tr>
    <tr>
      <td>X-Small<td>
      <td>None</td>
      <td>< 576px</td>
    </tr>
    <tr>
      <td>Small<td>
      <td>sm</td>
      <td>>= 576px</td>
    </tr>
    <tr>
      <td>Medium<td>
      <td>md</td>
      <td>>= 768px</td>
    </tr>
    <tr>
      <td>Large<td>
      <td>lg</td>
      <td>>= 992px</td>
    </tr>
    <tr>
      <td>Extra Large<td>
      <td>xl</td>
      <td>>= 1200px</td>
    </tr>
    <tr>
      <td>Extra extra Large<td>
      <td>xxl</td>
      <td>>= 1400px</td>
    </tr>
  </table>

  2. Containers <br>
     Container adalah elemen paling dasar dalam layout bootstrap. Terdapat 3 macam container dalam bootstrap, yaitu: <br>

     - Default Container <br>
       Class container memiliki sifat yang responsive dan fixed-width, yang berarti lebarnya akan berubah pada setiap breakpoint.

     ```html
     <div class="container">
       <!-- tuliskan kode disini -->
     </div>
     ```

     - Fluid Container
       Class container-fluid memiliki lebar yang sama dengan viewport

     ```html
     <div class="container-fluid">
       <!-- tuliskan kode disini -->
     </div>
     ```

     - Responsive Container

     ```html
     <div class="container-sm">100% wide until small breakpoint</div>
     <div class="container-md">100% wide until medium breakpoint</div>
     <div class="container-lg">100% wide until large breakpoint</div>
     <div class="container-xl">100% wide until extra large breakpoint</div>
     <div class="container-xxl">100% wide until extra extra large breakpoint</div>
     ```

  3. Grid <br>
     Grid biasanya digunakan bersamaan dengan container dan row serta col
  4. Columns <br>
     Columns adalah bagian dari container dan grid
  5. Gutters <br>
     Gutters adalah padding diantara kolom, biasanya digunakan untuk memberi ruang secara responsive dan menyelaraskan konten dalam sistem.
  6. Utilities <br>

  7. Z-index
