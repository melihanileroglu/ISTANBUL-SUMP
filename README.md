# 🚇 İstanbul SUMP

**İstanbul Sürdürülebilir Kentsel Hareketlilik Planı (SUMP)**, Avrupa Birliği'nin desteklediği ve İstanbul'un ulaşım geleceğini şekillendirmeyi amaçlayan uzun vadeli ve bütüncül bir planlama sürecidir. Bu süreçte, veriye dayalı karar alma sistemlerinin temeli olarak **Hanehalkı Ulaşım Anketi (HTS)** önemli bir rol oynamaktadır.

---

## 📊 HTS Verilerine Genel Bakış

Bu çalışma kapsamında toplanan veri seti, İstanbul’daki bireylerin ve hanehalklarının ulaşım alışkanlıklarını ayrıntılı şekilde ortaya koymaktadır. Aşağıdaki tabloda, verilerin kapsamı özetlenmiştir:

| 📁 **Veri Kategorisi**         | 🔢 **Kayıt Sayısı** |
|-------------------------------|----------------------|
| 👤 **Profil (Birey Bilgileri)**        | 169.423              |
| 🏠 **Hanehalkı**                | 59.879               |
| 📝 **Anket Formları**           | 65.954               |
| 🚗 **Araç Sahipliği**           | 23.084               |
| 🧱 **Seyahat Ayakları (Trip_leg)** | 245.254           |
| 🚳 **Seyahatler (Trip)**        | 235.540              |

> 🧹 *Bu veri setleri; toplu taşıma tercihleri, araç sahipliği durumu, yürüme ve mikromobilite davranışları gibi birçok alanda analiz yapılmasını sağlamaktadır.*

---

## ⚙️ HTS Verisi İşleme Süreci

HTS verileri kullanılmadan önce çeşitli temizleme ve filtreleme adımlarından geçirilmiştir. Aşağıdaki tabloda, işlem adımları ve veri sayısındaki değişim özetlenmiştir:

| 🔢 **Adım No** | 🔄 **Aşama** | 📝 **Açıklama** | 🧱 **TripLeg (Birlikte)** | 🚳 **Trip (Birlikte)** | 🧱 **TripLeg** | 🚳 **Trip** |
|---------------|--------------|----------------|--------------------------|------------------------|---------------|-------------|
| 1 | Ham Veri | Başlangıçta tüm birlikte yolculuk kayıtları dahil olmak üzere ham veri kullanıldı. | 245.254 | 235.540 | 212.242 | 207.173 |
| 2 | İşleme | Birlikte yolculuk yapan - diğer kişilerin veriden silinmesi. (Diğer yolcuların p_id'si olmadığı için Trip verisine etkisi yok.) | 240.891 | 235.540 | **Yok** | **Yok** |
| 3 | İşleme | `travel_time` değeri boş olan ve `vehicle_time < 0` olan kayıtlar silindi. Bu işlem **trip** bazında yapıldı. | 240.800 | 235.468 | 212.152 | 207.102 |
| 4 | İşleme | `travel_time`, belirlenen zaman aralıklarına uymayan trip kayıtları çıkarıldı: (1-5, 5-10, ..., 225-240 dakika) | 238.883 | 233.670 | 210.428 | 205.481 |

> 📌 *Bu işlemler sonucunda analiz için daha güvenilir ve tutarlı bir veri seti elde edilmiştir.*

---

## 🎯 Neden Önemli?

- İstanbul genelinde ulaşım talebini **alan bazında analiz etme** imkânı sunar.  
- Erişilebilirlik, **toplu taşıma kullanımı**, **araç bağımlılığı** ve **aktif ulaşım** gibi kavramların mekânsal ve sosyo-demografik düzeyde incelenmesini mümkün kılar.  
- **SUMP stratejilerinin şekillendirilmesi**, **yatırım önceliklerinin belirlenmesi** ve **karbon emisyonlarının azaltılması** gibi hedeflere doğrudan katkı sunar.  

---

## 🧠 Devam Eden Analizler

HTS verileri, aşağıdaki analiz modüllerinin temelini oluşturmaktadır:

- 🚶 **Yürünebilirlik ve Mikromobilite Davranışları**  
- 🚍 **Toplu Taşıma Performans ve Erişilebilirlik Analizi**  
- 🗺️ **Mekansal Seyahat Yoğunluğu Dağılımı**  
- ⏱️ **Seyahat Süreleri, Bekleme ve Aktarma Analizi**  
- 👥 **Demografik Temelli Ulaşım Eğilimleri**

---

> 🔹 *Aşağıdaki bölümlerde veri toplama metodolojisi, analiz yaklaşımları ve çıktıları detaylandırabilirsiniz.*

- 📌 Veri Toplama Süreci ve Metodolojisi  
- 🏞️ İlçelere Göre Seyahat Davranışları  
- 🌍 Öne Çıkan Bulgular ve Stratejik Öneriler

