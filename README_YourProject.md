# YMT5270 Ara Sınav Projesi: Orange ile Veri Analizi ve Makine Öğrenmesi

## Öğrenci Bilgileri
- **Ad Soyad**: Muhammed Efe DEVECİ
- **Öğrenci Numarası**: 241137130
- **E-posta**: 241137130@firat.edu.tr

## Proje Özeti
Bu projede, kalp hastalığı teşhisini veri madenciliği ve makine öğrenmesi yöntemleriyle analiz etmek amacıyla Kaggle üzerinden temin edilen bir veri seti kullanılmıştır. Veri seti; yaş, cinsiyet, kolesterol, kan basıncı, göğüs ağrısı tipi gibi bireysel sağlık bilgilerine ek olarak bireylerin kalp hastalığı durumu (var/yok) bilgilerini içermektedir.

Proje kapsamında öncelikle keşifsel veri analizi (EDA) gerçekleştirilmiş, özniteliklerin dağılımları incelenmiş ve aykırı değerler görselleştirilmiştir. Box Plot, Distributions ve Correlations bileşenleriyle veri hakkında ön bilgi edinilmiştir. Ardından, kNN, SVM, Random Forest, Logistic Regression ve Naive Bayes gibi sınıflandırma algoritmaları uygulanarak modeller eğitilmiş ve Test and Score bileşeni ile değerlendirilmiştir.

Modellerin başarıları; doğruluk, F1 skoru, ROC-AUC gibi metriklerle ölçülmüş, sonuçlar Confusion Matrix ve ROC Curve ile görselleştirilmiştir.



## Veri Seti
### Veri Seti Bilgileri
- **Veri Seti Adı**: 
- **Kaynak**: *(URL veya referans)*
- **Lisans**: *(Eğer belirtilmişse)*
- **Veri Seti Boyutu**: *(örn. 500 satır, 10 sütun)*

### Veri Seti Tanımı
> *Veri setinin içeriğini detaylı olarak açıklayınız. Hangi öznitelikleri içerdiği, verilerin nasıl toplandığı, olası sınırlılıkları gibi bilgileri buraya yazınız.*

### Öznitelik Açıklamaları
| Öznitelik Adı | Veri Tipi | Açıklama | Örnek Değer |
|---------------|-----------|----------|-------------|
| Örnek Öznitelik 1 | Sayısal | İlgili açıklama | 42.5 |
| Örnek Öznitelik 2 | Kategorik | İlgili açıklama | "Evet" |
| ... | ... | ... | ... |

## Keşifsel Veri Analizi (Explanatory Data Analysis - EDA)
### Temel İstatistikler
> *Veri setine ait temel istatistikleri (ortalama, medyan, standart sapma, vb.) buraya ekleyiniz. Orange'dan alınan ekran görüntüleri ile destekleyebilirsiniz.*

### Veri Ön İşleme
Olası eksiklikleri tespit etmek amacıyla Impute bileşeni kullanılmıştır. Bu bileşen, eksik değer olması durumunda sayısal veriler için ortalama, kategorik veriler için en sık değerle doldurma işlemi gerçekleştirecek şekilde yapılandırılmıştır.

Dağılım analizleri Distributions, Box Plot ve Scatter Plot bileşenleri ile görselleştirilmiştir.

Orange arayüzünde doğrudan normalize bileşeni kullanılmamıştır. Ancak SVM ve kNN gibi algoritmaların içinde yer alan ön işlem seçenekleri aracılığıyla normalizasyon işlemleri modellerin içsel olarak uygulanmasını sağlamıştır.

Continuize bileşeni aracılığıyla kategorik değişkenler otomatik olarak sayısal formata dönüştürülmüştür. Bu dönüşüm sayesinde algoritmaların sayısal işlem yapabilmesi mümkün olmuştur.

Son olarak, Select Columns bileşeni kullanılarak hedef değişken (HeartDisease) açıkça tanımlanmış, model eğitimi için gerekli öznitelikler belirlenmiştir. Bu sayede makine öğrenmesi algoritmalarının doğru şekilde eğitilmesi sağlanmıştır.

### Görselleştirmeler
> *Orange ile yaptığınız veri görselleştirmelerini buraya ekleyiniz. Her görselleştirme için kısa bir açıklama yazınız. Görselleri bu repoya yükleyip, markdown içinde referans verebilirsiniz.*

#### Görselleştirme 1: [Görselleştirme Adı]
![Görselleştirme 1 Açıklaması](goruntuler/gorselleştirme1.png)
> *Bu görselleştirme ile ilgili yorumunuz ve çıkarımlarınız.*

#### Görselleştirme 2: [Görselleştirme Adı]
![Görselleştirme 2 Açıklaması](goruntuler/gorselleştirme2.png)
> *Bu görselleştirme ile ilgili yorumunuz ve çıkarımlarınız.*

### Öznitelik İlişkileri
> *Öznitelikler arasındaki ilişkileri analiz ediniz. Korelasyon matrisi, scatter plot matrisi gibi görsellerle destekleyiniz.*

## Makine Öğrenmesi Uygulaması
### Kullanılan Yöntem
> *Veri setinize uyguladığınız makine öğrenmesi yöntemini (sınıflandırma, regresyon veya kümeleme) belirtiniz ve neden bu yöntemi seçtiğinizi açıklayınız.*

### Modeller ve Parametreler
> *Denediğiniz modelleri ve kullandığınız parametreleri açıklayınız. Orange'da yapılandırdığınız widget ayarlarını ekran görüntüleri ile destekleyebilirsiniz.*

### Model Değerlendirmesi
> *Uyguladığınız modelin performansını değerlendiriniz. Kullandığınız değerlendirme metriklerini açıklayınız.*

#### Metrikler
| Metrik | Değer |
|--------|-------|
| Örnek Metrik 1 | 0.85 |
| Örnek Metrik 2 | 0.78 |
| ... | ... |

### Sonuçların Yorumlanması
> *Elde ettiğiniz sonuçları detaylı bir şekilde yorumlayınız. Modelin güçlü ve zayıf yönleri nelerdir? Başka hangi modeller denenebilirdi?*

## Orange İş Akışı
> *Orange ile oluşturduğunuz iş akışı görselini buraya ekleyiniz. İş akışınızın adımlarını kısaca açıklayınız.*

![Orange İş Akışı](goruntuler/is_akisi.png)

## Sonuç ve Öneriler
> *Projenizin genel bir değerlendirmesini yapınız. Elde ettiğiniz sonuçlar hakkında çıkarımlarınızı ve gelecek çalışmalar için önerilerinizi yazınız.*

## Kaynaklar
> *Proje boyunca yararlandığınız kaynakları (makaleler, web siteleri, videolar, vb.) buraya ekleyiniz.*

1. Kaynak 1
2. Kaynak 2
3. ...

## Ekler
### Orange Proje Dosyası
> *Orange proje dosyanızı (.ows) bu repoya yükleyiniz ve buradan referans veriniz.*
> 
> [Proje_Dosyasi.ows](proje_dosyasi.ows)

### Veri Seti Dosyası veya Bağlantısı
> *Kullandığınız veri setini bu repoya yükleyebilir veya bağlantısını burada paylaşabilirsiniz.*
>
> [Veri_Seti.csv](veri_seti.csv) veya [Veri Seti Bağlantısı](https://ornek-veri-seti-baglantisi.com)
