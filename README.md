🏦 Makine Öğrenmesi ile Banka Vadeli Mevduat Tahmini

Bu proje, bir Portekiz bankasının doğrudan pazarlama kampanyalarından elde edilen verileri kullanarak müşterilerin vadeli mevduat açıp açmayacağını tahmin etmeyi amaçlayan bir makine öğrenmesi çalışmasıdır.

📌 Projenin Amacı

Telefonda yapılan pazarlama görüşmelerine verilen yanıtları analiz ederek, müşterinin “Evet, vadeli mevduat açıyorum” deme olasılığını makine öğrenmesi modelleriyle tahmin etmek.

Bu sayede:

Bankaların pazarlama maliyetlerini düşürmesi,

Doğru müşteri segmentine ulaşması,

Kampanyaların daha verimli yürütülmesi
hedeflenir.

📂 Veri Seti Hakkında

Bu çalışma, UCI Machine Learning Repository üzerinde yer alan Bank Marketing Dataset kullanılarak yapılmıştır.

Veri seti:

Portekiz’deki bir bankanın telefonla yapılan kampanyaları içeriyor.

Her müşteri için demografik bilgiler, önceki kampanya temas bilgileri, ekonomik göstergeler ve çağrı sonuçları bulunuyor.

Hedef değişken (y) = müşteri vadeli mevduata abone oldu mu? (yes/no)

🧹 Veri Hazırlama & Temizleme

Projede veri işleme aşamasında şunlar uygulandı:

✔ Eksik değer kontrolleri
✔ Kategorik değişkenleri “dummy encoding”
✔ Aykırı değer tespiti ve temizleme (Özellikle duration sütunu için IQR yöntemi)
✔ Eğitim/test ayrımı (80/20)
✔ Ölçeklendirme işlemleri (gerekli modellerde)

🔍 Keşifsel Veri Analizi (EDA)

Veri ilişkilerini anlamak için detaylı EDA yapıldı:

Korelasyon analizi

Hedef değişkene göre sınıf dağılımı

Yaş, meslek, eğitim gibi demografik değişkenlerin etkileri

Çağrı süresinin müşteri kararına etkisi

Ekonomik göstergeler ile abonelik arasındaki bağlantılar

🤖 Kullanılan Modeller

Aşağıdaki modeller eğitildi ve karşılaştırıldı:

Lojistik Regresyon

Karar Ağaçları

Random Forest

Gradient Boosting / AdaBoost / XGBoost

KNN

Destek Vektör Makineleri (SVM)

Yapay Sinir Ağları

Ayrıca RFE (Recursive Feature Elimination) yöntemiyle en anlamlı değişkenler seçildi.

🏆 Model Sonuçları

Tüm modeller karşılaştırıldığında:

🔥 En iyi performans: XGBoost Classifier

Yüksek doğruluk

Düşük hata (MAE / LogLoss)

Kararlı sonuçlar

Karmaşık ilişkileri iyi öğrenme

XGBoost'un başarısı nedeniyle proje finalinde ana model olarak seçilmiştir.

📊 Performans Değerlendirme

Modeller aşağıdaki metriklerle değerlendirildi:

Accuracy

Precision / Recall

F1-Score

ROC-AUC

Confusion Matrix

Sonuçlar tablo ve grafiklerle görselleştirilmiştir.

🛠 Kullanılan Teknolojiler

Python 3.11

pandas

numpy

matplotlib

seaborn

scikit-learn

xgboost

statsmodels

tensorflow (NN deneyleri için)

📌 Sonuç

Bu proje, bankacılık pazarlamasında kullanılabilecek güçlü bir müşteri tahmin modeli ortaya çıkardı.
XGBoost modeli, kampanya verilerini başarılı şekilde öğrenerek müşterilerin vadeli mevduata abone olup olmayacağını yüksek doğrulukla tahmin edebildi.
