# NodeJS, Sunucuyu Ayağa Kaldırma
***NodeJS*** server tarafında çalışan *JavaScript* runtime platformudur. Tarayıcıdan bir URL alabilmek ve sunucunun sunduğu varlığı görmek için yani NodeJS ile server ayağa kaldırmak için iki modülden yararlanabiliriz:  
> * HTTP modül (Express kullanmadan)  
> * Express modül  
***NPM***, JavaScript modüllerini içinde barındıran paket yönetim sistemidir.

## HTTP Modül  
Bu modül, NodeJSle yerleşik bir modüldür. Sunucu oluşturmak ve bağlantıları kurarak sunucuyu ayağa kaldırmak için kullanılır. Bu bağlantılar sayesinde veri alım ve iletim gerçekleştirilebilir. Kod örneği aşağıdaki gibidir.  
*Not:* 3000 portuna gönderdiğimiz için, çıktıyı localhost:3000'de kontrol edebiliriz.  

<p align="center"> <img width=600  src ="https://github.com/A101-Node-js-TypeScript-Bootcamp/a101-bootcamp-odev1-berceou/blob/main/serveup-nodejs/img/built-http-server.png"> </p> 



## Express Modül  
***Express*** sayesinde hızlı ve kolay bir şekilde web sunucuları oluşturabiliriz. Yani, statik bir web sitesi sunmak için de karmaşık bir *HTTP JSON tabanlı API* oluşturmak için de rahatça kullanılabilir.
Express sadece modül değil aynı zamanda bir frameworktür. API, sub-modüller ve fonksiyonlar gibi birçok imkan tanır.  
>* Öncelikle *Package JSON* oluşturmalıyız. Aşağıdaki komut yardıymıyla *package.json* için ayrı alanları doldurabiliriz (proje adı, açıklaması, vb.).  
*Not:* Her soru için varsayılan değeri kullanmak için sadece 'evet' yanıtını verecek olan -Y bayrağını kullanabiliriz.  

```
npm init  
```  

>* Package.json dosyasını elde ettikten sonra serve-up öncesi Express installation yapılması gerekir.  

```
nmp install express  
```  
Tüm işlemler tamamlandıktan sonra üzerinde çalışacağımız *app.js* dosyasını oluşturmalıyız. Kod örnekleri aşağıdaki gibidir.  

<p align="center"> <img width=600 sec="https://github.com/A101-Node-js-TypeScript-Bootcamp/a101-bootcamp-odev1-berceou/blob/main/serveup-nodejs/img/built-server-express.png"> </p>

> Öncelikle, express kütüphanesini yüklemek için yeni bir constant oluşturdum. Ve grab almak için de **require** kullandım.  
> Daha sonra, uygulamayı saklamak için yeni bir constant oluşturdum. Bu sayede Express fonksiyonu bir argüman almak yerine uygulamaya sağlanan metotları kullanarak sunucuyu yapılandırmış oluyorum. Artık uygulamaya ne yapması gerektiğini atayabiliriz.  
> Fonksiyon iki önemli argümanla çağırılır:
> * Sunucuya gelen request bilgisini içeren obje = ***req***
> * İstekte bulunana geri gönderilen cevap = ***res***
> * ```res.send()``` kod satırının amacı istekte bulunana bir şey göndermektir. Yani eğer browser talebinde bulunursak, çıktıyı bu şekilde görebiliriz.
> * Sunucu hala çalışır modda değil. Henüz tarayıcıda görüntüleyemiyoruz.  ``` .listen() ``` metotu ile sunucuyu başlatıp belirli bir bağlantı noktasında dinlemesini sağlarız.  
 ***NOT:*** Benim de kullandığım *port 3000* ortak geliştirme portudur. Varsayılan (default) bir port değildir.  





