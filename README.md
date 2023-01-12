# 102.-Binary-Tree-Level-Order-Traversa
102. İkili Ağaç Düzeyinde Sipariş Geçişi

İkili bir ağacın kökü verildiğinde, düğümlerinin değerlerinin seviye sırası geçişini döndürün. (yani, soldan sağa, seviye seviye).

![image](https://user-images.githubusercontent.com/77336040/212174051-1e6360af-f237-414c-8588-bf65ecf2ded3.png)


Breadth First Search mantığı 
Genişliğin öncelik alındığı graph algoritmasıdır. Bir root seçildikten sonra alt çocuk düğümlere (children node) geçilir. Daha sonra da bir alt çoçuk düğümlere(children node) geçilir. Root ve alt düğümler birer leveldir.
Kuyruk(Queue) veri yapısını kullanır.(FIFO ilk giren ilk çıkar)
Her düğüm en az bir kez gezildiğinden karmaşıklık O(N)'dir.

--------------
Bu soruda bizden levelleri liste yapısıyla sınıflandırılmış halini göstermemizi istiyor. Bunun için  sonucu göstermede ans=[]'i kullaırken level'leri göstermek için currLevel=[] kullanacağız. Döngü ile ilerlerken düğüm değerlerini currLevel'e eklerken ( node = q.popleft()) ile her levele geçtiğinde currLevel'i ans=[]'e ekleyeceğiz.
