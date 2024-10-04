# Docker Image Komutları

Docker ile imaj yönetimi yapmak için kullanılan komutlar ve açıklamaları:

## 1. `docker image ls`
Docker sistemindeki mevcut imajları listeler.

**Kullanım Örneği:**
```bash
docker image ls
```
**Açıklama:** 
Bu komut, sistemde yüklü olan tüm Docker imajlarını, etiketlerini, ID'lerini ve boyutlarını gösterir. Bu, kullanılabilir imajları görüntülemek için kullanılır.

---

## 2. `docker image pull <image-name>`
Belirtilen imajı Docker Hub gibi bir uzak depodan indirir.

**Kullanım Örneği:**
```bash
docker image pull nginx
```
**Açıklama:**
Bu komut, Nginx imajını Docker Hub'dan indirir ve yerel sistemde kullanılabilir hale getirir.

---

## 3. `docker image rm <image-id|image-name>`
Belirtilen imajı sistemden siler.

**Kullanım Örneği:**
```bash
docker image rm nginx
```
**Açıklama:**
Bu komut, "nginx" adlı Docker imajını sistemden kaldırır. İmaj ID'si ile de işlem yapılabilir.

---

## 4. `docker image inspect <image-id|image-name>`
Belirtilen imaj hakkında detaylı bilgi verir.

**Kullanım Örneği:**
```bash
docker image inspect nginx
```
**Açıklama:**
Bu komut, "nginx" adlı imajın meta verilerini (katmanları, yapılandırmaları) ve diğer detayları görüntüler.

---

## 5. `docker image prune`
Kullanılmayan tüm yerel imajları siler.

**Kullanım Örneği:**
```bash
docker image prune
```
**Açıklama:**
Bu komut, referans edilmeyen, kullanılmayan tüm Docker imajlarını temizleyerek disk alanı açılmasına yardımcı olur.

---

## 6. `docker image tag <source-image> <target-image>`
Bir imajı yeniden etiketler.

**Kullanım Örneği:**
```bash
docker image tag nginx mynginx:v1
```
**Açıklama:**
Bu komut, mevcut "nginx" imajını "mynginx:v1" adıyla etiketler ve yeni bir imaj oluşturur.

---

## 7. `docker image build -t <image-name> <path>`
Bir Dockerfile'dan yeni bir imaj oluşturur.

**Kullanım Örneği:**
```bash
docker image build -t myapp:latest .
```
**Açıklama:**
Bu komut, mevcut dizindeki Dockerfile'ı kullanarak "myapp:latest" adıyla yeni bir Docker imajı oluşturur.

---

## 8. `docker image push <image-name>`
Yerel imajı Docker Hub gibi uzak bir Docker deposuna gönderir.

**Kullanım Örneği:**
```bash
docker image push mynginx:v1
```
**Açıklama:**
Bu komut, yerel "mynginx:v1" imajını Docker Hub gibi uzak bir depoya gönderir.

---

## 9. `docker image history <image-name>`
Bir imajın katmanlarını ve geçmişini gösterir.

**Kullanım Örneği:**
```bash
docker image history nginx
```
**Açıklama:**
Bu komut, "nginx" imajının tüm katmanlarını ve hangi adımlarla oluşturulduğunu görüntüler.

---

## 10. `docker image save -o <output-file> <image-name>`
Belirtilen imajı bir dosyaya kaydeder.

**Kullanım Örneği:**
```bash
docker image save -o mynginx.tar mynginx:v1
```
**Açıklama:**
Bu komut, "mynginx:v1" imajını "mynginx.tar" adlı bir dosyaya kaydeder. Bu, imajın başka bir sisteme taşınması için kullanılabilir.

---

## 11. `docker image load -i <input-file>`
Kaydedilmiş bir imajı dosyadan geri yükler.

**Kullanım Örneği:**
```bash
docker image load -i mynginx.tar
```
**Açıklama:**
Bu komut, "mynginx.tar" adlı dosyadaki imajı Docker sistemine yükler ve kullanıma hazır hale getirir.
