# TUGAS-1-BIGDATA
  Nama : Raja Permata Boy<br>
  NRP  : 05111740000070<br>
  1.<b>Business Understanding</b><br>
  Kita bisa menentukan kota mana yang memiliki penduduk yang kaya, juga bisa memprediksi mulai umur berapa akan memiliki penghasilan       yang   besar, dan juga memprediksi pengaruh penghasilan terhadap sakit atau tidaknya. <br>
  2.<b>Data Understanding</b><br>
  Dataset ini memiliki 6 kolom dan 15000 baris dan menggunakan Number sebagai indeksnya.<br>
  Kolom City adalah kota tempat tinggal seseorang<br>
  Kolom Gender adalah jenis kelamin seseorang<br>
  Kolom Age adalah umur seseorang<br>
  Kolom Income adalah besaran pendapatan seseorang<br>
  Kolom Illness adalah apakah seseorang sakit atau tidak<br>
  <img src="/image/dataset.jpg"><br>
  
  3.<b>Data Preparation</b><br>
  Sebelum data di pisah, terlebih dahulu dibaca dengan CSV reader (karena format dataset adalah .csv)<br>
  <img src="/image/csvreader.jpg"><br>
  Lalu, dataset yg sudah berhasil dibaca maka akan kita pisah dengan menggunakan column splitter yang sudah ada di KNIME untuk membagi     tabel menjadi 2<br>
  <img src="/image/splitter.jpg"><br>
  Tabel Pertama saya isi dengan Gender, Age dan Ilness sedangkan tabel ke 2 yaitu City dan Income<br>
  <img src="/image/splitterconf.jpg"><br>
  Setelah itu tabel pertama saya masukkan ke database menggunakan database writer, sedangkan data kedua saya tulis dalam bentuk .csv       menggunakan csv reader<br>
  <img src="/image/splitterresult.jpg"><br>
  Untuk melakukan write ke database, kita terlebih dahulu harus tabel di database dan melakukan koneksi dengan database.
  <img src="/image/databaseconf.jpg"><br>
  
  4.<b>Modeling</b><br>
  Karena menggunakan 2 format yang berbeda yaitu .csv dan juga data dari database, maka saya menggunakan CSV reader dan juga Database     Reader<br>
  <img src="/image/modelling1.jpg"><br>
  Setelah pembacaan kedua dataset tersebut, saya melakukan append untuk menggabung kedua tabel tersebut. <br>
  Append dilakukan dengan row keys yang identik dan juga panjang row yang sama. <br>
  <img src="/image/modelling2.jpg"><br>
  
  5.<b>Evaluation</b><br>
  Append berhasil dilakukan. Untuk mengecek berhasil atau tidaknya, kita dapat mengecek apakah jumlah baris dan kolom sama dengan         dataset awal. Kita menggunakan Extract Dimension table untuk mengeceknya. Lalu kita jalankan, dan didapati hasilnya sama.<br>
  <img src="/image/eval1.jpg"><br>
          Ini dataset awal <br>
  <img src="/image/eval2.jpg"><br>
          Ini dataset akhir <br>
  6.<b>Deployment</b><br>
  Hasil dari Append akan kita taruh ke database menggunakan Database Writer dan juga ke file (format .csv) menggunakan CSV Writer.<br>
  <img src="/image/deployment.jpg"><br>
  
