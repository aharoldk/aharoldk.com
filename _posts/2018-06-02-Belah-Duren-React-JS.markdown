---
layout: post
title: Belah Duren React JS
categories: Software Development
date: 2018-06-02T00:00:00.000Z
---
<img src="{{ site.baseurl }}/images/fulls/7.png" class="fit image">
Halo teman-teman, pada topik hari ini saya ingin membelah duren React JS. hahaha. Maksudnya adalah bedah code dari React JS. btw udah install React JS kan? klo belum ayo ke link ini dulu <a href="https://reactjs.org/docs/add-react-to-a-new-app.html">Click Me</a>. Klo sudah mari saya jelaskan setetes tentang React JS.

<img src="{{ site.baseurl }}/images/fulls/reactjs/1.png" class="fit image">
Gambar diatas merupakan isi dari file index.js dimana dilakukan import ReactDOM sehingga ReactDom dapat digunakan.
ReactDOM.render(<App />, document.getElementById('root')) berfungsi untuk merender component App yang sudah di import diatas ke dalam document yang berelement 'root'.

<img src="{{ site.baseurl }}/images/fulls/reactjs/2.png" class="fit image">
Ini merupakan code dari App tadi yang bisa di import di Index.js. Dicode ini ditampilkan class yang menggunakan ES6 class, gimana menurut teman-teman sangat mudah dibacakan class ini? hahaha.
Kita menggunakan bahasa html dalam js, ini karena didukung dari JSX. JSX merupakan ekstensi sintaks javascript yang terlihat mirip seperti XML. Menarik bukan?
<br>
Di code App.js ini kita menampilkan tampilan Header dan Body sehingga hasil tampilannya seperti ini.
<img src="{{ site.baseurl }}/images/fulls/reactjs/6.png" class="fit image">
<br>
Di artikel sebelumnya <a href="http://aharoldk.com/software/development/2018/05/27/React-JS-Sebagai-Penyambung-Hidup-Yang-Baru/" target="_blank">Click Me</a>, saya pernah membahas tentang kenapa harus menggunakan React JS. Salah satu point yang saya mau bahas adalah Menggunakan konsep Component untuk memecah kode menjadi lebih kecil dan bisa digunakan berkali-kali. Oleh karena itu saya mau memecah contoh kode diatas.
<br>
<br>
<img src="{{ site.baseurl }}/images/fulls/reactjs/4.png" class="fit image">
Pada gambar diatas, saya membuat file baru dengan nama Header.js kemudian memindahkah code <Header>...</Header> kedalam return Header.js.
<br>
<br>
<img src="{{ site.baseurl }}/images/fulls/reactjs/3.png" class="fit image">
Selanjutnya saya juga membuat file baru dengan nama Body.js dan memindahkan code <p>...</p> kedalam return Body.js
<br>
<br>
<img src="{{ site.baseurl }}/images/fulls/reactjs/5.png" class="fit image">
Pada App.js saya import component Header.js dan Body.js dan mengunakan Component itu di dalam <div>...</div> dengan cara menambahkan <Header /> dan <Body />. Apabila kamu mau menggunakan component Header atau Body pada file lain sisa dilakukan import dan voala....

untuk contoh applikasi ini, anda bisa langsung melihat disini <a href="https://github.com/aharoldk/ReactJs-Blog">Github</a>

Apabila ada pertanyaan atau konten menarik yang ingin dibahas, silahkan di email ya. 