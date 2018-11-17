---
layout: post
title: Apache Kafka Consumer with Spring Boot
categories: Software Development
date: 2018-11-17T00:00:00.000Z
---
<img src="{{ site.baseurl }}/images/fulls/8.png" class="fit image">
Halo teman-teman, sekarang saya akan menjelaskan sedikit tentang <b>Apache kafka Consumer</b> dengan <b>Spring Boot</b>.
Saya harap teman-teman udah mengerti tentang apa itu <b>Apache Kafka</b> dan familiar dengan <b>Spring Boot</b>. <a href="https://kafka.apache.org/">Klik disini untuk belajar Apache Kafka</a>

Awalnya pergi ke <a href="https://start.spring.io/">Spring Initializr</a> untuk generate project spring dan pilih depedency yang akan digunakan, disini saya memilih depedency <u>Kafka</u>.
<img src="{{ site.baseurl }}/images/fulls/kafka-consumer/1.png" class="fit image">


Setelah itu buka project dan buka file <i>application.properties</i>.
- <i>server.port</i> menentukan port <b>Spring Boot</b> yang akan digunakan.
- <i>spring.kafka.bootstrap-servers</i> menentukan server dari kafka.
- <i>spring.kafka.consumer.group-id</i> menentukan consumer group dari kafka.

<img src="{{ site.baseurl }}/images/fulls/kafka-consumer/2.png" class="fit image">

Kemudian buat file <i>KafkaConsumerConfig</i> dimana kita melakukan configurasi dari kafka.
<img src="{{ site.baseurl }}/images/fulls/kafka-consumer/3.png" class="fit image">

Selanjutnya create file <i>KafkaConsumer</i> dan create method <i>kafkaListener</i> dengan menggunakan anotasi <i>@KafkaListener</i>. Di <i>@KafkaListener</i> bisa diset seperti <i>errorHandler</i>, <i>topicPartitions</i>, dll.
<img src="{{ site.baseurl }}/images/fulls/kafka-consumer/4.png" class="fit image">

Mungkin ada pertanyaan dari teman-teman, bagaimana apabila <i>message</i>/data yang diolah itu error dan tidak ingin dicommit. Teman-teman bisa menambahkan  <i>enable_auto_commit_config</i> pada configurasi <i>consumerFactory</i> dan <i>factory.getContainerProperties().setAckMode(AckMode.MANUAL_IMMEDIATE)</i> pada kafkaListenerContainerFactory.
<img src="{{ site.baseurl }}/images/fulls/kafka-consumer/5.png" class="fit image">


Dan menambahkan parameter <i>Acknowledgment</i> pada method dan eksekusi method <i>acknowledge()</i>.
<img src="{{ site.baseurl }}/images/fulls/kafka-consumer/6.png" class="fit image">


Lalu test-nya seperti apa? Apakah sulit? Santai yang kita harus lakukan adalah mengetes methodnya seperti contoh dibawah.
<img src="{{ site.baseurl }}/images/fulls/kafka-consumer/7.png" class="fit image">

Gimana teman-teman? Apakah memusingkan? atau buat Pingsan? hahaha. <br>
Untuk contoh applikasi ini, anda bisa langsung melihat disini <a href="https://github.com/aharoldk/simple-kafka-consumer">Github</a>

Apabila ada pertanyaan atau konten menarik yang ingin dibahas, silahkan di email ya. 