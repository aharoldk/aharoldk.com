---
layout: post
title: Part#2 Belah Duren React JS
categories: Software Development
date: 2018-06-03T00:00:00.000Z
---
<img src="{{ site.baseurl }}/images/fulls/7.png" class="fit image">
Halo teman-teman, pada topik hari ini saya ingin membelah duren React JS. hahaha. Maksudnya adalah bedah code dari React JS. btw udah install React JS kan? klo belum ayo ke link ini dulu <a href="https://reactjs.org/docs/add-react-to-a-new-app.html">Click Me</a>. Klo sudah mari saya jelaskan setetes tentang React JS.
<br/>
<br/>
Pada artikel sebelumnya, kita sudah belajar bagaimana untuk memecah Component App.js ke beberapa Component. Pada artikel ini, kita akan membuat form dan menampilkan data yang telah diinput. Okey? Sudah siap?

<img src="{{ site.baseurl }}/images/fulls/reactjs/part2/1.png" class="fit image">
Buat file baru dengan nama DetailMantan. Code diatas itu untuk menampilkan list dari mantan yang sudah kita input dimana menampilkan nama dan umur mantan kita dengan cara menangkap <u><strong>this.props.nama</strong></u> dan <u><strong>this.props.umur</strong></u>.

<img src="{{ site.baseurl }}/images/fulls/reactjs/part2/2.png" class="fit image">
Kemudian kita buat file baru dengan nama ListMantan untuk menampung data yang dikirim dari App.js. Coba lihat <strong><u>this.props.list.map(lists => ...)</u></strong> itu merupakan fungsi perulangan dimana tiap index dari list itu akan mengirim data ke DetailMantan untuk dicetak. <i>(Jangan Lupa Import DetailMantan ya supaya bisa digunakan tag DetailMantan dan bisa liat mantan-mantan kamu hahaha)</i>

<img src="{{ site.baseurl }}/images/fulls/reactjs/part2/3.png" class="fit image">
Ganti code pada Body.js seperti diatas dimana menampilkan form yang memiliki input nama mantan,umur mantan, dan input yang bertipe submit. Selanjutnya tambahkan onSubmit dan arahakan pada fungsi getSubmit untuk mengarahkan ketika melakukan submit. Ketika pada getSubmit, saya menggunakan preventDefault() untuk tidak merefresh page, menangkap value dari form yang sudah kita berikan nama pada form, dan mengirimkan value pada fungsi saveStateMantan yang berada pada App.js.
<br>
<br>
<img src="{{ site.baseurl }}/images/fulls/reactjs/part2/4.png" class="fit image">
Kemudian pada App.js, saya membuat <u><strong>constructor(props){ ... }</strong></u> dimana menampung data state <i>(next tutorial saya akan menjelaskan tentang state dan props)</i>. Kemudian saya initialisasikan state sebagai object dimana menampung name, title, dan daftar. <br>
Setelah itu saya buat fungsi untuk menangkap dan menambahkan data ke dalam state. <i>this.setState({...})</i> digunakan untuk menset state kita dengan data yang baru. Next pada render(), saya memberikan value kepada Header dan ListMantan dan memberikan fungsi kepada Body.
<br>
<br>
<img src="{{ site.baseurl }}/images/fulls/reactjs/part2/5.png" class="fit image">
Dan yang terakhir rubah sedikit pada Header.js dimana kita menampilkan name dan title.
<br>
<br>
<img src="{{ site.baseurl }}/images/fulls/reactjs/part2/6.png" class="fit image">
TADAAAAAAAAAAAAAAAAAAAAAAAAAAAAA. Berikut tampilannya teman-teman. <br>
Gimana teman-teman? Apakah memusingkan? atau buat Pingsan? hahaha. <br>
Untuk contoh applikasi ini, anda bisa langsung melihat disini <a href="https://github.com/aharoldk/ReactJs-Blog">Github</a>

Apabila ada pertanyaan atau konten menarik yang ingin dibahas, silahkan di email ya. 