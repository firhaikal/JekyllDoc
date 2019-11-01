---
layout: page
title: Send Data to Firebase
permalink: /send/
---

# _Send Data_ to Firebase

<center><img src="{{site.baseurl}}/assets/img/pemanis.jpeg"></center>

### Langkah - langkahnya :

**1.** Kita harus mempunyai _project_ android studio terlebih dahulu

**2.** Lalu buka _project_ tersebut

**3.** Lalu pada _tool windows bar_ , klik **_Tools_** lalu klik **firebase** , seperti ini


<img src="{{site.baseurl}}/assets/img/firebase.png">

**4.** Lalu akan muncul kotak firebase seperti ini,

<img src="{{site.baseurl}}/assets/img/klikSave.jpeg">

**5.** Lalu klik **_Realtime Database_**, maka akan muncul kotak seperti ini

<img src="{{site.baseurl}}/assets/img/klikSave.jpeg">

**6.** Lalu klik **_Save and retrieve data_**, maka akan tampil kotak seperti ini

<img src="{{site.baseurl}}/assets/img/kotakFirebase1.jpeg">

**7.** Lalu klik **_Connect to Firebase_**, maka akan muncul kotak seperti ini

<img src="{{site.baseurl}}/assets/img/createFirebase.jpeg">

**8.** Pada kotak tersebut pastikan anda sudah **_sign in_**

**9.** Pilih **_Create new Firebase Project_** , lalu beri nama project firebase tersebut dan jangan lupa pilih daerah atau negara kalian

**10.** Lalu klik _button_ **_Connect to Firebase_** yang berwarna biru

**11.** Lalu selanjutnya klik **_Add the Realtime Database to your App_** , maka akan muncul kotak seperti ini

<img src="{{site.baseurl}}/assets/img/konfigAPP.jpeg">

**12.** Lalu klik **_Accept Changes_** yang berwarna biru pada kotak tersebut

**13.** Jika berhasil , maka semuanya akan terceklis hijau seperti ini

<img src="{{site.baseurl}}/assets/img/berhasilRealtime.jpeg">

**14.** Lalu pada kodingan di android studio tambahkan **Class Data Barcode**, yang diisi oleh data-data dari barcode seperti ini

<img src="{{site.baseurl}}/assets/img/classBarcode.png">

**15.** Lalu buatlah method untuk menyimpan data tersebut ke firebase seperti ini

<img src="{{site.baseurl}}/assets/img/method.png">

**16.** Lalu simpan atau panggil method tersebut ditempat yang seharusnya seperti ini

<img src="{{site.baseurl}}/assets/img/simpanMethod.png">

**17.** Jangan lupa untuk menginisialisasikan firebasenya seperti ini

<img src="{{site.baseurl}}/assets/img/inisialisasi.png">

**18.** Lalu masuk ke web firebase menggunakan akun yang dipakai untuk membuat project firebase

**19.** Lalu klik button **_Get Started_** , maka akan muncul nama project firebase tadi seperti ini

<img src="{{site.baseurl}}/assets/img/projectFirebase.jpeg">

**20.** Lalu klik nama project firebase tadi

**21.** Lalu buat **_Realtime Database_** seperti ini

<img src="{{site.baseurl}}/assets/img/createRealtime.jpeg">

**22.** Lalu pilih **_Start in locked mode_** seperti ini

foto true false
<img src="{{site.baseurl}}/assets/img/chooseRules.jpeg">

**23.** Lalu klik button **enable** yang berwarna biru

**24.** Lalu klik **_Database_** pada kotak biru disebelah kiri seperti ini

<img src="{{site.baseurl}}/assets/img/sidebar.jpeg">

**25.** Lalu klik **Rules** pada kotak putih seperti ini

<img src="{{site.baseurl}}/assets/img/Rfalse.jpeg">

**26.** Lalu ubah **_read_** dan **_write_** menjadi true 

**27.** Lalu klik **_Publish_** seperti ini

<img src="{{site.baseurl}}/assets/img/publish.jpeg">

**28.** Lalu klik **_dismiss_** seperti ini

<img src="{{site.baseurl}}/assets/img/dismiss.jpeg">

**29.** Lalu run project android studio tersebut

**30.** Lalu cek data tersebut di web firebase seperti ini

<img src="{{site.baseurl}}/assets/img/data.png">
