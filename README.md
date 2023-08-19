# Forecasting-API-Orders-Number
The challenge of Forecasting Daily order quantities / Statsmodels/ Sarımax

Our aim was to find a solution to the challenge of forecasting daily order quantities. Our dataset includes daily order counts from May 2, 2020, to June 30, 2022. Additionally, we collected temperature and marketing expenditure data.
Our task was to run the model every Monday morning and obtain predictions for the upcoming period. We specify the number of days we want to forecast, and our model provides order predictions for those days. It's important to note that the temperature column values represent real data and are only available for current and past days. On the other hand, marketing expenditure, being a feature that can be known in advance, is accessible at prediction time. Furthermore, we're not only interested in point predictions but also in the uncertainty of those predictions. Before deploying this model, we need to evaluate its performance, hence we kindly request information about the out-of-sample performance.
Considering that our future colleagues will evaluate this task, we have taken care to structure our work meticulously. Our code is clean, well-commented, and easy to follow, with explanatory comments where necessary. Our report has been prepared to reflect our thought process in detail, explaining our reasoning comprehensively.
In the final stages, we've exposed the model through an API endpoint. This endpoint can return forecasts for a specified date range or provide forecasts for a desired prediction horizon. We trigger the 'predictions' function by providing the desired number of forecasted days. This function utilizes our model to predict order quantities starting from the given date.
This project not only showcases our technical skills but also demonstrates our ability to provide a consistent and well-explained solution, ready for evaluation by our future colleagues.

İhtiyacımız olan şey, günlük sipariş sayısını tahmin etme konusundaki sorunumuza çözüm bulmaktı. Veri setimiz, 2 Mayıs 2020'den 30 Haziran 2022'ye kadar olan günlük sipariş sayılarını içeriyor. Ayrıca, sıcaklık ve pazarlama harcaması verilerini de topladık.
"Görevimiz, her Pazartesi sabahı modeli çalıştırmak ve gelecek tahminlerimizi elde etmek oldu. Tahmin etmek istediğimiz gün sayısını belirtiyoruz ve modelimiz bu günler için sipariş tahminlerini sunuyor.". Sıcaklık sütunundaki değerlerin gerçek değerler olduğunu ve sadece mevcut ve geçmiş günler için mevcut olduğunu unutmamız önemlidir. Öte yandan, pazarlama harcaması önceden bilinebilen bir özellik olduğu için tahminleme anında erişilebilir durumdadır.Ayrıca, sadece nokta tahminlerine değil, tahminlerin belirsizliğine de ilgi duyuyoruz. Bu modeli üretime sokmadan önce performansını değerlendirmemiz gerekti, bu nedenle dış örneklem performansı hakkında bilgi sunmanızı rica ediyoruz.
Gelecekteki meslektaşlarımızın bu görevi değerlendireceğini unutmayarak, çalışmamızı düzenli bir şekilde yapmaya özen gösterdik. Kodumuz temiz, açıklamalı ve takip edilmesi kolaydır, gerekli yerlerde yorumlar ve açıklamalar bulunmaktadır. Raporumuz, düşünce sürecimizi ayrıntılı bir şekilde yansıtarak mantığımızı açıklamak üzere hazırlanmıştır.
Son aşamalarda, modeli bir API uç noktasıyla açığa çıkardık. Bu uç nokta, belirli bir tarih aralığı için tahminler veya istenen bir tahmin süresi için tahminler döndürebilir. Tahmin edilen gün sayısını sağlayarak 'predictions' fonksiyonunu tetikleriz. Bu fonksiyon, modelimizi kullanarak verilen tarihten itibaren sipariş sayısını tahmin etmek için kullanılır.
Bu çalışma, teknik yeteneklerimizi sergilemenin ötesinde, tutarlı ve açıklamalı bir çözüm sunma becerimizi de gösterdi, böylece gelecekteki meslektaşlarımız tarafından değerlendirmeye hazır bir şekilde sunuldu.


# Order Prediction Application

This project contains a Flask application developed to predict daily order counts. The project works on a dataset that includes daily order counts from May 2, 2020, to June 30, 2022. Additionally, features such as temperature and marketing spend are also utilized.

## How It Works

The application runs every Monday morning to generate order predictions for the upcoming 2 weeks. Users specify the number of days they want predictions for, and the model provides order predictions for those days. Note that the temperature data is not real-time, so it's only available for past and current days. However, marketing spend is an accessible feature at prediction time.

Uncertainty of predictions is also taken into account, and prediction results are statistically evaluated.

## Installation

1. Install the required Python libraries by running the following command:

   ```bash
   pip install flask pandas statsmodels numpy joblib

Usage

When the application starts, open your browser and go to http://localhost:5001.
Enter the date and temperature value you want to predict.
Specify the number of days for which you want order predictions.
Click the "Make Prediction" button and view the results.


# Sipariş Tahmini Uygulaması

Bu proje, günlük sipariş sayısını tahmin etmek için geliştirilmiş bir Flask uygulamasını içermektedir. Proje, 2 Mayıs 2020'den 30 Haziran 2022'ye kadar olan günlük sipariş sayılarını içeren bir veri kümesi üzerine çalışmaktadır. Ayrıca, sıcaklık ve pazarlama harcaması gibi özellikler de kullanılmaktadır.

## Nasıl Çalışır

Uygulama, her Pazartesi sabahı çalıştırılarak gelecek 2 hafta için sipariş tahminleri üretir. Kullanıcı, tahmin etmek istediği gün sayısını belirtir ve bu günler için sipariş tahminlerini alır. Sıcaklık verisi gerçek zamanlı değildir, bu nedenle yalnızca geçmiş ve mevcut günler için mevcuttur. Ancak, pazarlama harcaması tahminleme anında erişilebilir bir özelliktir.

Tahminlerin belirsizliği de hesaba katılır ve tahmin sonuçları istatistiksel olarak değerlendirilir.

## Kurulum

1. Gerekli Python kütüphanelerini yüklemek için aşağıdaki komutları kullanın:

   ```bash
   pip install flask pandas statsmodels numpy joblib

Kullanım

Uygulama başladığında, tarayıcınızdan http://localhost:5001 adresine gidin.
Tahmin etmek istediğiniz tarih ve sıcaklık değerini girin.
Kaç gün boyunca sipariş tahminleri almak istediğinizi belirtin.
"Tahmin Yap" düğmesine tıklayın ve sonuçları görün.


