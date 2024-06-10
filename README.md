# Cizgi-izleyen-robot 
KULLANILAN PARCALAR 
    1-Arduino Uno R3
    2-L298 Motor Sürücüsü
    3-Hazır Araç Platformu
    4-Pil
    5-Motor
    6-Çizgi Takip Sensörü
    7-Dönüştürücü
    8-Jumper Kablo

Devre Şeması ve Çalışma Düzeni

   -  Arduino Uno: Projeyin kontrolünü sağlar ve sensörlerden gelen verileri işler.
   -  L298 Motor Sürücüsü: Motorlara güç sağlar ve yönlendirme işlemlerini gerçekleştirir.
   -  Sensörler: Zemin üzerindeki çizgiyi algılar ve Arduino'ya bu bilgiyi iletir.
   -  Motorlar: Arduino ve motor sürücü aracılığıyla kontrol edilir ve çizgiyi takip etmek için hareket eder.

   Çizgiyi Takip Etme Olayı
Çizgi takibi için kullanılan sensör sayesinde toplanan verilere göre bir dizi işlem uygulanır. Projede 3 tane kontrast farkını algılayan ve farka göre 0 veya 1 değeri dönderen sensör bulunmaktadır. Bu sensörlerden gelen 0 ve 1 verilerine göre robotun hangi tarafında çizginin olduğunu anlayabiliyoruz. Bu 3 sensör sağ-sol-orta olacak şekilde tanımlanır. Örneğin sağ sensör eğer bir çizgi tespit ederse 1 değerini dönderir. Gelen bu 1 değeri işlenemden önce diğer sensörlerden gelen değerlerde kontrol edilir. Eğer diğer sensörlerden de 0 değeri geliyorsa, çizginin sağ tarafta olduğuna emin oluruz. Daha sonra sağ tarafta kalan çizgiyi takip edebilmek için motorlara hareket değişikliği yapmasını söyleriz. Robotun ilerleyiş yönündeki sağ tarafında çizgi varsa o çizgiyi takip edebilmesi için saü motorun durması/hızının yavaşlaması ve sol motorun harekete devam etmesi/hızlanması gerekir. Bu şekilde orta sensörden 1 değeri gelinceye yani çizginin tam üzerinde olduğunu anlayıncaya kadar devam eder ve tekrar çizgiden çıkması durumunda bu döngü devam eder

![resim](https://github.com/INEXUSS/Cizgi-izleyen-robot/assets/115108092/c019c184-7800-4980-a231-27640ea3d4e9)
