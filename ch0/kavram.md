0-A. Derlediğin programı neden a.out diye değil de ./a.out diye çalıştırıyorsun? Kabuk, bir komutu
aradığı yerlerde mevcut dizine neden bakmaz?

- Programın adını dizin belirtmeden verirsek Shell programı $PATH içinde arayacaktır. Mevcut dizin PATH de yer almadığından
program bulunamayacaktır. Mevcut dizinin PATH de yer almamasının sebebi güvenlikle ilgilidir. Eğer ortak bir dizinde çalışıyorsak
ve başka biri dizine 'ls' adında bir kötü amaçlı program yerleştirdiyse biz ls komutunu çalıştırmak isterken Shell sonradan yerleştirilen
programı çalıştıracaktır. Bu sebeple mevcut dizin PATH de tutulmaz.

0-B. ./prog < in.txt > out.txt komutunda program dosyaların adını biliyor mu? Okuma ve yazma
işlerini kim ayarlıyor?

- ./prog dosyaların adını bilmez. Okuma ve yazma işlerini programın çalıştığı Shell ayarlar. Program her zamanki gibi
Standart girişten veri okuduğunu ve standart çıkıştan veri gönderdiğini zanneder. Bu akışların arka planda hangi dosyalara
bağlı olduğunu bilmez.

0-C. kc kısayolundaki -fsanitize=address,undefined neyi yakalar? Kitaptaki programlar için bu
neden faydalı?

- Bellek hatalarını ve tanımsız davranışları yakalar. Sessiz hataları anında yakaladığı için öğrenim sürecinde faydalıdır.

0-D. Derlenmiş çalıştırılabilir dosyalar neden repoya eklenmez?

- Git gibi versiyon kontrol araçları binary dosyalar için tasarlanmamıştır.