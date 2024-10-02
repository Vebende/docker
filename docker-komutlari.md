### Temel Docker Komutları

1. **docker --version**
   - **Anlamı**: Yüklü Docker sürümünü gösterir.
   - **Kullanım**: Docker'ın doğru kurulduğunu ve hangi sürümde olduğunu kontrol etmek için.

   ```bash
   docker --version
   ```

2. **docker pull [image_name]**
   - **Anlamı**: Docker Hub'dan bir imajı indirir.
   - **Kullanım**: Docker konteyneri oluşturmak için bir imaj indirmek gerektiğinde.

   ```bash
   docker pull ubuntu
   ```

3. **docker run [options] [image_name]**
   - **Anlamı**: Belirtilen Docker imajını kullanarak bir konteyner çalıştırır.
   - **Kullanım**: Bir konteyner oluşturup başlatmak için.

   ```bash
   docker run ubuntu
   ```

   - **Seçenekler**:
     - `-it`: Etkileşimli modda başlatmak için (örn: bir terminal açmak).
     - `-d`: Arka planda (detached) çalıştırmak için.
     - `--name [container_name]`: Konteyner adı vermek için.

   ```bash
   docker run -it ubuntu bash
   ```

4. **docker ps**
   - **Anlamı**: Çalışan Docker konteynerlerini listeler.
   - **Kullanım**: Hangi konteynerlerin aktif olduğunu görmek için.

   ```bash
   docker ps
   ```

5. **docker ps -a**
   - **Anlamı**: Tüm (çalışan ve durdurulmuş) Docker konteynerlerini listeler.
   - **Kullanım**: Geçmişte başlatılan tüm konteynerleri görmek için.

   ```bash
   docker ps -a
   ```

6. **docker stop [container_name_or_id]**
   - **Anlamı**: Çalışan bir konteyneri durdurur.
   - **Kullanım**: Aktif bir konteyneri sonlandırmak için.

   ```bash
   docker stop my_container
   ```

7. **docker start [container_name_or_id]**
   - **Anlamı**: Durdurulmuş bir konteyneri başlatır.
   - **Kullanım**: Daha önce durdurulmuş bir konteyneri yeniden başlatmak için.

   ```bash
   docker start my_container
   ```

8. **docker rm [container_name_or_id]**
   - **Anlamı**: Belirtilen konteyneri siler.
   - **Kullanım**: Bir konteyneri kalıcı olarak kaldırmak için.

   ```bash
   docker rm my_container
   ```

9. **docker rmi [image_name_or_id]**
   - **Anlamı**: Belirtilen Docker imajını siler.
   - **Kullanım**: Sistemden artık kullanılmayan imajları kaldırmak için.

   ```bash
   docker rmi ubuntu
   ```

10. **docker images**
    - **Anlamı**: İndirilen tüm Docker imajlarını listeler.
    - **Kullanım**: Yerel sistemde hangi Docker imajlarının olduğunu görmek için.

    ```bash
    docker images
    ```

### İleri Düzey Docker Komutları

11. **docker exec [options] [container_name_or_id] [command]**
    - **Anlamı**: Çalışan bir konteynerin içine komut çalıştırır.
    - **Kullanım**: Çalışan bir konteynerde komut çalıştırmak için, örneğin bash kabuğuna girmek.

    ```bash
    docker exec -it my_container bash
    ```

12. **docker build [options] [path]**
    - **Anlamı**: Dockerfile kullanarak bir imaj oluşturur.
    - **Kullanım**: Dockerfile ile bir uygulamayı paketleyip imaj oluşturmak için.

    ```bash
    docker build -t my_image .
    ```

    - `-t`: Oluşturulan imaja bir isim vermek için.

13. **docker logs [container_name_or_id]**
    - **Anlamı**: Bir konteynerin loglarını görüntüler.
    - **Kullanım**: Konteynerde oluşan hataları veya işlemleri izlemek için.

    ```bash
    docker logs my_container
    ```

14. **docker pull [repository/image:tag]**
    - **Anlamı**: Belirli bir imajı ve etiketini Docker Hub'dan indirir.
    - **Kullanım**: İmajın belirli bir sürümünü indirmek için.

    ```bash
    docker pull nginx:latest
    ```

15. **docker commit [container_id] [new_image_name]**
    - **Anlamı**: Bir konteynerin mevcut durumunu yeni bir Docker imajı olarak kaydeder.
    - **Kullanım**: Çalışan bir konteynerden yeni bir imaj oluşturmak için.

    ```bash
    docker commit my_container my_new_image
    ```

16. **docker network ls**
    - **Anlamı**: Docker ağlarını listeler.
    - **Kullanım**: Mevcut Docker ağlarını görmek için.

    ```bash
    docker network ls
    ```

17. **docker volume ls**
    - **Anlamı**: Docker hacimlerini (volumes) listeler.
    - **Kullanım**: Mevcut depolama hacimlerini görüntülemek için.

    ```bash
    docker volume ls
    ```

18. **docker inspect [container_name_or_id]**
    - **Anlamı**: Bir konteynerin veya imajın ayrıntılı yapılandırmasını gösterir.
    - **Kullanım**: Konteynerin veya imajın meta verilerini görmek için.

    ```bash
    docker inspect my_container
    ```

19. **docker-compose up**
    - **Anlamı**: `docker-compose.yml` dosyasındaki tanımlamalara göre birden fazla konteyneri başlatır.
    - **Kullanım**: Birden fazla servisi içeren Docker uygulamalarını kolayca çalıştırmak için.

    ```bash
    docker-compose up
    ```

20. **docker-compose down**
    - **Anlamı**: `docker-compose up` ile başlatılmış tüm konteynerleri durdurur ve temizler.
    - **Kullanım**: Tüm bağlı hizmetleri kapatmak için.

    ```bash
    docker-compose down
    ```
