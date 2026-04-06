# 🚌 İzmir ESHOT Ulaşım Ağı Analizi (Geliştirme Aşamasında 🚧)

Bu proje, İzmir Büyükşehir Belediyesi'nin sağladığı açık verileri (GTFS) kullanarak şehir içi otobüs ulaşım ağını veri bilimi yöntemleriyle analiz etmeyi amaçlamaktadır. Proje, bir YBS öğrencisinin veri işleme, görselleştirme ve içgörü üretme süreçlerini yansıtmaktadır.

## 📍 Veri Kaynağı
Veriler, [İzmir Büyükşehir Belediyesi Açık Veri Portalı](https://acikveri.bizizmir.com/tr/dataset/toplu-ulasim-gtfs-verileri) üzerinden temin edilmiştir. 
*Veri Seti:* Toplu Ulaşım GTFS Verileri

## 🚀 Projenin Amacı
İzmir'deki 400'den fazla otobüs hattının operasyonel verimliliğini ölçmek, yoğunluk haritalarını çıkarmak ve sosyal erişilebilirlik (engelli dostu araçlar vb.) analizleri yaparak iyileştirme önerileri sunmak.

## 🛠️ Yapılan Çalışmalar & Yetkinlikler
- **Veri Temizleme (Wrangling):** Ham `.txt` formatındaki GTFS dosyaları (stops, routes, trips, stop_times) Pandas kullanılarak ilişkisel bir yapıya dönüştürüldü.
- **Merge & Mapping:** Teknik `route_id` değerleri, vatandaşların kullandığı gerçek hat numaraları (`route_short_name`) ile eşleştirildi.
- **Zaman Serisi Analizi:** Otobüs seferlerinin gün içindeki dağılımı analiz edilerek sabah ve akşam pik saatleri (08:00 ve 18:00) verilerle kanıtlandı.
- **Donanım Optimizasyonu:** Büyük veri setleri (stop_times), **Apple M4 Chip (MPS)** desteği ve Pandas optimizasyon teknikleri kullanılarak işlendi.

## 📊 Öne Çıkan Bulgular
* **En İşlek Hat:** Sefer sayısı baz alındığında İzmir'in ana omurgasını 800, 587 gibi hatların oluşturduğu saptandı.
* **Sefer Yoğunluğu:** Seferlerin sabah 07:00-09:00 arasında maksimuma ulaştığı, gece saatlerinde ise operasyonel minimuma indiği görselleştirildi.

## 🚧 Gelecek Planları (Roadmap)
- [ ] **Makine Öğrenmesi:** Sefer sürelerini ve olası gecikmeleri tahmin eden bir regresyon modeli geliştirilecek.
- [ ] **Harita Görselleştirme:** Folium kütüphanesi ile durak yoğunluk ısı haritası (Heatmap) eklenecek.

## 💻 Kullanılan Teknolojiler
- **Dil:** Python
- **Kütüphaneler:** Pandas, Matplotlib, Folium
- **Donanım:** MacBook Air M4
