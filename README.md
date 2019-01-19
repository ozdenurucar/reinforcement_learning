# ROS ve Gazebo ile Pekiştirmeli Öğrenme

![](https://github.com/ozdenurucar/reinforcement_learning/blob/master/Resimler/rl.png)



OpenAI Gym, son zamanlarda makine öğrenmesi topluluğunda popülerlik kazanmış pekiştirmeli öğrenme araştırmaları için bir araçtır. OpenAI Gym, her bölümdeki toplam ödül beklentisini en üst seviyeye çıkarmayı ve mümkün olduğunca hızlı bir şekilde kabul edilebilir bir performans seviyesi elde etmeyi amaçlayan, epizodik RL'ye odaklanır. Bu araç seti Gym API'sini robotik donanıma entegre etmeyi ve gerçek ortamlarda donatı öğrenme algoritmalarını doğrulamayı amaçlamaktadır. 3D modelleme ve görüntü oluşturma aracı olan Gazebo simülatörü, yazılım geliştiricilerin robot uygulamaları oluşturmasına yardımcı olan bir dizi kitaplık ve araç olan Robot İşletim Sistemi ile birleştirilerek gerçek dünyaya ulaşıldı. 

Daha önce de tartışıldığı gibi, robotikteki RL ile ilgili temel problem, sadece ekonomik maliyet değil aynı zamanda öğrenme işlemlerini gerçekleştirmek için gereken uzun süre olan deneme başına yüksek maliyettir. Bilinen bir başka husus, gerçek bir ortamda gerçek bir robotla öğrenmenin, özellikle quadcopters gibi uçan robotlarla tehlikeli olabileceğidir. Bu zorlukların üstesinden gelmek için, maliyet tasarrufu, zaman tasarrufu ve simülasyonu hızlandırmaya yardımcı olan Gazebo gibi gelişmiş robotik simülatörler geliştirilmiştir.
