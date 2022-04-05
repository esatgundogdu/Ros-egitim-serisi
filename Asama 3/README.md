# Ros-egitim-serisi
## Aşama 3 - Control

* ### Hedef: Bu aşamada hedefimiz geçtiğimiz aşamada oluşturduğumuz modeli kontrol etmek.

* ### Seri boyunca verilen görevleri nasıl yapacağınızı internetten araştırmanız beklenmektedir. Takıldığınız yerlerde GAT2 repo'sundan yardım alabilirsiniz.

* ### Gerekli ön bilgiler:
  1. TF (Kısa bir ön araştırma iyi olur)

* ### Kullanılacak paketler:
  * Ros controller
  * Robot_state_publisher

* ### Bu aşamada yapılması gerekenler: 
    1. Öncelikle ros-controllers paketini indiriyoruz.
    2. Workspace'de yeni bir paket oluşturuyoruz. 
       1. "<workspace_ismi>_control"
       2. Paket içerisinde launch dizinine launch dosyası oluşturuyoruz.
    3. URDF dosyası içine gazebo_ros_control pluginini ekliyoruz.
    4. Aşama 2'de bahsettiğimiz tekerlekler gibi "fixed" olmayan jointler için transmission eklememiz gerekiyor. Her bir tekerleğe transmission ekliyoruz.
    5. Oluşturduğumuz control paketi içerisine config dizini oluşturuyoruz. Daha sonra bu dizine joint controller'larımız için bazı parametreler ekleyeceğiz. (Burayı araştır, kendin yap)
       1. Bu yaml dosyasını launch dosyasında çağıracağız.
       2. Joint_state_controller, position_controller, velocity_controller başlıklarını araştır.
    6. Launch dosyasında controller'ı ekliyoruz.
    7. Robot_state_publisher'ı launch dosyasında çağırıyoruz.
       1. Bu node tüm linkleri TF ile paylaşıyor.
    8. Bu aşamaları uygularken birçok hata ile karşılaşabilirsiniz. Bu hataları tek tek internetten araştırmak gerekiyor. Yukarıdaki aşamalar bittikten sonra hata almıyorsanız controller paketinin paylaştığı topicler aracılığıyla tekerlekleri hareket ettirin. Bu hareketi gördükten sonra diğer aşamaları uygulamaya devam edin.
    9. Tekerlekleri düz bir şekilde hareket ettirdikten sonra sırada direksiyon var. Direksiyon için aracın ön tekerleklerini iki eksende döndürmemiz gerekir. Birincisini zaten yapmıştık, düz giderkenki dönüşü, ikincisi ise direksiyon kırdığımızda tekerlerin z eksenindeki hareketini sağlamak için.
       1.  Tekerleri yana doğru hareket ettirebilmek için aracın base'i (bizim modelimizde base_link) ile teker arasına bir link daha eklemek gerekiyor. Eklediğimiz link sadece z ekseninde yani yanlara doğru dönebilir olmalı. Tekerleği de artık base_link yerine bu linke bağlıyoruz (bağlama şeklimiz aynı, arka tekerler gibi sadece düz şekilde ileri doğru dönebiliyor.)
       2.  Bu jointler için yeni controller'lar eklememiz gerekiyor (önceki eklediklerimiz aynen duracak, direksiyon için yeni ekleme yapacağız). Yaml dosyasına direksiyon controller'larını da ekliyoruz. 
   1.  Simülasyonda tekerleklerin yeni oluşturduğumuz controller'lar ile yanlara döndüğünü görünce bu aşamayı tamamlamış bulunuyoruz.

* ### NOT: Bu aşamada anlatılanlar sadece yol gösterici, aşamayı geçmek için internetten araştırmanız gerekecektir. İnsanların yazdığı hazır kodları incelemek faydalı olur. Takıldığınız yerlerde yine GAT2 repo'sundan bizim nasıl yaptığımıza bakabilirsiniz. 

* ### Anahtar Kelimeler:
  * ros-controllers
  * gazebo_ros_control
  * transmission
  * joint_controller
    * joint_state_controller
    * position controller
    * velocity controller
  * Robot_state_publisher
  * TF
