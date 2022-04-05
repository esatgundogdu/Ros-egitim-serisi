# Ros-egitim-serisi
## Aşama 1 - Gazebo'ya giriş

* ### Hedef: Bu aşamada hedefimiz ROS aracılığıyla Gazebo'ya model eklemek.

* #### Seri boyunca verilen görevleri nasıl yapacağınızı internetten araştırmanız beklenmektedir. Takıldığınız yerlerde GAT2 repo'sundan yardım alabilirsiniz.

* ### Bu aşamada yapılması gerekenler: 
  1. Workspace'inizde Gazebo için yeni bir paket oluşturmak. Gazebo için yazdığımız launch dosyaları, node'lar vs. bu paket içinde olacak. Paket isimlendirmeleri için "<workspace_ismi>_<paket_ismi>" formatında yazmak ileride paketleri karıştırmamak açısından faydalı oluyor (bizim repo'muzda da isimlendirmeler bu şekilde). Bu aşamada paket ismi "<workspace_ismi>_gazebo" olabilir.
  2. Paketlerin içine yazacağımız ".launch" dosyaları için "launch" isminde bir dizin oluşturuyoruz. Buraya ilk launch dosyamızı ekleyeceğiz.
  3. Öncelikle launch dosyasında gazebo_ros paketinden "empty_world" dosyasını çağırarak boş bir dünya oluşturuyoruz.
     1. Bu gibi aşamaların hepsini birden yapmak yerine teker teker yapıp denemek faydalı olacaktır.
  4. Daha sonra ilk modeli oluşturmak için workspace'de yeni bir paket oluşturuyoruz.
     1. Örnek isim "<workspace_ismi>_description" olabilir. 
     2. Paket içerisine urdf dosyaları için "urdf" isminde bir dizin oluşturuyoruz. Bu dizin içerisinde ilk urdf dosyamızı oluşturuyoruz.
        1. URDF dosyasını xacro ile olusturmak onemli, bircok konuda fayda sagliyor.
  5. URDF dosyasında bir küp oluşturuyoruz. (Bu aşamalarda internetten araştırmak ve GAT2 reposundan faydalanmak gerekebilir.)
  6. Oluşturduğumuz modeli gazebo paketindeki launch dosyası içerisinde simülasyona ekliyoruz.
     1. Burada "spawn_model" node'unu kullanıyoruz, daha sonrasında "robot_description" paylaşıyoruz. (Bu isimleri aşağıdaki anahtar kelimeler bölümüne ekledim, internetten bunların kullanımını araştırırsanız kolaylıkla bulabilirsiniz.)
  7. Oluşturduğumuz küp model simülasyona eklendiyse bu aşama tamamlanmış demektir. Bir sonraki aşamaya geçebilirsiniz.


* ### Anahtar Kelimeler (İnternetten araştırma yaparken bunları kullanmak işinizi kolaylaştırır):
  * Launch file
  * URDF file
  * xacro
  * gazebo_ros, empty_world
  * spawn_model
  * robot_description