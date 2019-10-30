---
title: Install Jekyll
permalink: /install-jekyll/
---
# Install Jekyll
Jekyll merupakan [Ruby Gem](https://jekyllrb.com/docs/ruby-101/#gems) yang bisa diinstall di hampir semua sistem

## Kebutuhan
* [Ruby](https://www.ruby-lang.org/en/downloads/) dengan versi 2.4.0 atau lebih(versi ruby bisa dicek dengan menjalankan `ruby -v`)
* [RubyGems](https://rubygems.org/pages/download)(yang bisa dicek dengan menjalankan `gem -v`)

Ruby bisa diinstal di Website [Ruby](https://rubyinstaller.org/downloads/)
## Petunjuk
### Windows
Cara termudah menjalankan Jekyll adalah dengan menggunakan RubyInstaller
1. Download dan Install Ruby+Devkit dari [RubyInstaller Downloads](https://rubyinstaller.org/downloads/). gunakan installer yang sesuai
2. Jalankan installer tersebut lalu setelah terinstall buka CommandPrompt
   dan jalankan command berikut untuk menginstall Jekyll dan Bundler:

            gem install jekyll bundler

3. Cek jika Jekyll sudah terinstall dengan benar `jekyll -v`
Setelah itu Jekyll pun bisa digunakan

## Membuat projek Jekyll baru
1. Buka CommandPrompt lalu tujukan cmd ke lokasi dimana anda akan membuat folder projek, misal:
   
            cd D:/JekyllProject

2. Lalu jalankan `jekyll new projekku`
   dimana `projekku` adalah nama dari projeknya
3. setelah projek dibuat buka folder projeknya di cmd
   
            cd projekku

4. untuk membuka projeknya jalankan command

            jekyll serve

    lalu buka link yang diberikan

Untuk mengubah isi judul dan sejenisnya, terdapat di `config.yml`,
dan bila akan menambahkan post, buat file markdown dengan format nama seperti `TAHUN-BULAN-HARI-JUDULPOST.MARKDOWN` dan simpan didalam
folder `_post`.

Isi dari file markdown biasanya seperti ini:

            ---
            layout: post
            title: judul
            ---
            //Isi konten