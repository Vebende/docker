# Docker Maintenance (Bakım) Komutları

Docker'ın disk alanını yönetmek ve performansı artırmak için kullanılabilecek bakım ve temizlik komutları:

## 1. `docker system prune`
Kullanılmayan tüm Docker objelerini (durdurulmuş konteynerler, gereksiz ağlar, boştaki imajlar ve önbellek) temizler.

**Kullanım Örneği:**
```bash
docker system prune
```
**Açıklama:**
Bu komut, sistemde yer kaplayan ancak kullanılmayan verileri temizler. Disk alanını geri kazanmak ve sistemin performansını artırmak için kullanılır.

**Tüm Kullanılmayan Objeleri Temizle (İmajlar Dahil):**
```bash
docker system prune -a
```
Bu komut ayrıca, referans edilmeyen kullanılmayan imajları da temizler.

---

## 2. `docker image prune`
Kullanılmayan tüm Docker imajlarını temizler.

**Kullanım Örneği:**
```bash
docker image prune
```
**Açıklama:**
Bu komut, hiçbir konteynerin kullanmadığı boştaki imajları temizler. Disk alanını açmak için faydalıdır.

**Tüm Boş İmajları Temizle (Etiketlenmemiş Olanlar Dahil):**
```bash
docker image prune -a
```
Bu komut, boştaki tüm imajları (etiketlenmemiş olanlar dahil) temizler.

---

## 3. `docker container prune`
Kullanılmayan durdurulmuş tüm konteynerleri temizler.

**Kullanım Örneği:**
```bash
docker container prune
```
**Açıklama:**
Bu komut, durdurulmuş tüm konteynerleri temizler. Sistem kaynaklarını gereksiz yere tüketen konteynerleri kaldırmak için kullanılır.

---

## 4. `docker volume prune`
Kullanılmayan tüm Docker hacimlerini (volumes) temizler.

**Kullanım Örneği:**
```bash
docker volume prune
```
**Açıklama:**
Bu komut, hiçbir konteyner tarafından kullanılmayan hacimleri temizler. Disk alanı kazanmak için gereksiz hacimlerin silinmesinde kullanılır.

---

## 5. `docker network prune`
Kullanılmayan Docker ağlarını temizler.

**Kullanım Örneği:**
```bash
docker network prune
```
**Açıklama:**
Bu komut, hiçbir konteynerin kullanmadığı ağları temizler. Ağ yapılandırmasını düzenli tutmak ve sistem kaynaklarını optimize etmek için kullanılır.

---

## 6. `docker builder prune`
Kullanılmayan tüm yapı (build) önbelleğini temizler.

**Kullanım Örneği:**
```bash
docker builder prune
```
**Açıklama:**
Bu komut, Docker imajları oluştururken biriken yapı önbelleğini temizler. Disk alanı yönetimi ve yapı işlemlerinin hızlandırılması için faydalıdır.

**Tüm Build Olanları Sil:**
```bash
docker builder prune --all
```
Bu komut, tüm build önbelleklerini temizler.

---

## 7. `docker system df`
Docker'da disk kullanımını gösterir.

**Kullanım Örneği:**
```bash
docker system df
```
**Açıklama:**
Bu komut, Docker'ın ne kadar disk alanı kullandığını detaylı şekilde gösterir. Konteynerler, imajlar, ağlar ve hacimlerin boyutları hakkında bilgi verir.
