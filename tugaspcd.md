<div style="text-align: center;">
   <h2> Tugas Pemrosesan Citra Digital</h2>
</div>

<div style="text-align: center;">
  <img src="download.png" alt="alt text" />
</div>

<div style="text-align: center;">
   <h5> Nama: </h5> <p> Muhammad Rizfani   (2310131110006)</p>
   <h5> Dosen Pengampu: </h5> <p> Dr.Harja Santana Purba,M.Kom.</p><p>Novan A.B.Saputra, S.Kom.,M.T</p>
</div>

<br>
<br>
<br>
<br>
<br>

<div style="text-align: center;">
    <h1>Daftar Isi</h1>
    <h3>
        <ul style="list-style-type: none; padding: 0; color: black;">
            <li><a style="color:black;">Pendahuluan</a></li>
            <li><a href="#Apengertian-halftoning" style="color:black;">Pengertian Halftoning</a></li>
            <li><a href="#11-halftoning-patterning" style="color:black;">Halftoning: Patterning</a></li>
            <li><a href="#12-halftoning-dithering" style="color:black;">Halftoning: Dithering</a></li>
        </ul>
    </h3>
</div>


<h1 style="text-align: center;"> Pendahuluan </h1>

Halftoning merupakan teknik penting dalam dunia cetak dan grafis digital yang digunakan untuk menciptakan ilusi gradasi warna dengan menggunakan palet warna terbatas, seperti hitam dan putih. Dalam banyak aplikasi, terutama dalam pencetakan, halftoning memungkinkan representasi gambar yang kompleks dengan tingkat detail yang lebih tinggi meskipun hanya menggunakan titik-titik warna yang berbeda ukuran atau intensitasnya. Teknik ini sangat krusial dalam mengatasi keterbatasan media cetak yang tidak dapat menampilkan spektrum warna penuh.

Dalam halftoning, terdapat dua metode utama yang sering digunakan: Patterning dan Dithering. Keduanya memiliki prinsip kerja yang berbeda, tetapi keduanya bertujuan untuk menghasilkan gambar yang tampak halus meskipun hanya menggunakan warna yang terbatas.

Patterning melibatkan penyusunan titik-titik dalam pola yang teratur, di mana ukuran dan kepadatan titik mencerminkan kecerahan gambar asli. Di sisi lain, dithering menggunakan pendekatan yang lebih acak dan mengandalkan distribusi kesalahan untuk menghasilkan transisi warna yang lebih halus dan realistis.

Kedua teknik ini memiliki aplikasi yang luas, mulai dari pencetakan tradisional hingga pengolahan gambar digital, dan masing-masing memiliki kelebihan serta kekurangan yang membuatnya sesuai untuk konteks tertentu. Dengan memahami prinsip dasar halftoning, kita dapat lebih menghargai bagaimana teknik ini mempengaruhi cara kita melihat dan berinteraksi dengan gambar dalam berbagai media.

Dalam kajian ini, kita akan mendalami lebih jauh tentang kedua metode halftoning tersebut, mulai dari cara kerja, implementasi, hingga perbandingan efektivitasnya dalam berbagai konteks penggunaan.




# A. Pengertian Halftoning

Halftoning adalah sebuah teknik yang digunakan dalam dunia cetak dan grafis digital untuk mensimulasikan rentang warna (grayscale) dengan menggunakan jumlah warna yang terbatas, seperti hitam dan putih. Hal ini sangat umum digunakan dalam proses cetak untuk menghasilkan gambar yang terlihat memiliki warna gradasi meskipun hanya menggunakan titik-titik warna yang berbeda ukuran atau intensitasnya.

*Terdapat dua teknik utama dalam halftoning:*
1. Patterning (pola)
2. Dithering (pengacakan)

##	1.1. Halftoning: Patterning

Patterning adalah metode halftoning di mana titik-titik disusun dalam pola atau kisi (grid) yang sistematis untuk mensimulasikan gradasi warna. Pola-pola ini dibuat dengan mengubah ukuran atau jarak antar titik, yang secara visual memberikan ilusi kecerahan yang berbeda. Ukuran titik lebih besar menunjukkan warna yang lebih gelap, sedangkan titik yang lebih kecil menandakan warna yang lebih terang.

* Cara Kerja:
    * Gambar dibagi menjadi grid atau sel, dan setiap sel diberikan pola titik tetap. Pola ini biasanya terdiri dari titik-titik hitam yang disusun dalam bentuk tertentu. Semakin gelap area gambar, semakin banyak titik dalam pola tersebut.
    * Setiap blok piksel pada gambar asli diubah menjadi pola titik hitam dan putih yang ukurannya tetap, tetapi kepadatannya berubah berdasarkan intensitas kecerahan piksel asli.

* Ciri Utama:
  * Titik-titik disusun dalam pola yang teratur (biasanya dalam bentuk persegi atau lingkaran).
  * Pola titik selalu memiliki ukuran yang sama, hanya jumlah atau distribusi titik yang berubah untuk merepresentasikan kecerahan.

* Kelebihan:
  * Mudah diimplementasikan.
  * Hasil cetakan cenderung bersih dan konsisten.

* Kekurangan:
  Kadang-kadang menghasilkan pola yang terlalu terlihat jelas (seperti "moiré") dan tidak halus ketika dilihat dari dekat.

* Contoh Penggunaan:

    Patterning sering digunakan dalam teknik cetak yang lebih sederhana dan terbatas dalam resolusi. Ini dapat dilihat dalam beberapa teknik pencetakan layar (screen printing) atau media cetak tradisional.

* Perhitungan sederhana
  * Konversi ke Grayscale
    
    Jika gambar awalnya berwarna, ubah gambar tersebut menjadi grayscale. Namun, dalam contoh ini, gambar sudah dalam format grayscale.

  * Gambar Sederhana (5x5 Piksel)
    
    * 200 200 200 100 100
    * 200 200 200 100 100
    * 150 150 150 80 80
    * 150 150 150 80 80
    * 100 100 100 50 50

  * Pembagian Gambar Menjadi Blok
    Bagilah gambar menjadi blok-blok kecil. Untuk kemudahan, kita akan menggunakan blok 2x2 piksel:

    Blok 1:
     * 200 200
     * 200 200
    
    Blok 2:
     * 100 100
     * 100 100

    Blok 3:
     * 150 150
     * 150 150

    Blok 4:
     * 80 80
     * 80 80

    Blok 5:
    * 100 100
    * 50  50

* Hitung Rata-rata Kecerahan
  
  Hitung rata-rata intensitas kecerahan untuk setiap blok:

    Blok 1:
    
    Rata-rata = (200 + 200 + 200 + 200) / 4 = 200
   
    Blok 2:
    
    Rata-rata = (100 + 100 + 100 + 100) / 4 = 100

    Blok 3:
    
    Rata-rata = (150 + 150 + 150 + 150) / 4 = 150

    Blok 4:
    
    Rata-rata = (80 + 80 + 80 + 80) / 4 = 80


    Blok 5:
    
    Rata-rata = (100 + 100 + 50 + 50) / 4 = 75

* Pilih Pola Titik Berdasarkan Rata-rata Intensitas
  
  Tentukan pola titik untuk setiap blok berdasarkan kecerahan rata-rata. Misalnya, kita bisa menggunakan pola berikut:

   * Intensitas 200 (Putih):
        * Pola Titik Putih (Kosong):

                  □ □
                  □ □
   * Intensitas 100 (Abu-Abu Gelap):
        * Pola Titik Sedang:

                  ■ □
                  □ ■
   * Intensitas 150 (Abu-Abu Sedang):
        * Pola Titik Menengah:

                 ■ □
                 ■ □
   *Intensitas 80 (Abu-Abu Gelap):
        * Pola Titik Hampir Penuh:

                ■ ■
                ■ ■
    
* Gabungan akhir


      □ □ □ ■ □
      □ □ □ ■ □
      ■ □ ■ □ □
      ■ □ ■ □ □
      ■ ■ ■ □ □
     
*Pseoducode*

Input: Grayscale image G dengan ukuran NxM piksel

Output: Gambar halftoning H dengan pola titik

1. Tentukan ukuran blok BxB (misal: 2x2 atau 3x3)
2. Buat tabel pola titik (dot patterns) berdasarkan tingkat intensitas

   Misal:
     - Pola kosong untuk intensitas tinggi (hampir putih)
     - Pola sebagian untuk intensitas sedang
     - Pola penuh untuk intensitas rendah (hampir hitam)

3. Untuk setiap blok dalam gambar G:
   a. Ambil piksel-piksel dalam blok berukuran BxB
   b. Hitung rata-rata intensitas blok tersebut
   c. Pilih pola titik berdasarkan rata-rata intensitas
   d. Gantikan blok tersebut dengan pola titik yang sesuai di gambar H

4. Kembalikan gambar H

End

*Contoh Pseducode*
   
    Input: G (grayscale image 6x6)
    Output: H (halftoned image)

    Step 1: Tentukan ukuran blok B = 2x2

    Step 2: Tentukan tabel pola titik:
      - Intensitas tinggi (200-255) → Pola: □ □ □ □
      - Intensitas sedang (100-199) → Pola: ■ □ □ □
      - Intensitas rendah (0-99) → Pola: ■ ■ □ □

    Step 3: Proses setiap blok:

    For i from 1 to 6 step 2:  # Untuk setiap baris dengan loncatan 2 piksel
      For j from 1 to 6 step 2:  # Untuk setiap kolom dengan loncatan 2 piksel
        Block = G[i:i+1, j:j+1]  # Ambil blok 2x2 dari gambar G
        Avg_intensity = Rata-rata nilai piksel dalam blok
        Pola = Pilih pola titik berdasarkan Avg_intensity
        Gantikan blok G[i:i+1, j:j+1] dengan Pola di gambar H

    Step 4: Output H

**Kode Program**

	pkg load image; % Memastikan paket image terinstal

	function halftone_patterning(input_image, output_image)
		% Membaca gambar
		img = imread("orang.tif");

		% Mengubah gambar menjadi grayscale
		if size(img, 3) == 3
			img = rgb2gray(img);
		end

		% Mendapatkan ukuran gambar
		[rows, cols] = size(img);

		% Membuat gambar kosong untuk output
		halftoned_img = zeros(rows, cols);

		% Thresholding (menggunakan pola 4x4 untuk halftoning)
		dither_matrix = [
			0  8  2 10;
			12  4 14  6;
			3 11  1  9;
			15  7 13  5
		];

		% Mengubah ukuran dither matrix sesuai dengan ukuran gambar
		[dither_rows, dither_cols] = size(dither_matrix);

		% Looping untuk setiap piksel
		for i = 1:rows
			for j = 1:cols
				% Mengambil nilai intensitas piksel
				pixel_value = img(i, j);

				% Menentukan threshold berdasarkan dither_matrix
				threshold = (dither_matrix(mod(i-1, dither_rows)+1, mod(j-1, dither_cols)+1) / 16) * 255;

				% Mengubah piksel berdasarkan threshold
				if pixel_value > threshold
					halftoned_img(i, j) = 255; % Putih
				else
					halftoned_img(i, j) = 0;   % Hitam
				end
			end
		end

		% Menyimpan gambar halftoned
		imwrite(uint8(halftoned_img), output_image);

		% Menampilkan gambar asli dan hasil halftoning
		figure;
		subplot(1, 2, 1), imshow(img), title('Gambar Asli');
		subplot(1, 2, 2), imshow(halftoned_img), title('Gambar Halftoned');
	end
	% Memanggil fungsi dengan nama file input dan output
	halftone_patterning('input_image.jpg', 'output_halftoned.jpg');


**Outputnya**
![alt text](<Screen Shot 2024-09-25 at 18.14.21.png>)

**Langkah-langkah:**
* Gambar dipecah menjadi kisi-kisi (grid) kecil.
* Pada setiap kotak grid, jumlah titik hitam ditentukan berdasarkan tingkat kecerahan dari bagian gambar tersebut. Semakin terang area gambar, semakin sedikit atau semakin kecil titik yang digunakan.
* Pola atau distribusi titik biasanya diulang dan teratur.

**Contoh:**
Misalkan kita memiliki gambar dengan gradasi dari putih ke hitam. Pada area yang lebih terang, titik yang digunakan lebih sedikit atau kecil. Di sisi lain, pada area yang lebih gelap, titik-titik menjadi lebih besar atau lebih padat. Pola ini berulang dalam blok-blok kecil yang dapat berupa lingkaran, bujur sangkar, atau bentuk lainnya.

**Metode Patterning:**
* AM (Amplitude Modulation): Metode di mana ukuran titik berubah sesuai dengan intensitas kecerahan, sementara posisi titik tetap berada di lokasi grid yang tetap.

**Output**
Hasil dari patterning adalah gambar yang tampak lebih terstruktur dan memiliki pola yang jelas. Efek visual lebih terlihat teratur dan sering digunakan dalam cetakan dengan resolusi rendah.

## 	1.2. Halftoning: Dithering

Teknik lain yang digunakan untuk menghasilkan gambar halftoning digital adalah dithering. Berbeda dengan patterning, dithering menciptakan gambar keluaran dengan jumlah titik yang sama dengan jumlah piksel pada gambar sumber. Dithering dapat dianggap sebagai penapisan (thresholding) gambar sumber dengan matriks dither. Matriks tersebut diletakkan berulang kali di atas gambar sumber. Di mana pun nilai piksel gambar lebih besar dari nilai dalam matriks, sebuah titik pada gambar keluaran akan diisi. Masalah yang terkenal dari dithering adalah bahwa ia menghasilkan artefak pola yang diperkenalkan oleh matriks ambang tetap. Gambar 4.5 menunjukkan contoh operasi dithering.

![alt text](<Screen Shot 2024-09-25 at 14.11.13.png>)

**Penjelasan**

Gambar pertama menunjukkan gambar input dalam bentuk matriks piksel dengan nilai intensitas grayscale (misalnya 12, 51, 34, 121, dst.). Nilai intensitas ini berada pada rentang 0 (hitam) hingga 255 (putih).

Di tengah, terdapat "repeated dither matrix" atau matriks threshold yang diulang. Ini adalah matriks nilai-nilai threshold yang digunakan untuk mengubah gambar input menjadi gambar biner (hitam-putih). Nilai pada matriks ini diulang secara periodik pada gambar yang lebih besar. Matriks dither memiliki nilai seperti 0, 60, 45, 110, yang akan dibandingkan dengan nilai piksel input.

Pada proses dithering setiap piksel dari gambar input dibandingkan dengan nilai threshold pada posisi yang sesuai di matriks dither.
Jika nilai intensitas piksel input lebih besar dari nilai pada matriks threshold, maka hasil output adalah 1 (putih), dan jika lebih kecil, hasil output adalah 0 (hitam).

**contoh perhitungannya:**
* Piksel (1,1) di input image memiliki nilai 12.
* Piksel (1,1) di repeated dither matrix memiliki nilai 0.
* Karena 12 > 0, piksel (1,1) pada output image menjadi 1 (putih).

Dan pada gambar ketiga, hasil akhir adalah gambar hitam-putih (biner) yang terbentuk dari hasil komparasi antara nilai piksel pada input image dan nilai threshold pada repeated dither matrix. Setiap piksel akan bernilai 1 (putih) jika nilainya lebih besar dari threshold, atau 0 (hitam) jika lebih kecil atau sama dengan threshold.

**Berikut adalah langkah-langkah untuk melakukan halftoning dithering pada sebuah gambar grayscale:**
1. **Persiapan Gambar Grayscale**
   - **Input**: Ambil gambar grayscale (misalnya dengan resolusi 8-bit, dengan nilai pixel antara 0 hingga 255).
   - **Output**: Gambar hanya terdiri dari skala abu-abu yang nantinya akan diubah menjadi hitam-putih.

2. **Buat Tabel Threshold (Ambang Batas)**
   - Buat tabel threshold sesuai dengan ukuran sel halftone yang diinginkan (misalnya 3x3 atau 4x4).
   - Contoh tabel threshold untuk sel halftone 3x3:
     ```
     6 8 4
     1 9 2
     7 3 5
     ```
   - Nilai di dalam tabel menentukan urutan munculnya titik hitam dalam satu sel halftone. Tabel ini dapat bervariasi tergantung kebutuhan.
  
3. **Pilih Ukuran Sel Halftone**
   - Misalnya, pilih ukuran sel halftone 3x3 (untuk setiap 9 piksel).
   - Setiap sel halftone berisi beberapa piksel yang akan dirender berdasarkan nilai grayscale aslinya.

4. **Iterasi Melalui Gambar**
   - Iterasi gambar dalam blok-blok sebesar sel halftone (misalnya 3x3 piksel).
   - Misalnya, untuk gambar 100x100 piksel dan ukuran sel halftone 3x3, bagi gambar menjadi blok 3x3 piksel.

5. **Bandingkan Setiap Nilai Piksel dengan Tabel Threshold**
   - Untuk setiap blok 3x3:
     1. **Ambil Nilai Grayscale Piksel**: Misalnya, nilai grayscale piksel = 150.
     2. **Bandingkan dengan Tabel Threshold**: Bandingkan nilai grayscale piksel tersebut dengan nilai threshold pada posisi yang sama dalam tabel threshold.
     3. **Putuskan Warna Piksel**:
        - Jika nilai grayscale lebih besar atau sama dengan nilai threshold, ubah piksel menjadi **putih** (nilai 255).
        - Jika lebih kecil, ubah piksel menjadi **hitam** (nilai 0).

#### Contoh
Misalkan nilai grayscale sebuah blok 3x3 piksel adalah:
```
120 140 180
220 200 190
170 160 150
```
Dan tabel threshold-nya adalah:
```
6 8 4
1 9 2
7 3 5
```
Bandingkan nilai grayscale masing-masing piksel dengan nilai threshold di posisi yang sama:

- Piksel [0,0] (120) lebih besar dari threshold [6] → Putih (255)
- Piksel [0,1] (140) lebih kecil dari threshold [8] → Hitam (0)
- Piksel [0,2] (180) lebih besar dari threshold [4] → Putih (255)
  
Lakukan ini untuk seluruh blok dan ubah pikselnya.

6. **Render Gambar**
   - Setelah seluruh piksel dalam blok-blok halftone telah diproses, gabungkan kembali blok-blok tersebut untuk menghasilkan gambar akhir.
   - Gambar hasilnya akan menjadi hitam-putih, tetapi karena pola titik yang tersebar (halftone), masih dapat memberikan kesan adanya gradasi.

7. **Tinjau dan Sesuaikan Hasil**
   - Setelah gambar selesai diproses, Anda dapat melihat apakah distribusi titik sesuai dengan harapan. 
   - Jika hasil kurang memuaskan, Anda bisa menyesuaikan ukuran sel atau nilai threshold pada tabel.

Ini adalah langkah-langkah umum untuk melakukan halftoning dithering. 

**Algoritma Dithering:**
Ada beberapa algoritma yang sering digunakan dalam dithering, di antaranya:

1. **Ordered Dithering:**
      * Teknik ini menggunakan matriks threshold yang diulang di seluruh gambar. Piksel gambar dibandingkan dengan nilai dalam matriks threshold tersebut untuk menentukan apakah akan menjadi hitam atau putih.
      * Output dari algoritma ini adalah gambar dengan pola berulang kecil yang menghasilkan gradasi warna dengan baik.
	**Langkah-langkah**
	  * Buat matriks threshold kecil, misalnya 4x4.
	  * Setiap piksel gambar dibandingkan dengan nilai dalam matriks threshold.
	  * Jika nilai piksel lebih tinggi dari threshold, piksel tersebut menjadi putih, jika lebih rendah menjadi hitam.
	  **Contoh:** Untuk gambar grayscale dengan nilai 0 hingga 255, matriks threshold 4x4 dapat berupa:
	  [ 0, 128, 32, 160 ]
	  [ 192, 64, 224, 96 ]
	  [ 48, 176, 16, 144 ]
      [ 240, 112, 208, 80 ]
2. **Floyd-Steinberg Dithering:**
   * Teknik ini menggunakan kesalahan (error) distribusi untuk menyebarkan kesalahan kuantisasi ke piksel tetangga, sehingga transisi antara warna menjadi lebih halus.
	**Langkah-langkah:**
	* Untuk setiap piksel, hitung kesalahan antara nilai piksel asli dan nilai yang dikuantisasi (hitam atau putih).
	* Bagikan kesalahan ini ke piksel tetangga, mengikuti pola distribusi yang telah ditentukan, misalnya:
		X   7
	   3  5  1
	* X adalah piksel saat ini, dan kesalahan dibagikan ke tetangga di kanan, bawah, dan bawah kanan berdasarkan berat distribusi (7/16, 5/16, 3/16, dan 1/16).

	**Contoh:** Jika sebuah piksel memiliki nilai grayscale 180, dan dikuantisasi menjadi putih (nilai 255), maka kesalahan sebesar -75 (255 - 180) dibagikan ke piksel tetangga sesuai dengan distribusi Floyd-Steinberg.

**Kode Program**
	
	pkg load image; % Memastikan paket image terinstal

	function halftone_dithering(input_image, output_image)
		% Membaca gambar
		img = imread("orang.tif");

		% Mengubah gambar menjadi grayscale
		if size(img, 3) == 3
			img = rgb2gray(img);
		end

		% Mendapatkan ukuran gambar
		[rows, cols] = size(img);

		% Membuat gambar kosong untuk output
		halftoned_img = zeros(rows, cols);

		% Menggunakan threshold (0-255)
		for i = 1:rows
			for j = 1:cols
				% Mengambil nilai intensitas piksel
				pixel_value = img(i, j);

				% Menentukan nilai biner (hitam atau putih)
				if pixel_value > 127
					halftoned_img(i, j) = 255; % Putih
					error = pixel_value - 255;  % Hitung error
				else
					halftoned_img(i, j) = 0;   % Hitam
					error = pixel_value;        % Hitung error
				end

				% Sebarkan error ke tetangga (Floyd-Steinberg)
				if j < cols
					img(i, j + 1) = img(i, j + 1) + error * 7 / 16; % Piksel kanan
				end
				if i < rows && j > 1
					img(i + 1, j - 1) = img(i + 1, j - 1) + error * 3 / 16; % Piksel bawah kiri
				end
				if i < rows
					img(i + 1, j) = img(i + 1, j) + error * 5 / 16; % Piksel bawah
				end
				if i < rows && j < cols
					img(i + 1, j + 1) = img(i + 1, j + 1) + error * 1 / 16; % Piksel bawah kanan
				end
			end
		end

		% Menyimpan gambar halftoned
		imwrite(uint8(halftoned_img), output_image);

		% Menampilkan gambar asli dan hasil dithering
		figure;
		subplot(1, 2, 1), imshow(img), title('Gambar Asli');
		subplot(1, 2, 2), imshow(halftoned_img), title('Gambar Dithering');
	end

	% Memanggil fungsi dengan nama file input dan output
	halftone_dithering('input_image.jpg', 'output_dithering.jpg');


**Output**
![alt text](<Screen Shot 2024-09-25 at 18.22.04.png>)

**Cara Perhitungan Halftoning Dithering**
1. Tentukan Resolusi Gambar:
   * Tentukan ukuran gambar yang akan di-dithering (misalnya 100x100 piksel).

2. Pilih Ukuran Cluster atau Sel Halftone:
   * Biasanya, satu sel halftone terdiri dari sekumpulan piksel (misalnya, 4x4 atau 8x8 piksel) yang digunakan untuk mewakili satu area grayscale.

3. Hitung Nilai Grayscale Setiap Piksel:
   * Setiap piksel pada gambar asli memiliki nilai grayscale (misalnya dari 0 hingga 255 dalam sistem 8-bit). Nilai ini menentukan seberapa "terang" atau "gelap" suatu piksel.

4. Pola Dot Matrix:
   * Buat atau pilih pola dot halftone. Dalam pola ini, semakin besar area berwarna hitam dalam sebuah cluster piksel, semakin gelap area yang terwakili.
   * Misalnya, untuk area yang sangat terang, hanya satu atau dua titik hitam digunakan di dalam satu sel halftone. Sedangkan untuk area yang lebih gelap, lebih banyak titik hitam di dalam cluster.
  
5. Bandingkan Nilai Grayscale dengan Threshold (Ambang Batas):
   * Gunakan tabel threshold atau ambang batas untuk menentukan jumlah titik hitam dalam setiap sel berdasarkan nilai grayscale.
   * Tabel threshold ini bisa berbentuk grid yang sesuai dengan ukuran sel halftone. Nilai-nilai di dalam tabel threshold akan dibandingkan dengan nilai grayscale dari gambar asli untuk menentukan piksel mana yang akan dijadikan hitam dan mana yang akan dijadikan putih.
   Contoh tabel threshold 3x3:
   	6 8 4
   	1 9 2
   	7 3 5

6. Konversi ke Hitam-Putih:
   * Untuk setiap piksel di dalam sel halftone, bandingkan nilai grayscale dengan nilai threshold di posisi yang sama di dalam tabel. Jika nilai grayscale lebih besar dari nilai threshold, piksel tersebut menjadi putih. Jika lebih kecil, piksel tersebut menjadi hitam.
   Misalnya, jika nilai grayscale suatu piksel adalah 130, dan threshold-nya adalah 128, maka piksel tersebut akan diwarnai putih.

**Contoh Penerapan Halftoning Dithering**
Jika Anda memiliki gambar grayscale dengan nilai 150 dan sel halftone 3x3 seperti tabel threshold di atas:

1. Ambil nilai grayscale piksel (misal 150) dan bandingkan dengan tabel threshold.
2. Gambar piksel yang melebihi nilai 150 menjadi putih, dan sisanya menjadi hitam.
**Algoritma:**
* Loop setiap piksel gambar.
* Untuk setiap blok 3x3:
  * Bandingkan nilai setiap piksel dengan ambang batas di sel.
  * Jika piksel lebih besar dari threshold, biarkan putih; jika lebih kecil, jadikan hitam.

**Perbandingan Patterning dan Dithering:**
* Patterning, Menghasilkan pola teratur dan struktural, cocok untuk cetakan dengan resolusi rendah atau efek artistik yang disengaja.
* Dithering, Menghasilkan pola acak yang lebih halus, memberikan hasil yang lebih realistis untuk gradasi warna, sering digunakan dalam pencetakan dengan resolusi tinggi atau untuk tampilan digital.
**Contoh Penggunaan:**
* Patterning sering digunakan dalam proses cetak tradisional seperti surat kabar atau gambar dengan resolusi rendah.
* Dithering sering digunakan dalam kompresi gambar digital, pengolahan gambar di perangkat seperti monitor atau printer, serta dalam seni piksel.

# Daftar Pustaka

1. *Lau, Daniel Leo*. Modern digital halftoning. Arbor: UMI Company, 1999.

2. *Eran Steinberg, Robert J. Rolleston, Roger L. Easton Jr.*, "Analysis of random dithering patterns using second-order statistics," Journal of Electronic Imaging, vol. 1,Issue 4,1992. DOI:https://doi.org/10.1117/12.60717
   
3. *https://youtu.be/5lVjAXBFa-s?si=5by5621SMPpkxs0B*