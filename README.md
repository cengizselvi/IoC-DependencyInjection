```
Inversion of Control (IoC)
Dependency Injection 
@Component
@RestController 
@Autowired
@Qualifier
@Primary
@Lazy
```


**Inversion of Control (IoC)**, yazılım tasarımında bir bileşenin kontrolünü başka bir bileşene devretme prensibidir. Geleneksel tasarımlarda bir bileşen diğer bileşenleri doğrudan yaratır ve kontrolünü elinde tutar, ancak IoC ile kontrol tersine çevrilir. Bağımlılık Enjeksiyonu (Dependency Injection) adı verilen bir tasarım kalıbı ile ilişkilendirilen IoC, bir bileşene gerektiği diğer bağımlı bileşenleri dışarıdan vererek bağımlılıkları gevşetir. Bu sayede bileşenlerin test edilmesi, değiştirilmesi ve tekrar kullanılması kolaylaşır. IoC prensibi, yazılımın esnek, yeniden kullanılabilir ve test edilebilir olmasını sağlar. Ayrıca bileşenlerin daha iyi organize edilmesine ve sürdürülebilir bir kod tabanının oluşturulmasına da yardımcı olur.IoC tamamen kontrolü tersine çevirmekle ilgilidir. Bunu meslekten olmayanların terimleriyle açıklamak için, iş yerinize arabayla gittiğinizi varsayalım. Bu, arabayı kontrol ettiğiniz anlamına gelir. IoC ilkesi, kontrolü tersine çevirmeyi önerir, yani arabayı kendiniz sürmek yerine, başka birinin arabayı kullanacağı bir taksi kiralarsınız. Bu nedenle, kontrolün tersine çevrilmesi denir - sizden taksi sürücüsüne. Kendiniz araba kullanmak zorunda değilsiniz ve asıl işinize odaklanabilmeniz için arabayı sürücünün kullanmasına izin verebilirsiniz.

**Dependency Injection** (Bağımlılık Enjeksiyonu), bir bileşenin ihtiyaç duyduğu diğer bileşenleri dışarıdan alarak kullanma prensibidir. Böylece bağımlı bileşenler arasındaki sıkı bağlantılar gevşer, esneklik, test edilebilirlik ve sürdürülebilirlik sağlanır. genellikle bir arayüz (interface) veya bir soyutlama (abstract class) üzerinden tanımlanır. Ardından, bu bağımlılıkların bir başka bileşen tarafından dışarıdan sağlanması ve enjekte edilmesi sağlanır. Böylece, bileşenin bu bağımlılıklara erişimi ve kullanımı mümkün olur.

**"@Component"** genellikle bir Java Spring Framework terimidir ve bir sınıfın bir bileşen olduğunu belirtmek için kullanılır. Bu anotasyon, Spring konteynerine bir sınıfın bir bileşen olarak yönetilmesini sağlar. @Component anotasyonu, bir sınıfın Spring konteyneri tarafından yönetilen bir bileşen olduğunu belirtir. Bu anotasyon, Spring tarafından taranarak bileşenin otomatik olarak oluşturulmasını sağlar. Spring uygulamasının çalışması sırasında, @Component anotasyonuna sahip sınıfların örnekleri oluşturulur ve Spring konteyneri tarafından yönetilir.

**@RestController** anotasyonu, bir sınıfın HTTP isteklerini karşılamak ve HTTP yanıtlarını oluşturmak için kullanılan bir Controller sınıfı olduğunu belirtir. Özetlemek gerekirse, @RestController anotasyonu, Spring Framework içinde bir Controller bileşeninin RESTful web hizmetleri sağlayan bir sınıf olduğunu belirtmek için kullanılır.

**@Autowired**, Java Spring Framework'te kullanılan bir anotasyondur. Bu anotasyon, bağımlılık enjeksiyonunu gerçekleştirmek için kullanılır. Bir sınıfın belirli bir bağımlılığı olduğunda, @Autowired anotasyonu ile bu bağımlılığın otomatik olarak enjekte edilmesi sağlanır.@Autowired anotasyonu, Spring Framework tarafından yönetilen bir sınıfın (bean) başka bir sınıfa bağımlı olduğunu belirtmek için kullanılır. Bu anotasyonu kullanarak, bağımlı nesneleri otomatik olarak oluşturabilir ve enjekte edebilirsiniz.


**Bean Nedir ?**
Spring Framework uygulamamızın omurgasını oluşturan ve Spring IOC container tarafından yönetilen nesnelere BEAN denir. Yeniden kullanılabilir objeler olarak kabul edebiliriz.

**@Qualifier** - Hem @Qualifier hem de @Primary  mevcutsa, @Qualifier ilk  önceliğe sahiptir. 
**@Qualifier kullanımı-> public DemoController(@Qualifier("cricketCoach") Coach theCoach) {}

**@Primary**- aynı türden birden fazla bean olduğunda bir bean'e daha yüksek tercih vermek için kullanırız  .

**@Lazy** – ihtiyaç duyulmadığı sürece hiçbir bean oluşturulmaz

spring.main.lazy-initialization=true // global olarak tanımlama (application.properties)

