# AzureServiceBusAsyncCacher

Azure Service Bus kuyruklarının temel avantajları şunlardır:

İleti başına 256 KB (standart katman) veya 1 MB (premium katman) olmak üzere daha büyük ileti boyutunu destekler (64 KB yerine)
En az bir kez ve en çok bir kez teslimi destekler. İletinin kaybolma veya iki kez işlenme ihtimali arasında seçim yapmanız gerekir ve bu iki ihtimal de oldukça düşüktür
İlk giren ilk çıkar (FIFO) sıralamasını garanti eder. İletiler eklendikleri sırayla işlenir (FIFO kuyruğun normal çalışma şekli olsa da her ileti için garanti edilmez)
Birden fazla ileti tek bir işlemde gruplandırılabilir. İşlemdeki iletilerden biri teslim edilemezse diğerleri de teslim edilemez
Rol tabanlı güvenliği destekler
Hedef bileşenlerin kuyruğu sürekli yoklaması gerekmez

Aşağıdaki durumlarda Service Bus kuyruklarını kullanın:
En çok bir kez teslim garantisine ihtiyacınız var
FIFO garantisine ihtiyacınız var
İletilerin işlemler içinde gruplandırılmasına ihtiyacınız var
Kuyruğu yoklamadan iletileri almak istiyorsunuz
Kuyruklara rol tabanlı erişim sağlamanız gerekiyor
64 KB'tan büyük ama 256 KB'tan küçük iletileri işlemeniz gerekiyor
Kuyruk boyutunuz 80 GB'ın üzerine çıkmayacaktır
İletileri toplu halde yayımlayabilmek ve kullanabilmek istersiniz
