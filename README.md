Türkiye İkinci El Araç Fiyat Tahminleme Projesi
2020 Türkiye araç fiyatları dataseti kullanılarak fiyat tahmini yapmaya çalışan ML projesi.

Proje Hakkında
Projenin amacı, bir aracın markası, modeli, yaşı, kilometresi, motor hacmi gibi özelliklerini kullanarak piyasa değerini en doğru şekilde tahmin etmektir. Analiz sürecinde veri seti detaylı bir şekilde işlenmiş ve LazyPredict kütüphanesi kullanılarak en iyi model performansı araştırılmıştır. Sonuç olarak Random Forest Regressor modeli seçilmiş ve optimize edilmiştir.

Veri İşleme: pandas, numpy

Görselleştirme: matplotlib, plotly, sns

Makine Öğrenmesi: scikit-learn, lazypredict, RandomForestRegression, StandardScaler


Veri Temizleme:

Gereksiz sütunlar çıkarıldı.

"Bilmiyorum" veya "-" gibi eksik veriler temizlendi veya dolduruldu 

Encoding (Dönüştürme):

Kategorik veriler (Yakıt, Vites) LabelEncoder ile,

Nominal veriler (Renk, Kasa Tipi, Kimden) One-Hot Encoding (get_dummies) ile sayısal verilere dönüştürüldü.

Modelleme Süreci
Veri Ayrımı: Veri seti %70 Eğitim, %30 Test olarak ayrıldı.

Ölçeklendirme: Veriler StandardScaler kullanılarak normalize edildi.

Model Seçimi: LazyRegressor kullanılarak çeşitli ML algoritmalarının başarı oranları karşılaştırılıp en uygunu kullanıldı.

Seçilen Model: Aşırı öğrenme (overfitting) riskini iyi yönetmesi ve yüksek başarısı nedeniyle Random Forest Regressor seçildi.

Hiperparametre Optimizasyonu: GridSearchCV kullanılarak modelin parametreleri (n_estimators, max_depth, min_samples_split vb.) optimize edildi. Ve en iyi sonuç kullanıldı.

Sonuç
Optimize edilmiş Random Forest modeli ile elde edilen test sonuçları:

R2 Skoru: ~0.90 (Model, fiyat değişimlerinin %90'ını açıklayabiliyor.)

RMSE (Hata Kareler Ortalaması Karekökü): ~66,860 TL

Grafikler
<img width="824" height="358" alt="image" src="https://github.com/user-attachments/assets/f58e8d5d-924b-4502-b59b-6d5999984449" />
<img width="673" height="362" alt="image" src="https://github.com/user-attachments/assets/c68792c4-0e19-4534-94e3-f0b60cfbb06c" />
<img width="770" height="372" alt="Ekran görüntüsü 2025-11-22 182320" src="https://github.com/user-attachments/assets/9bb1f449-5efe-483f-ac6d-1fa958a1a4ae" />
