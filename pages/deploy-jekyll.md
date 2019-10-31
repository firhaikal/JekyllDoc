---
title: Deploy Projek
permalink: /deploy/
---
# Deploy Projek
## Install Surge
Pertama-tama install surge terlebih dahulu dengan menjalankan
command ini di CommandPrompt

        npm install -g surge

lalu arahkan CommandPrompt ke lokasi projek dan build projeknya

        jekyll build

Sekarang source code anda sudah diolah didalam folder **_site/**,
**_site/** ini akan dibuild ulang tiap anda menjalankan command `jekyll build`
dan didalamnya terdapat file - file yang ditujukan untuk dipublish ke web.

## Mendeploy situs Jekyll
untuk mempublish folder **_site/** ke web, jalankan command berikut:

        surge _site/

Maka di CommandPrompt anda akan ditujukan untuk login atau signup bila
anda belum melakukannya, lalu anda akan diberikan subdomain. Anda bisa mengubahnya dengan sesuai yang anda mau, seperti **example-jekyll.surge.sh**:

![assets/img/deploy.gif](/assets/img/deploy.gif)