Senaryo: Büyük Bir Şirketin Ağ Altyapısını Tasarlama ve Güvenlik Sağlama
Şirket Adı: TechCorp Ltd.

Lokasyonlar: 
Merkez Ofis: (Ana yönlendirme ve sunucu odası burada olacak)
Şube 1: (Küçük bir ofis, internet erişimi ve merkezi kaynaklara erişim olmalı)
Şube 2: (Orta ölçekli bir ofis, VLAN’lar ve güvenlik önlemleri uygulanmalı)
Çalışan Sayısı: 200+

1 - Ağ Tasarımını Yap

    a - Merkez ofiste en az 3 VLAN oluştur. (Örn: Yönetim, Çalışanlar, Misafir)
    b - Her şubede ayrı IP subnetleri kullan. (Örn: Şube 1 - 192.168.10.0/24, Şube 2 - 192.168.20.0/24)
    c - Router-on-a-Stick yapılandırarak VLAN’lar arası iletişimi sağla.
    d - Tüm cihazları statik IP veya DHCP ile adreslendir.

2 - Yönlendirme ve İnternet Çıkışı Ayarları

    a - Merkez ofis ve şubeler arasında OSPF veya EIGRP ile dinamik yönlendirme yap.
    b - Her şube, merkez ofis üzerinden internete çıkmalı.
    c - NAT (Network Address Translation) kullanarak iç ağın internet erişimini sağla.

3 - Ağ Güvenliğini Sağla

    a - ACL’ler (Access Control Lists) kullanarak güvenlik kuralları belirle. 
        Örn: Misafir VLAN’ı sadece internete çıkabilmeli, iç ağa erişememeli.
        Örn: Yönetim VLAN’ı tüm ağa erişebilmeli ama diğer VLAN’lardan erişim engellenmeli.
    b - Port Security kullanarak switch güvenliğini sağla.
    c - SSH ve Telnet erişimini sadece belirli IP’lere izin vererek sınırla.
    d - Firewall ve IDS/IPS (Simüle edilebilir) gibi güvenlik önlemlerini uygula.

4 - Sunucu Hizmetlerini Yapılandır

    a - Merkez ofiste bir DHCP sunucu yapılandır ve şubelere DHCP relay ile dağıt.
    b - DNS sunucusu ekle ve istemcilerin isim çözümleme yapmasını sağla.
    c - Bir FTP veya Web sunucusu kur ve kullanıcıların dosya paylaşımını sağla.


5 - Kablosuz Ağ Entegrasyonu (Opsiyonel, Daha Zor Seviye)

    a - Şirket içi kablosuz ağ kurarak SSID’leri farklı VLAN’lara yönlendir.
    b - WPA2-Enterprise kullanarak güvenli kablosuz erişim sağla.
    c - MAC filtreleme ile ek güvenlik sağla.


Bu projeyi Cisco Packet Tracer’da tamamla ve şu bileşenlerin çalıştığını doğrula:

    VLAN’lar ve yönlendirme (PC’ler arası ping testi)
    İnternet çıkışı ve NAT doğrulama
    ACL kurallarının çalışması (engellenen/gelen paketleri test et)
    SSH ile güvenli yönetim bağlantısı yap
    DHCP sunucusunun IP dağıttığını doğrula
