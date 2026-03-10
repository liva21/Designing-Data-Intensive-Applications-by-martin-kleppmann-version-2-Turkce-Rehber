# 🗄️ Designing Data-Intensive Applications — Türkçe Notlar

**Martin Kleppmann**'ın yazılım dünyasının en önemli kitaplarından biri olan  
*Designing Data-Intensive Applications (2. Baskı)*'ı baştan sona okudum  
ve her bölümü kendi anladığım şekliyle Türkçeye aktardım.

---

## 🔥 Neden Bu Repoyu Oluşturdum?

Bu kitabı okumaya başladığımda fark ettim ki içerik inanılmaz derinlikli —  
distributed systems, replication, consensus, stream processing…  
Sadece okumak yetmiyordu, gerçekten *anlayıp içselleştirmem* gerekiyordu.

Türkçe kaynak neredeyse yok. Varolan çeviriler ya çok yüzeysel  
ya da teknik terimleri öylesine Türkçeleştirmiş ki tanıyamıyorsun.

Bu yüzden kendi notlarımı oluşturmaya karar verdim:  
**Terimler İngilizce kalsın, açıklamalar Türkçe olsun.**  
Okuyan biri hem kavramı anlasın hem de İngilizce teknik dili öğrensin.

Eğer sen de bu kitapla boğuşuyorsan, bu notlar sana zaman kazandırabilir.  
Eğer kitabı zaten okuduysan, farklı bir bakış açısı sunabilir.  
Her iki durumda da umarım işine yarar. 🚀

---

## 📂 İçerik

```
📁 repo/
│
├── 📘 Bölüm 1  — Reliable, Scalable, and Maintainable Applications
├── 📘 Bölüm 2  — Data Models and Query Languages
├── 📘 Bölüm 3  — Storage and Retrieval
├── 📘 Bölüm 4  — Encoding and Evolution
├── 📘 Bölüm 5  — Replication
├── 📘 Bölüm 6  — Partitioning
├── 📘 Bölüm 7  — Transactions
├── 📘 Bölüm 8  — The Trouble with Distributed Systems
├── 📘 Bölüm 9  — Consistency and Consensus
├── 📘 Bölüm 10 — Batch Processing
├── 📘 Bölüm 11 — Stream Processing
└── 📘 Bölüm 12 — The Future of Data Systems
```

---

## 🗂️ Bölüm Bazında Konu Özeti

### Bölüm 1 — Reliable, Scalable, and Maintainable Applications
Veri yoğun uygulamaların üç temel hedefi: **Reliability** (güvenilirlik), **Scalability** (ölçeklenebilirlik) ve **Maintainability** (sürdürülebilirlik). Fault ile failure arasındaki fark, load ve performance nasıl ölçülür, Twitter'ın fan-out problemi üzerinden gerçek dünya tasarım kararları.

### Bölüm 2 — Data Models and Query Languages
İlişkisel model (SQL) vs. doküman modeli (NoSQL) vs. graf modeli. Her birinin güçlü olduğu yerler ve tradeoff'lar. MapReduce, Datalog ve deklaratif vs. imperatif sorgulama dilleri arasındaki felsefe farkı.

### Bölüm 3 — Storage and Retrieval
Veritabanının içinde neler oluyor? Log-structured storage (LSM-Tree, SSTables, Bloom Filters) ile B-Tree arasındaki mimari fark. OLTP vs. OLAP ayrımı, column-oriented storage ve veri ambarı tasarımı.

### Bölüm 4 — Encoding and Evolution
Veri formatları: JSON, XML, Protobuf, Thrift, Avro. Schema evrimi sırasında geriye/ileriye dönük uyumluluk (backward/forward compatibility) nasıl sağlanır? Servisler arası iletişimde REST, RPC ve mesaj kuyrukları.

### Bölüm 5 — Replication
Aynı veriyi birden fazla node'da tutmanın yolları: **Single-leader**, **multi-leader** ve **leaderless** replikasyon. Replication lag neden olur, eventual consistency ne demektir, read-your-writes ve monotonic reads garantileri nedir.

### Bölüm 6 — Partitioning (Sharding)
Büyük veriyi node'lara bölme stratejileri: key-range vs. hash partitioning. Secondary index'lerde scatter/gather problemi, rebalancing ile hot spot yönetimi. Partitioning + replication kombinasyonu.

### Bölüm 7 — Transactions
ACID garantileri gerçekte ne anlama gelir? Read committed, snapshot isolation (MVCC), serializability. Dirty read, nonrepeatable read, phantom read ve write skew anomalileri. Two-phase locking (2PL) ve serializable snapshot isolation (SSI).

### Bölüm 8 — The Trouble with Distributed Systems
Dağıtık sistemlerin acımasız gerçekleri: unreliable networks, unreliable clocks, process pauses (GC stop-the-world!). Byzantine fault nedir, truth sadece çoğunluğun kararıyla mı belirlenir? Sistemlerin neden bu kadar belirsiz (nondeterministic) olduğu.

### Bölüm 9 — Consistency and Consensus
Linearizability nedir ve neden bu kadar pahalıdır? CAP teoremi — gerçekte ne söylüyor, ne söylemiyor? Total order broadcast, 2PC (two-phase commit) ve distributed transactions. **Raft** ve **Paxos** algoritmalarının temel fikri ve ZooKeeper'ın bu dünyadaki rolü.

### Bölüm 10 — Batch Processing
Unix felsefesi ve MapReduce arasındaki derin bağ. Hadoop ekosistemi, join stratejileri (sort-merge join, broadcast hash join), dataflow motorları (Spark, Flink, Tez) ve neden MapReduce'un yerini aldılar.

### Bölüm 11 — Stream Processing
Event streams, message brokers (Kafka, RabbitMQ) ve log-based messaging. Stream-stream join, stream-table join, windowing. **Exactly-once semantics** neden bu kadar zor? Microbatching vs. gerçek stream processing farkı.

### Bölüm 12 — The Future of Data Systems
Lambda ve Kappa mimarileri. Unbundling databases fikri: verinin tek bir sistemde değil, özelleşmiş araçların kompozisyonuyla işlenmesi. Veri sistemlerinde doğruluk, gizlilik ve etik sorumluluk.

---

## 🛠️ Nasıl Kullanılır?

### Doğrudan GitHub'da Oku
Her notebook GitHub üzerinde render edilir — herhangi bir kurulum gerekmez, tarayıcıdan okuyabilirsin.

### Yerel Ortamda Çalıştır

```bash
# Repoyu klonla
git clone <repo-url>
cd <klasör-adı>

# Jupyter Notebook başlat
jupyter notebook
```

> Jupyter kurulu değilse: `pip install notebook`

### Google Colab'da Aç
Her notebook'un en üstünde Colab bağlantısı bulunuyor — tek tıkla açıp çalıştırabilirsin.

---

## 🤝 Katkı

Yanlış anladığım bir kavram mı var? Eksik bıraktığım bir konu mu?  
**Issue aç veya pull request gönder** — her türlü katkıya açığım.

Bu notlar "bir kişinin anlayışı" — farklı bakış açıları sadece zenginleştirir.

---

## 📖 Orijinal Kaynak

> **Designing Data-Intensive Applications**, 2. Baskı  
> Yazar: Martin Kleppmann  
> Yayınevi: O'Reilly Media  
> 🔗 [dataintensive.net](https://dataintensive.net)

Bu repo orijinal kitabın bir çevirisi değil, okuma notlarından oluşan  
**kişisel bir öğrenme kaynağıdır**. Tüm haklar Martin Kleppmann'a aittir.  
Kitabı satın alarak desteklemenizi öneririm — her sayfasına değer.

---

## ⭐ Destek

Notlar işine yaradıysa repoya **star** atarsan sevinirim.  
Başkalarının da bulmasına yardımcı olur.

---

<p align="center">
  Dağıtık sistemleri anlamak isteyenler için ❤️ ile hazırlandı
</p>
