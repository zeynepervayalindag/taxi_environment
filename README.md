# taxi_environment
BLM5027 Derin Pekiştirmeli Öğrenme dersi kapsamında öğrenme algoritmaları ile ortamlar arasında iletişim kurmak için standart bir API olan ve bu API'ye uygun standart bir ortam seti sunarak pekiştirme öğrenme algoritmaları geliştirmek ve karşılaştırmak için açık kaynaklı bir Python kütüphanesi olan OpenAI Gym Taxi-v3 çevresinden yararlanılarak kendi environmentimizi oluşturduğumuz Q-Learning tabanlı otonom taxi uygulaması. Standart OpenAI Taxi ortamından farklı olarak özelleştirilmiş 6x6 grid tabanlı çevre (environment) kullanılmıştır. Bu ortamda:
  Harita kaldırımlar yerine labirent benzeri olmayan duvarlar ile sınırlandırılmış alanlardan oluşur.
  Taksi harita üzerinde hareket ederken beş farklı varış (drop-off) noktasından birine yolcuyu ulaştırmakla görevlidir.
  Harita içerisinde bazı hücreler "yasak bölge" olarak tanımlanmıştır. Bu hücreler:
    Kırmızı renkle işaretlidir,
    Varış noktası değildir,
    Taksi bu hücrelere giremez.
  Q-Learning Yapısı
    Proje Q-Learning algoritmasını temel alır ve şu özellikleri içerir:
      Simülasyon sırasında oluşturulan Q-Tablosu, eğitim sonunda dosyaya kaydedilir.
  Kullanıcı isterse:
    Eğitim aşamasını atlayarak önceden kaydedilen Q tablosunu yükleyebilir,
    Böylece taksi doğrudan öğrenilmiş en iyi davranış modeliyle çalışabilir.
  Eğitim sürecinde:
    Toplam ödül, kaç denemenin başarısız olduğu, adım sayıları gibi performans metrikleri izlenir ve en iyi model bulunur.
<img width="592" height="455" alt="indir" src="https://github.com/user-attachments/assets/146c0cea-d9b4-4d89-9aaf-40a4de8c5049" />
<img width="580" height="455" alt="indir (1)" src="https://github.com/user-attachments/assets/da236397-e007-47dd-aadd-b9e96d27e64b" />


Bu not defteri oluşturulurken aşağıdaki kaynaklar kullanılmıştır:

        [1] A Q-learning implementation for OpenAIs Taxi-v3 environment
          https://github.com/woutervanheeswijk/taxi_environment
          
        [2] OpenAI Gym. Taxi-v3 ortamı. OpenAI Gym ortamı MIT Lisansı altında mevcuttur.
          https://github.com/openai/gym/blob/master/gym/envs/toy_text/taxi.py
          
        [3] LearnDataSci. OpenAI Gym ile Python'da Sıfırdan Takviyeli Q-Öğrenme. Taxi-v2 uygulaması.
          https://www.learndatasci.com/tutorials/reinforcement-q-learning-scratch-python-openai-gym/
          
        [4] Botforge. OpenAI Gym render'larını GIF olarak kaydedin. Herkese açık GitHub Gist.
          https://gist.github.com/botforge/64cbb71780e6208172bbf03cd9293553
