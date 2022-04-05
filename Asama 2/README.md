# Ros-egitim-serisi
## Aşama 2 - Model oluşturma

* ### Hedef: Bu aşamada hedefimiz simülasyon boyunca kullanabilinecek bir model oluşturmak. Bir sonraki aşamada oluşturduğumuz modeli kontrol edeceğiz. 

* ### Seri boyunca verilen görevleri nasıl yapacağınızı internetten araştırmanız beklenmektedir. Takıldığınız yerlerde GAT2 repo'sundan yardım alabilirsiniz.

* ### Bu aşamada yapılması gerekenler: 
    1. Linkler ve Jointler hakkında araştırma yapılacak.
    2. Aşama 1'de oluşturduğumuz küp modeli daha gerçekçi bir model haline getirmek. 
       1. Yeni modelin 4 tekerlekli bir araba olması yarışmaya uygunluğu açısından iyi olur. 
       2. Oluşturacağımız aracın ölçülerini xacro değişkenlerine atamak ileride kolaylık sağlayacaktır.
       3. Tekerleklerin dönebilmesi için joint tipini sabit jointlerden farklı yapmanız gerekiyor. Araştır.
          1. Burada tekerleklerin joint tipini değiştirirseniz model yüklenirken hata ile karşılaşabilirsiniz. Bunun için modele transmission eklemek gerekiyor. Bir sonraki aşamada eklememiz gerekecek, isterseniz şimdiden araştırabilirsiniz.
       4. İsteğe bağlı: oluşturduğunuz modeli renklendirmek için urdf dosyasına material eklemeyi araştırabilirsiniz.
    3. Oluşturduğunuz araba modelini Gazebo'ya eklediğinizde bir sonraki aşamaya geçebilirsiniz.


* ### Anahtar Kelimeler:
  * Xacro
  * URDF
  * Link, joint, material
  * Joint types
