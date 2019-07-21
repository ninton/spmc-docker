# scanned-pdf-margin-cutter on Ubuntu16.04 (developing)

## 必要なもの

+ docker
+ docker-compose

## 使い方

    表紙.pdf を spmc-docker/pdf/a.pdf へコピーしてください。
    本体.pdf を spmc-docker/pdf/b.pdf へコピーしてください。

    $ cd spmc-docker
    $ sudo docker-compose build
    $ sudo docker-compose up -d
    $ sudo docker exec -it spmc.docker bash

    root# cd /tmp
    root# spmc-main-prompt
    表紙pdf(ないときはENTER):a.pdf
    本文pdf:b.pdf
    左綴じ(Yes|no)[Yes]:
    上余白(mm)[0]:14
    右余白(mm)[0]:10
    幅(mm):155
    高さ(mm):233
    表示pdf   : a.pdf
    本体df    : b.pdf
    左綴じ    : 1
    上余白(mm): 14
    右余白(mm): 10
    幅(mm)    : 155
    高さ(mm)  : 233
    OK(yes/no)[yes]

    $ sudo docker-compose down

    spmc-docker/pdf/output.pdf が、完成pdfです。
