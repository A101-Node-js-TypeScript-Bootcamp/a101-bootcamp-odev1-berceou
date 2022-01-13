# TypeScript ve JavaScript Arasındaki Farklar  
</br>  

*TypeScript* (TS) strongly-typed (data tiplerinin kesinliği), nesne yönelimli (object-oriented) ve derlenebilir (compilable) açık kaynaklı (open-source) bir programlama dilidir. JavaScript (JS) dilinin tüm özelliklerini barındırırken ek özellikler de içeren bir üst kümesi olarak tanımlanabilir. Daha büyük ve komplex projelerde verimliliği artırır. TypeScript dilinde yazılan kodlar derlernirken JavaScript dilindeki karşılığına dönüştürülür. Çıktı olarak JS kodu verir ve JS kodunu çalıştırır.  
> ***Bir üst kümedeki TypeScript:*** JavaScript kodu, bir TypeScript kodudur denilebilir. Öte yandan, bir TypeScript kodu derlenip çalıştırılmadığı sürece bir JavaScript kodu değildir. Bu sebeple TypeScript olarak yazılan tüm kodların JavaScript çıktısı, bütün JavaScript frameworklerini (çatılarını), araçlarını (tools) ve kütüphanelerini (libraries) kullanabilir.  
> ***Nesne yönelimli TypeScript:***
Sınıflar, arayüzler, modüller, inheritance gibi özellikleri destekler. JavaScript'te bir sınıf oluşturmak için bir işlev oluşturulmalıdır. Kalıtım için prototipler kullanılır. TypeScript sınıf tabanlıdır, bu nedenle kalıtım, kapsülleme ve değiştiriciyi nesne yönelimli bir programlama dili olarak destekleyebilir.  

*JavaScript*, interpreted (yorumlamalı) bir dildir, derleme aşamasına ihtiyaç yoktur. Bu nedenle kod çalışana dek hata tespiti yapılamaz. Hata varsa bile tüm kodun gözden geçirilmesi gerekir bu durum da zaman ve efor kaybı yaratabilir. **TypeScript**, bu noktada derleme aşamasında hata denetimi sağladığı için bu soruna çözüm getirmiş olur. 
JavaScript dilinde statik veri tiplemesi yoktur, veri tipleri dinamik olarak yürütme aşamasında belirlenir.
Form doğrulama, bir web sayfasına çeşitli özellikler eklemek gibi işlevler için JavaScript daha kullanışlıdır.  
 </br>  

## Uygulamalı Farklar  

#### Değişken Tanımlaması:  

> *JavaScript*  
```  
let numbers = 123456
let strings = "lpsum";
const numberArray = [1, 2];
const stringArray = ["lorem", "ipsum"];
let isBoolean = false;
const anObject = {
  property1: 1,
  property2: "lipsum"
};  
```  

> *TypeScript*  
```  
let numbers: number = 123456 ;
let strings: string = "lpsum";
let numberArray: number[] = [1, 2];
let stringArray: string[] = ["lorem", "ipsum"];
let isBoolean: boolean = false;
let anObject: object = {
  property1: 1,
  property2: "lipsum"
};  
```  
> * TS ile tanımlanan değişkenler aynı zamanda tip ataması da aldılar.  
> ***Not:*** Değişken tipleri ne olursa olsun *null* ve ya *undefined* alabilirler.
</br>  

> *TypeScript* **interface**, **class**, **extends**, **implements**, **modules** özellikleri:  

*Interface* ile kullanıcı için özellikler atamak: 
```  
interface UserInterface{
  firstName: string;
  lastName: string;
  phone: number;
}  
```    
> *Interface* yapılar birbirlerinden **extend** olabilir, ama **implement** olamazlar. Değişkenlere ve classlara atanabilirler.
  
*class*  
``` 
class User implements UserInterface{
	firstName: string;
	lastName: string;
	phone: number;

    constructor(
        firstName: string;
        lastName: string;
        phone: number;
    ){
        this.firstName = firstName;
        this.lastName = lastName;
        this.phone = phone;
    }
}  
```  
> JavaScript dilinde class yapılarını simüle etmeye çalışırız. TypeScript dilinde class mantığını kullanabiliriz. Burada "User" class oluşturup özellik atamalarını tamamladık.  

</br>  

##### Özetle, JS ve TS arasındaki farkları uygulamalı bir şekilde ilk hafta derslerini de baz alarak anlatmaya çalıştım. İçerik bu özelliklerle ve kıyaslamalarla kısıtlı değildir.  






