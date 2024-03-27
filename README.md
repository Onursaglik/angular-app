# Yapılanlar

JSON Server'ı kullanarak basit bir Restful API'ye sahip olan ve bu API'yi JSON dosyası üzerinden yönetebileceğim bir sunucu oluşturdum.
Database oluşturmak için json-server kullandım (touch indir: npm install touch-cli -g , dosya oluştur: touch db.json , sunucu oluştur: json-server --watch db.json).
db.json'a verileri koyduktan sonra sunucum hazır hale geldi:
jsonAnasayfa.png , jsonSayfaData.png , jsonData.png


interface ile model yapıp(model.png) async bir şekilde verileri fetch'ledim{service.png(10)(14)}

Router kullanarak sayfaların path'lerini oluşturdum(routes.png)
Sitenin iskeletini oluştururken app.component.ts'ye HomeComponent'i importlayıp router-outlet ile html'ini gösterdim{appModule.png(8)(17)}
Daha sonra anlatacağım details sayfasından geri çıkarken sürekli sayfayı geri döndürmekten sıkıldığım için başlıktaki "homes" fotoğrafını anasayfaya bağladım{appModule.png(12)}.

anasayfa.png'deki evleri listeleyebilmek için evlerin verilerini alıp{anasayfaEvler(21)} template'ini oluşturdum{anasayfaEvler(9)}. Fotoğrafta her ne kadar typescript üzerine yazmış 
olsam da html kodunu, bunu daha az fotoğraf koymak ve anlaşılabilirliği kolaylaştırmak için yaptım yoksa .html'e yazıp templateUrl: './example.component.html', olarak da yapılabilir.

Anasayfayı artık tamamlamak için bir arama filtresi koydum{ansayfaKod(14)} ve şehre göre filtreledim{ansayfaKod(35)}. anasayfaEvler.png'de yaptığım evleri sıralaması için ngFor kullandım.

Detay sayfasını oluşturup @angular/forms kullanarak evlere başvurabilecekleri bir form oluşturdum. Her bir ev için id'lerine göre pathler ayarladım{detay2.png(50)}
web sitesi üzerinden f12>terminal kısmına girersek submit butonuna basıldığında verinin alındığını da görebiliriz service.png(18) detaySayfa.png.

Hepsine ek olarak tabiki de css ve html kodları nasıl yazılır nasıl birbirleri arasında iletişim kurarlar üzerinde çalışarak öğrendim.



Takıldığım kısımlar: Arama barında sadece butona basarak değil, klavyeden enter'a basarak da aramasını istedim. Bastığımda sayfanın aramayı anlık yaptığını ama sonuç olarak sayfayı tekrar
tamamını yüklediğini debug yaparak fark ettim. Bir kaç saat açıkçası bununla uğraştım. Arama bölümünü anlık olarak aratması için "submit"'e çevirip arama bölümüne yazdığım sürece
alt kısımda filtrelemesini sağladım ancak bu sefer de search butonunun gereksiz olacağını fark ettiğim için yapmadım. Ama güzel bir özellik olarak gördüm diyebilirim.




## AngularApp

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 17.2.2.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The application will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory.

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI Overview and Command Reference](https://angular.io/cli) page.
