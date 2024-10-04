# Container Run  
Aşağıdaki komut, Docker kullanarak bir Alpine Linux konteyneri başlatır ve ardından basit bir şekilde "hello world!" ifadesini ekrana yazdırır:

```bash
docker container run alpine echo hello world!
```

### Komutun Açıklaması:

1. **`docker container run`**:
   - Bu komut, yeni bir Docker konteyneri çalıştırmak için kullanılır. Eğer belirtilen image mevcut değilse, Docker önce bu imajı indirir ve ardından çalıştırır.
   
2. **`alpine`**:
   - Bu, çalıştırılacak olan konteynerin temel aldığı Docker imajıdır. Alpine, küçük ve hafif bir Linux dağıtımıdır. 
   
3. **`echo hello world!`**:
   - Konteyner başlatıldıktan sonra içinde çalıştırılacak komuttur. Burada `echo` komutu ile "hello world!" mesajı terminale yazdırılır.

### Özet:

Bu komut bir Alpine Linux imajını kullanarak geçici bir konteyner başlatır, sadece "hello world!" ifadesini yazdırır ve ardından konteyner kapanır.

# Container'ları Anlamak 
### 1. `docker container run`
```bash
docker container run [OPTIONS] IMAGE [COMMAND] [ARG...]
```
- Belirtilen imajı temel alarak bir konteyner çalıştırır. Eğer imaj yerel olarak mevcut değilse, önce imajı indirir.
- Örnek: 
  ```bash
  docker container run alpine echo "Hello from Alpine"
  ```

### 2. `docker container start`
```bash
docker container start [OPTIONS] CONTAINER [CONTAINER...]
```
- Daha önce oluşturulmuş ve durdurulmuş bir konteyneri yeniden başlatır.
- Örnek:
  ```bash
  docker container start my_container
  ```

### 3. `docker container stop`
```bash
docker container stop [OPTIONS] CONTAINER [CONTAINER...]
```
- Çalışan bir konteyneri durdurur.
- Örnek:
  ```bash
  docker container stop my_container
  ```

### 4. `docker container restart`
```bash
docker container restart [OPTIONS] CONTAINER [CONTAINER...]
```
- Çalışan veya durdurulmuş bir konteyneri yeniden başlatır.
- Örnek:
  ```bash
  docker container restart my_container
  ```

### 5. `docker container rm`
```bash
docker container rm [OPTIONS] CONTAINER [CONTAINER...]
```
- Belirtilen konteyner(leri) siler. Durdurulmuş bir konteynerin silinmesi gerekir.
- Örnek:
  ```bash
  docker container rm my_container
  ```

### 6. `docker container ls`
```bash
docker container ls [OPTIONS]
```
- Çalışan konteynerlerin listesini gösterir. `-a` opsiyonu ile durdurulmuş olanlar da gösterilebilir.
- Örnek:
  ```bash
  docker container ls
  docker container ls -a
  ```

### 7. `docker container exec`
```bash
docker container exec [OPTIONS] CONTAINER COMMAND [ARG...]
```
- Çalışan bir konteynerin içinde bir komut çalıştırır.
- Örnek:
  ```bash
  docker container exec -it my_container /bin/sh
  ```

### 8. `docker container logs`
```bash
docker container logs [OPTIONS] CONTAINER
```
- Belirtilen konteynerin loglarını gösterir.
- Örnek:
  ```bash
  docker container logs my_container
  ```

### 9. `docker container inspect`
```bash
docker container inspect [OPTIONS] CONTAINER [CONTAINER...]
```
- Belirtilen konteynerin detaylı yapılandırma ve durum bilgilerini JSON formatında gösterir.
- Örnek:
  ```bash
  docker container inspect my_container
  ```

### 10. `docker container top`
```bash
docker container top CONTAINER [ps OPTIONS]
```
- Belirtilen konteyner içinde çalışan işlemleri listeler.
- Örnek:
  ```bash
  docker container top my_container
  ```

### 11. `docker container stats`
```bash
docker container stats [OPTIONS] [CONTAINER...]
```
- Konteynerlerin gerçek zamanlı performans istatistiklerini gösterir.
- Örnek:
  ```bash
  docker container stats my_container
  ```

### 12. `docker container attach`
```bash
docker container attach [OPTIONS] CONTAINER
```
- Belirtilen konteynerin standart giriş/çıkış akışına bağlanır. Özellikle interaktif modda çalışan konteynerler için kullanılır. Bu komut sayesinde host edilen işletim sisteminde kuruluymuş gibi komutları çalıştırmaya devam edebilirsiniz
- Örnek:
  ```bash
  docker container attach my_container
  ```

### 13. `docker container cp`
```bash
docker container cp [OPTIONS] CONTAINER:SRC_PATH DEST_PATH|-
```
- Konteynerden host makineye veya hosttan konteynere dosya kopyalar.
- Örnek:
  ```bash
  docker container cp my_container:/path/to/file /local/path
  ```

### 14. `docker container commit`
```bash
docker container commit [OPTIONS] CONTAINER [REPOSITORY[:TAG]]
```
- Mevcut bir konteynerin anlık durumunu bir imaj olarak kaydeder.
- Örnek:
  ```bash
  docker container commit my_container my_image
  ```

### 15. `docker container pause`
```bash
docker container pause [CONTAINER...]
```
- Bir konteyneri geçici olarak durdurur (CPU gibi kaynaklar askıya alınır).
- Örnek:
  ```bash
  docker container pause my_container
  ```

### 16. `docker container unpause`
```bash
docker container unpause [CONTAINER...]
```
- Askıya alınmış (pause) bir konteyneri yeniden çalıştırır.
- Örnek:
  ```bash
  docker container unpause my_container
  ```

### 17. `docker container rename`
```bash
docker container rename CONTAINER NEW_NAME
```
- Mevcut bir konteynerin adını değiştirir.
- Örnek:
  ```bash
  docker container rename old_name new_name
  ```

### 18. `docker container prune`
```bash
docker container prune
```
- Durdurulmuş tüm konteynerleri temizler (siler).
- Örnek:
  ```bash
  docker container prune
  ```

---

Bu komutlar Docker konteynerlerini yönetmek, izlemek ve çalıştırmak için kullanılır. Geliştirme sürecinde konteynerlerin durumu, performansı ve yapılandırılması gibi birçok önemli işlevi sağlar.
