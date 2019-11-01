---
layout: page
title: Menampilkan Data dari Firebase ke website
permalink: /ftw/
---

# Menampilkan Data dari Firebase ke website

<center><img src="{{site.baseurl}}/assets/img/firelog.png"></center>

<br/>&nbsp; &nbsp; &nbsp; Setelah mengambil dan mengirim data ke Firebase selanjutnya kita akan menampilkan Data dari Firebase ke Website milik kita.<br/>

<br/>&nbsp; &nbsp; &nbsp; Berikut Langkah langkah yang perlu kita lakukan :

## A. Mendaftarkan Website kita ke Database Firebase

1. Add Website ke Firebase.

	<br/>&nbsp; &nbsp; &nbsp; Untuk mendaftarkan Web kita ke Firebase kita perlu Login ke Akun Firebase dan kemudian membuka Konsol dari Database Fire base kita
	lalu klik tombol "Add App" yang ada di layar <br/>

	<center><img src="{{site.baseurl}}/assets/img/AddApp.png"></center>

2. Pilih Jenis Aplikasi.

	Setelah Itu, pilih jenis Aplikasi kita, karena kita ingin menampilkan data di Website maka pilih Web. <br/>

	<center><img src="{{site.baseurl}}/assets/img/PilihWeb.png"></center>

3. Memasukan Nama Aplikasi.

	<br/>&nbsp; &nbsp; &nbsp; Selanjutnya kita diminta untuk memasukan Nama Aplikasi kita <br/>

	<center><img src="{{site.baseurl}}/assets/img/RegisWeb.png"></center>

4. Salin Konfigurasi.

<br/>&nbsp; &nbsp; &nbsp; dan nanti akan muncul File Konfigurasi yang akan kita simpan di
kodingan Laman Web yang digunakan. <br/>

<center><img src="{{site.baseurl}}/assets/img/ConfigDBWeb.png"></center>

**Alternative**

1. Melihat Project Settings.

	<br/>&nbsp; &nbsp; &nbsp; Apabila kita sudah pernah mendaftarkan Aplikasi tapi lupa belum menyimpan Konfigurasi Firebasenya ke Web maka Klik Icon Roda Gigi di samping "Project Overview" dan pilih "Project Setting". <br/>

	<center><img src="{{site.baseurl}}/assets/img/altSeeConfig.png"></center>

2. Konfigurasi Database.

	Nanti kita akan tiba di laman setting dan di bagian bawahnya akan ada Konfigurasi Database kita <br/>

	<center><img src="{{site.baseurl}}/assets/img/altConf.png"></center>

## B. Setup file HTML + JS :
1. Buat file HTML biasa + (buat tabel untuk menampung data).

2. Mengimpor file-file yang diperlukan. Simpan setelah tag <body>.
	>	<script src="https://www.gstatic.com/firebasejs/7.2.2/firebase.js"></script>
    >	<script defer src="/__/firebase/7.2.2/firebase-auth.js"></script>
    >	<script src="/__/firebase/7.2.2/firebase-firestore.js"></script>

3. Buat tag `<script>` untuk menampung kode JavaScript yang akan kita buat.
	>	<script type="text/javascript"></script>

4. Inisialisasi Firebase dengan cara memasukkan identitas dari project Firebase masing-masing.
	>	var config = {
	>		apiKey: "YOURAPIKEY",
	>		authDomain: "YOURDOMAIN",
	>		databaseURL: "YOURURL",
	>		projectId: "YOURPROJECTID",
	>		storageBucket: "YOURSTORAGEBUCKET",
	>		messagingSenderId: "YOURSENDERID"
	>	};
	>	firebase.initializeApp(config);

5. Buat Referensi dari Database Firebase kalian.
	>	var dbRef = firebase.database();
	> 	var statusAlat = dbRef.ref("reference-name");

6. Dapatkan referensi tabel-nya.
	>	var table = document.getElementById("reference-table").getElementsByTagName('tbody')[0];

7. Memuat Data dari Firebase.
	>	statusAlat.on("child_added", function(data, prevChildKey) {
	>		var newstatusAlat = data.val();
	>	
	>		// Menghitung jumlah baris yang ada di Database masing-masing
	>		var row = table.insertRow(table.rows.length);
	>	
	>		// Buat cell sesuai jumlah kolom pada realtime database masing-masing
	>		var cell1 = row.insertCell(0);
	>		var cell2 = row.insertCell(1);
	>		var cell3 = row.insertCell(2);
	>		var cell4 = row.insertCell(3);
	>	
	>		cell1.innerHTML = newstatusAlat.nama_alat;
	>		cell2.innerHTML = newstatusAlat.status_alat;
	>		cell3.innerHTML = newstatusAlat.tanggal_alat;
	>		cell4.innerHTML = newstatusAlat.jam_alat;
	>	});

