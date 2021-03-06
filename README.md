# markovchain untuk menghitung peluang naik turun saham
Penentuan Peluang Naik Turun Harga Saham Harian 1 Interval dengan Simulasi Markov Chain menggunakan MATLAB 2015

Data yang digunakan berasal dari data Yahoo Finance dan contoh yang digunakan merupakan data saham Bank BCA periode 6 November 2017 hingga 6 November 2018 dengan detail data yang diambil sebagai berikut :<br>
<p align="center">
  <img src="https://github.com/ayunimatulf/markovchain/blob/master/data_saham.PNG">
</p>
Keterangan :<br>
	Close : Harga Saham Penutupan pada tanggal t.<br>
	Moving Avarage : Harga Saham Penutupan pada tanggal sebelumnya (t-1).<br>
	Delta Price : Selisih antara Moving Avarage – Close. <br>
	State dan State Description : Kode status saham dan penjelasannya ada 5 kategori yaitu :<br>
	1 : Naik Drastis <br>
	2 : Naik <br>
	3 : Tetap <br>
	4 : Turun <br>
	5 : Turun Drastis <br>
Sedangkan fungsi yang digunakan untuk kategorisasi adalah 
<p align="left">
  <img src="https://github.com/ayunimatulf/markovchain/blob/master/function.PNG">
</p><br>

## Metodologi
1.  Memasukkan input berupa data excel seperti tercantum diatas beserta table fungsi untuk kategorisasi kondisi seperti berikut : <br>
	<p align="center">
	  <img src="https://github.com/ayunimatulf/markovchain/blob/master/fungsi_kategorisasi.PNG">
	</p>
2.  Menghitung banyak data dalam setiap transisi kondisi kemudian membuat matriks P dengan menghitung peluang setiap kondisi dimana setiap kolom memiliki ∑▒P=1
	<p align="center">
	  <img src="https://github.com/ayunimatulf/markovchain/blob/master/matriks_transisi.PNG">
	</p>
3. Menghitung banyak data dalam setiap transisi kondisi kemudian dihitung peluangnya dengan setiap kolom memiliki ∑▒P=1
4. Menentukan status kondisi hari ini untuk melihat peluang keesokan harinya maka digunakan matriks P namun jika mencari peluang 3 hari kemudian maka maka digunakan matriks P^3 dan seterusnya. 

### Tampilan GUI
* Menu Upload Data
	<p align="center">
	  <img src="https://github.com/ayunimatulf/markovchain/blob/master/menu_upload.png">
	</p>
* Menu Matriks Transisi
	<p align="center">
	  <img src="https://github.com/ayunimatulf/markovchain/blob/master/menu_matriks_transisi.png">
	</p>
* Menu Prediksi Peluang
	<p align="center">
	  <img src="https://github.com/ayunimatulf/markovchain/blob/master/menu_predisi_peluang.png">
	</p>
