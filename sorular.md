## Araştırma Soruları

Şimdi görevi gerçekleştirmek için hazırsınız. Şimdi biraz daha kullandığımız araçları anlama zamanı. Bu dokümanı güncelleyerek, aşağıdaki soruları cevaplayınız. Git'e biraz daha aşina olmaya başladığınızı göreceksiniz. 

Soruları cevaplamak için [GitHub docs](https://docs.github.com/en)'u kullanabilirsiniz. Docs, (ingilizce documentation'ın kısaltılmış halidir) bir programı veya dilin nasıl kullanılacağını anlatan dokümandır. Yazılım dünyasında sıkça kullanılır. Bir yazılımcı olarak zamanınızın büyük çoğunluğu da bu tarz dokümanları okumakla ve üzerinde çalışmakla geçer.

Eğer aradığınız soruların cevapları GitHub docs'ta yok ise Google'lama becerileriniz size yardımcı olacaktır :)


1. Git nedir?
Git, yazılım geliştirme süreçlerinde kullanılan, hız odaklı, dağıtık çalışan bir sürüm kontrol ve kaynak kod yönetim sistemidir. Yazdığımız projelerini internet üzerinde tutmamızı ve yönetmemizi sağlayan bir sistemdir. Git sayesinde yaptığımız projelerin adım adım versiyonlarının kopyalarını alarak daha sonra ihtiyaç duyduğumuzda aldığımız kopyalara yani versiyonlara kolayca dönebiliyoruz. 

2. Git ile GitHub arasında ne fark var?
Github, dünyanın en büyük geliştirici topluluklarından birisi olup, git versiyon kontrol sistemini kullanarak yazılım geliştirme projeleri için web tabanlı bir bulut depolama servisidir.
Github yazılım geliştiricileri için bir sosyal ağ platformudur. Github sayesinde, yazılım geliştiriciler, kendileri gibi yazılımla uğraşan kişilerin projelerine göz atabilir onları takip edebilirler.
Bir de projeyi birden fazla kişi yapıyorsa bu yapılanlar nasıl birleştirilecek diye düşünürsek Git bu konuda hayatımızı ciddi anlamda kolaylaştırmıştır. Github ise projelerimizin saklandığı (depolandığı) uzak sunucudur.

3. Neden bir branch oluşturuyoruz? 
Kullanıcı, projesine bir yenilik eklemek istediğinde, yaptığı değişiklik projenin çalışmasını olumsuz etkileyebilir. Bu gibi durumlarda projemizin o anki halini bozmamak için branch kullanabiliriz. Branch yardımı ile projemizin çalışır halini kaydedip, yeni eklenti üzerinde rahatlıkla çalışabiliriz. Projemizde herhangi bir sorun çıktığı takdirde geri dönüp önceki versiyona kolaylıkla erişebiliriz. Branch, projemizi değiştirirken ya da güncellerken eski halini koruyoruz ve projemize bir versiyon çıkarttığımız zaman her yeni versiyon için repository oluşturmak yerine her bir versiyon için farklı branchler açabiliyoruz. Böylece versiyonları bir arada kolayca takip edebilir ve erişebilmemizi sağlıyor.

4. Pull Request'in amacı nedir?
Pull request olarak göndermenin amacı; proje üzerinde değişiklik yaptım, sen de bu değişiklikleri onaylarak projene merge et demek anlamına gelir.
Bazı değişiklikleri yaptıktan sonra, bir pull request talebinde bulunarak bu kodu bir şubeye geri gönderebiliriz. Pull request talebi, temelde branch’dan sorumlu kişiden kodunuzu eklemesini istemektir. Ayrıca o kişinin kodda tam olarak neyi değiştirdiğimizi görmesine de yardımcı olur.

5. Bir Branchten diğerine geçmek için kullanıdığımız KOMUT nedir? Örneğin ADINIZ-SOYADINIZ branch'inde çalıştığınızı hayal edin ve main branch'ine geçmek istiyorsunuz.
git checkout main

6. `git fetch`, `git merge` ve `git pull` arasındaki farklıarı açıklayınız. Bu konutlar ne yapar açıklayınız.
"git fetch" Komutu: 
fetch kullandığınızda, Git, hedef branchteki bulunan ve mevcut branchte bulunmayan herhangi bir commit işlemini yapar ve yerel reponuza kaydeder. Ancak, bunları mevcut branchiniz ile birleştirmez. Peki git fetch ne işe yarar? Repomuzu güncel tutmamız gerekiyorsa, ancak dosyalarımızı güncellersek de bozulabilecek bir şeyler varsa fetch kullanmayı tercih ederiz. Bu işlemleri mevcut branchinize entegre etmek için sonrasında merge kullanmalısınız.
"git merge" Komutu: 
Üzerinde çalışmış olduğunuz iki parçayı birleştirme işlemini gerçekleştirir. Git'de merge işlemi başka bir branch'deki değişiklikleri üzerinde çalıştığınız kendi branch'inize entegre etme işlemidir. Git merge işlemi sırasında değişikliklerin çoğunu sizin için otomatik olarak entegre eder
"git pull" Komutu: 
Proje ana dosyasındaki yaptığınız değişikliklerin bilgisayarınızdaki versiyonuna çekilmesini sağlar.
pull kullandığınızda, Git otomatik olarak merge çalışır. Bağlamsal olarak hassastır, bu nedenle Git şu anda çalıştığınız branch için herhangi bir commit varsa birleştirecektir. Dolayısıyla git pull ne işe yarar diye bir soru sorarsak; pull yapılan değişiklikleri gözden geçirmenize izin vermeden otomatik olarak birleştirir diyebiliriz. Eğer branchlerinizi dikkatlice yönetmiyorsanız, sık sık sorunlarla karşılaşabilirsiniz.

7. Merge conflict nedir?
Bu dal üzerinde belirli bir süre çalışırken, bu süreç içerisinde takım arkadaşlarımız master üzerine kendi özellik dallarını birleştirdiler. Artık master o eski bildiğimiz master değil. Eğer aynı dosya üzerinde çalışılmadıysa master ne kadar çok değişirse değişsin herhangi bir çalışma sorunu olmayacaktır. Hatta aynı dosya üzerinde bile çalışsanız, çoğu zaman git çakışma yaratmadan değişiklikleri birleştirecektir. Ancak kimi zaman aynı satırlar üzerinde değişiklikler yaptığınız zaman, git doğal olarak bunu nasıl birleştireceğini bilemiyor. Bu durumda seçimi size bırakmak üzere “conflict” yani çakışma uyarısı veriyor. 


8. Merge conflict'i nasıl çözeriz?
Bu durumun önüne 2 şekilde geçebiliriz:
1-Çakışma gerçekleşmeden önce bunu önlemenin en iyi yolu, üzerinde çalıştığımız özellik dalını sıklıkla master üzerinden rebase komutuyla güncelleştirmektir. Bunu alışkanlık haline getirmek gerekir. Böylelikle çakışma şansını minimuma indirilir. Ancak çakışma ihtimaline karşılık da rebase işlemi öncesinde kodunu stash ile koruma altına almak gerekir.
2-Çakışma gerçekleştikten sonra; Ancak bazı durumlarda PR yaratıldıktan sonra başka PR’lar da master ile birleştirilmiş olabilir. Bu durumda da çakışmalar gerçekleşebilir. Bu durumda ise bir kaç tane ekstra komuta ihtiyacımız olacaktır.
git reset HEAD~1
Bu işlem ile yaptığım değişiklikleri geri almak için. Burada dikkat etmemiz gereken “HEAD~1" seçeneği. Eğer PR yaratmadan önce 2 commit yaptıysak “git reset HEAD~2” komutunu (dolayısıyla 3, 4… için de benzer şekilde) kullanmamız gerekiyor. Daha sonra yukarıda çakışma gerçekleşmeden önce uyguladığımız tüm adımları tek tek tekrar uygulamalıyız. Daha sonra:
git add -A
git commit -m “Çakışma giderildi.”
git push --force

Reset komutunu kullandıktan sonra üzerinde çalıştığımız yerel kod, sunucudaki kodun 1 commit gerisinde kaldı. Git sizin “pull” etmenizi bekliyor. Ancak pull ile bu kodu çekersek edersek tekrar başa dönmüş olacağız. “Pull” etmeden “push” komutunu kullanmaya kalkarsak da git buna izin vermeyecek. Git’e --force seçeneğini kullanmamız gerekiyor. Bu adımdan sonra çakışma tekrar giderildi. Şimdi yapmamız gereken takım arkadaşlarıma kodumu inceletmek (code review) ve sonrasında özellik dalımızı master üzerine “merge” etmek. Bitbucket ya da GitLab gibi sistemler kullanıyorsanız PR yaratıldıktan sonra “Merge” işlemini gerçekleştiren düğmenin olduğunu göreceksiniz. Ancak eğer bu tip bir sistem kullanmıyorsanız
git checkout master
git merge profil-sayfasi
komutlarını kullanabilirsiniz.
