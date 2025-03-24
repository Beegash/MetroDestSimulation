# Metro Ağı Simülasyonu

Bu proje, bir metro ağı simülasyonu gerçekleştiren ve farklı rota bulma algoritmalarını uygulayan bir Python uygulamasıdır.

## 🚇 Proje Hakkında

Bu simülasyon, gerçek bir metro ağını temsil eden ve yolcular için en uygun rotaları bulan bir sistemdir. Proje, farklı metro hatlarını, istasyonları ve bunlar arasındaki geçiş sürelerini modelleyerek en optimal rotaları hesaplar.


## 📊 Temel Özellikler

1. **Metro Ağı Modelleme**
   - İstasyonlar ve hatlar arası bağlantılar
   - Geçiş süreleri
   - Hat bazlı organizasyon

2. **Rota Bulma Algoritmaları**
   - En az aktarmalı rota (BFS)
   - En hızlı rota (A* algoritması)

3. **Görselleştirme**
   - Ağ yapısının interaktif gösterimi
   - Algoritmaların çalışma adımlarının görselleştirilmesi
   - Hat bazlı renklendirme

## 🔍 Algoritma Görselleştirmeleri

### Metro Ağı Yapısı
![Metro Ağı](https://github.com/user-attachments/assets/919ca00a-c91e-4380-813d-f4b0404498e6)

Bu görselleştirmede:
- Kırmızı düğümler: Kırmızı Hat istasyonları
- Mavi düğümler: Mavi Hat istasyonları
- Turuncu düğümler: Turuncu Hat istasyonları
- Kenarlar üzerindeki sayılar: İstasyonlar arası seyahat süreleri (dakika)

### BFS (Breadth-First Search) Algoritması
![BFS Algoritması](https://github.com/user-attachments/assets/fb05bfd8-dbe2-4b5c-9f94-924951c6d441)

BFS algoritması görselleştirmesinde:
- Sarı düğümler: Algoritmanın keşfettiği istasyonlar
- Yeşil kalın çizgiler: Bulunan en kısa rota
- Düğümler üzerindeki sayılar: Algoritmanın kaçıncı adımda bu istasyonu keşfettiği

### A* Algoritması
![A* Algoritması](https://github.com/user-attachments/assets/302ed105-32b2-4a9d-9c53-8029fbf0d50d)

A* algoritması görselleştirmesinde:
- Sarı düğümler: Algoritmanın keşfettiği istasyonlar
- Yeşil kalın çizgiler: Bulunan en optimal rota
- Düğümler üzerindeki sayılar: Toplam seyahat süresi
- Kenarlar üzerindeki sayılar: İstasyonlar arası geçiş süresi ve o noktaya kadar olan toplam süre

## 🔍 Kullanılan Algoritmalar

### 1. BFS (Breadth-First Search) - En Az Aktarmalı Rota
```python
def en_az_aktarma_bul(self, baslangic_id: str, hedef_id: str)
```
- **Amaç**: En az istasyon geçişi gerektiren rotayı bulma
- **Çalışma Prensibi**: Seviye seviye arama yaparak en kısa yolu bulur
- **Veri Yapısı**: Çift yönlü kuyruk (deque)
- **Zaman Karmaşıklığı**: O(V + E) [V: istasyon sayısı, E: bağlantı sayısı]
- **Avantajlar**: 
  - Her zaman en az istasyon geçişli rotayı bulur
  - Aktarma sayısını minimize eder
  - Basit ve anlaşılır

### 2. A* Algoritması - En Hızlı Rota
```python
def en_hizli_rota_bul(self, baslangic_id: str, hedef_id: str)
```
- **Amaç**: En kısa sürede hedefe ulaşan rotayı bulma
- **Çalışma Prensibi**: Öncelik kuyruğu kullanarak en optimal yolu bulur
- **Veri Yapısı**: Öncelik kuyruğu (heapq)
- **Zaman Karmaşıklığı**: O(E log V)
- **Avantajlar**:
  - Seyahat sürelerini dikkate alır
  - Her zaman en hızlı rotayı bulur
  - Akıllı arama stratejisi sayesinde daha az düğüm keşfeder

## 📝 Sınıf Yapısı

### Istasyon Sınıfı
- İstasyon bilgilerini tutar
- Komşu istasyonları ve geçiş sürelerini yönetir

### MetroAgi Sınıfı
- Tüm ağ yapısını yönetir
- Rota bulma algoritmalarını içerir
- İstasyon ve bağlantı ekleme fonksiyonlarını barındırır

## 🚀 Kullanım Örneği

```python
# Metro ağı oluşturma
metro = MetroAgi()

# İstasyon ekleme
metro.istasyon_ekle("K1", "Kızılay", "Kırmızı Hat")
metro.istasyon_ekle("M1", "AŞTİ", "Mavi Hat")

# Bağlantı ekleme
metro.baglanti_ekle("K1", "M1", 5)

```

## 🔧 Kurulum

1. Projeyi klonlayın:
```bash
git clone [https://github.com/Beegash/MetroNetworkSimulation   ]
```

2. Projeyi çalıştırın:
```bash
python IzzettinFurkanOzmen_MetroSimulation.py
```



