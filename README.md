# [nafidurmus.github.io](http://nafidurmus.github.io/about)

# Burası nasıl yapıldı ?

1.) Githubda kullanıcı_adı.github.io adında bir repo oluşturalım.

2.) Kullandığımız işletim sisteminde ruby kurulu olmalı.Debian tabanlı bir sisteme kurulum;

2.1) Sistemi güncelleyelim.
```bash
$ sudo apt-get update
```
2.2) Rvm yüklerken kullanacak olduğumuz curl indirelim.
```bash
$ sudo apt-get install curl
```
2.3) Rvm kullanarak ruby indirelim.
```bash
$ \curl -L https://get.rvm.io | bash -s stable --ruby
```
2.4) Ruby yi yüklediğimize emin olmak için aşağıdaki kodu çalıştıralım.
```bash
$ ruby -v
```
Aşağıdakine benzer bir çıktı almanız gerekli.
![picture](/images/jekyll-blog/ruby-version.png)

3.) Jekly gem ini bilgisayarımıza indirelim.
3.1) Aşağıdaki komutu kullanarak indirebilirsiniz. 
```bash
$ gem install jekyll
```

4.) Blogumuzun iskeletini oluşturmak için aşağıdaki komutu girelim.
```bash
$ jekyll new user_blog
```
5.) Oluşturduğumuz iskelet dizinine aşağıdaki komutla girelim.
```bash
$ cd user_blog
```
5.1) Aşağıdaki kodu kullararak kodumuzu localde çalıştırabiliriz.
```bash
$ jekyll serve
```
6.) Gelelim oluşturduğumuz iskeleti githuba göndermeye.

6.1)İsterseniz aşağıdaki yazımdan faydalanarak bu işlemleri gerçekleştirebilirsiniz.
- [Githuba 8 adımda git ile proje nasıl yüklenir ?](https://medium.com/@nafidurmus/githuba-8-ad%C4%B1m-da-git-ile-proje-nas%C4%B1l-y%C3%BCklenir-5a7f7f8aeaf3)

6.2)Okumak istemezseni sırasıyla aşağıdaki komutları kullarak githuba push edebilirsiniz.

6.2.1) [Bu siteden](https://git-scm.com/download/) kendinize uygun git versiyonunu indiriniz.

6.2.2) Aşağıdaki kodları kullanarak git terminalinde yapılandırma işlemini gerçekleştiriniz.
```bash
$ git config --global user.name "example"
$ git config --global user.email "email@example.com"
```
6.2.3) Projenizi oluşturduğunuz dizinde aşağıdaki kodu kullanarak yerel bir repo oluşturunuz.
```bash
$ git init
```
6.2.4) Projenize ilk commit işlemini aşağıdaki gibi yapınız.
```bash
$ git commit -m "jekyll kullanarak blog oluşturma"
```
6.2.5) 1. adımda oluşturmuş olduğunuz sayfanın bilgilerini giriniz.
```bash
$ git remote add origin https://github.com/github-kullanıcı-adınız/kullanıcı_adı.github.io.git
```
6.2.6) Son olarak aşağıdaki komutla projenizi githuba gönderelim.
```bash
$ git push -u origin master
```
7.) Jekyll ile blog projenizi başarılı bir şekilde gönderdiyseniz kullanıcı_adı.github.io sayfasından aşağıdaki çıktıyı almanız gerekli.
![picture](/images/jekyll-blog/basarili-yukleme.png)

8.) Aşağıdaki bilgileri değiştirmek için  `_config.yml` i değiştirebilirsiniz.
![picture](/images/jekyll-blog/bilgiler.png)

9.) Kendinize hakkında sayfası oluşturma için.
9.1) Bulunduğunuz dizinde `about.md` gibi `md` uzantlı bir dosya oluşturunuz.
9.2) Aşağıdaki kodlar bulunmalıdır.
```bash
---
layout: page
title: hakkında
permalink: /about/
---
```
9.2.1) Geri kalan kısmını istediğiniz gibi doldurabilirsiniz.
```bash
---
layout: page
title: post
permalink: /about/
---
> Merhabalar ben Jenkll ile blog yapımı hakkında yazı yazıyorum.
```
9.2.2) Yukarıdaki kod yazıldığı takdide hakkında yazısı sağ üst köşededir.
![picture](/images/jekyll-blog/hakkinda.png)

9.2.3) Sayfanın içeriği aşağıdaki gibidir.
![picture](/images/jekyll-blog/hakkinda-icerik.png)

10.) Yazmak istediğiniz yazıları `_posts` dizinini içine yazmalısınız.

10.1) Yazazağınız yazının ismi **yıl - ay - gün - sayfanızım urlde gözükecek ismi** olmalı.Buraya yazdığınız olduğu gibi urlde görülecektir.
10.2) Yazınızın başlangıcı aşağıdaki gibi olamalıdır.
```bash
---
layout: post
title:  "Jekyll kullanarak 20 dakikada blog yapımı "
date:   2018-05-13 24:45:43 +0300
categories: jekyll blog
---
```

10.3) Bu yazıyı yukarıdaki maddeleri uygulayarak yazdım.
