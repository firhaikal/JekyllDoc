---
layout: page
title: Mengambil data dari QR Code
permalink: /ambildataqr/
---
# **Mengambil data dari QR Code**
Dalam tiap QR Code terdapat data yang tersimpan, walaupun hanya terdiri dari karakter - karakter,
dengan memindai suatu QR Code kita dapat mengambil data yang tersimpan itu lalu kita bisa menggunakan datanya.

Dengan mengenerate QR Code dari [Mashtips QR Generator](https://mashtips.com/qr-code-for-contact-list/),
lalu kita hanya perlu untuk mengisi data yang ada didalam tabel

![qr](/assets/img/contact-qr-generator.jpg)

lalu QR Codenya akan mengenerate otomatis, QR Code ini yang akan kita pakai untuk dipindai
dan mengambil datanya.

Dalam project QR Code scanner kita tambahkan library [ez-vcard](https://github.com/mangstadt/ez-vcard)

    compile 'com.googlecode.ez-vcard:ez-vcard:0.10.5'

lalu Graddle sync projectnya, buka class dimana method **handleResult** berada,
dan tambahkan variable seperti berikut:

    String emailV, telNum, Nama;

Walaupun dalam QR Code generator kita mengisi 4 data, dikarenakan data Nama depan dan Nama belakang akan digabung,
jadi kita hanya perlu mengambil 3 data.

Dalam method **handleResult** kita menambahkan code untuk mengambil result scannya

    VCard vCard = Ezvcard.parse(rawResult.getText()).first();
                    for (Email email : vCard.getEmails()){
                        emailV = email.getValue();
                        for (Telephone tel : vCard.getTelephoneNumbers()){
                            telNum = tel.getText();
                            Nama = vCard.getStructuredName().getFamily();
                        }
                    }

Disana kita gunakan library **ez-vcard** untuk mengambil datanya dimana data yang terambil berbentuk string, namun data tersebut masih menyatu,
jadi kita gunakan librarynya, library ini akan memisahkan datanya, seperti data **Nama**, mengambil Structure yang sudah menjadi Fullname,
lalu variabel string email dan telepon akan menyimpan data yang diambil dari variable Email dan Telephone.

Maka datanya sudah diambil dan bisa digunakan untuk keperluan selanjutnya.