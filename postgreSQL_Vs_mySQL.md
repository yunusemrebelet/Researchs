# MySQL vs PostgreSQL

## Açık Kaynak

PostgreSQL, çeşitli şirketler ve bireysel katılımcılar grubu olan PostgreSQL Global Development Group tarafından geliştirilmiştir.

Ücretsiz ve açık kaynaklı bir veritabanıdır. PostgreSQL, BSD veya MIT lisanslarına benzer bir liberal Açık Kaynak lisansı olan PostgreSQL lisansı altında yayınlanmaktadır.

MySQL, kaynak kodunu, çeşitli özel anlaşmaların yanı sıra GNU Genel Kamu Lisansı şartlarına uygun hale getirmiştir.

Şu anda Oracle Corporation’a aittir, açık kaynaklı veritabanıdır ama tescilli kullanım için çeşitli ücretli sürümler de sunmaktadır.

## ACID

ACID, veritabanı işlemlerinin bir özellik kümesidir. ACID uyumluluğu, tek bir işlem sırasında çok sayıda değişiklik yapıldığında bile, olası arıza durumunda sistemde hiçbir verinin kaybolmamasını ve yanlış iletişim yapılmamasını sağlar.

Atomicity, Consistency, Isolation, Durability

**Atomicity(Bütünlük):** İşlemler veri tabanı taradından bir bütün olarak ele alınmalıdır. Yapılan işlem herhangi bir kesintiye uğradığında tüm işlemler geçersiz sayılır.

PostgreSQL, ACID ile uyumludur ve tüm gereksinimlerin karşılanmasını sağlar.

MySQL, sadece InnoDB ve NDB Cluster Storage motorlarını kullanırken ACID uyumludur.

## SQL Uyumluluğu

SQL uyumluluğuna sahip olmak, verileri bir SQL uyumlu veritabanından diğerine (ör. Oracle’dan PostgreSQL veya SQL Server’a) taşımayı çok kolaylaştırır.

PostgreSQL büyük ölçüde SQL uyumludur. Her bir özellik için uygunluk seviyesi, resmi dökümantasyonun Ek D’sinde açıkça belirtilmiştir ve herhangi bir sapma, PostgreSQL kılavuzunun “Referans” bölümünde açıkça belgelenmiştir.

PostgreSQL, SQL’in önemli özelliklerinin çoğunu destekler: 2011. Tam Çekirdek uyumluluğu için gerekli olan 179 zorunlu özellik arasından, PostgreSQL en az 160’ı ile uyumludur.

MySQL, bazı sürümlerde kısmen uyumludur (örn. CHECK kısıtlamalarını desteklemez).

## Performans

MySQL, sadece basit veri işlemleri için bir veri tabanına ihtiyaç duyan web tabanlı projeler için yaygın olarak kullanılmaktadır. Dolayısıyla, MySQL’e ağır bir yük yüklendiğinde ya da karmaşık sorguları tamamlamaya çalışırken düşük performans göstermesi olasıdır.

PostgreSQL ise çoğunlukla büyük veritabanlarına ihtiyaç duyulan, yazma ve okuma hızının önemli olduğu projelerde kullanılır. Genel olarak, PostgreSQL performansı, karmaşık sorguların yürütülmesini gerektiren sistemlerde en iyi şekilde kullanılır.

## NoSQL Özellikleri / JSON Desteği

PostgreSQL, yerel XML desteği ve HSTORE ile anahtar / değer çiftleri gibi JSON ve diğer NoSQL özelliklerini destekler. Ayrıca daha hızlı erişim için JSON verilerini indekslemeyi de destekler.

MySQL’in JSON veri türü desteği vardır, ancak başka bir NoSQL özelliği yoktur. JSON için indekslemeyi desteklemez.

## Programlama Dilleri Desteği

PostgreSQL, C / C ++, Java, JavaScript, .Net, PHP, R, Perl, Python, Ruby, Tcl ve diğerleri dahil olmak üzere çok çeşitli programlama dillerini destekler; Kullanıcı tarafından sağlanan kodu ayrı süreçlerde çalıştırmak (hatta arka plan çalışanları olarak çalışmak) bile mümkündür.

MySQL Sunucu taraflı (Server Side) programlama dillerinde kullanılabilir.

## Postgres'in MySQL'e göre avantajları

Postgres object-relational database iken MySQL sadece relational-databasedir. Bu şu anlama gelmektedir:
Postgres table inheritance [table inheritance](https://dzone.com/articles/table-inheritance-whats-it-good-for), function overloading(Yazılımcıya birden fazla aynı adda fonksiyon tanımlamaya fakat farklı parametreler vermesine izin verir) [function overloading](https://beginnersbook.com/2017/08/cpp-function-overloading/) gibi özellikleri barındırmaktadır.
