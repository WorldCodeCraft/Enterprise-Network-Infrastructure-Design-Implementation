# 🖧 Merkez Kurumsal Ağ Altyapısı — Gelişmiş Ağ Simülasyonu

## 🔹 Proje Hakkında
Bu proje, **Cisco Packet Tracer** üzerinde tasarlanmış tam yedekli ve güvenli bir kurumsal ağı simüle eder.  
Ağ yapısında **6 departman (VLAN)** ve dışa açık servisler için bir **DMZ** bulunur.  
Merkezi **Core Switch'ler** üzerinden inter-VLAN routing sağlanmış, **Cisco ASA Firewall** ile güvenlik katmanları oluşturulmuştur.  
Amaç; **ağ segmentasyonu, gateway/internet yedekliliği (Failover), güvenlik ve yönetim prensiplerini** uygulamalı olarak göstermektir.  

---

## 🌐 Cisco Network Diagram

<img width="1379" height="667" alt="tasarım" src="https://github.com/user-attachments/assets/6fe459f1-e54c-47fb-9131-ec0436a5fc1d" />


---

## 🏢 Ağ Topolojisi

| Departman/Bölge | VLAN ID | IP Aralığı | Switch | Açıklama |
|------------|----------|-------------|----------|------------|
| IT | 10 | 10.10.10.0/24 | ACC-IT01 | IT Departmanı |
| HR | 20 | 10.10.20.0/24 | ACC-HR01 | İnsan Kaynakları |
| Finance | 30 | 10.10.30.0/24 | ACC-FIN01 | Finans Departmanı |
| Operations | 40 | 10.10.40.0/24 | ACC-OPS01 | Operasyon |
| Office | 50 | 10.10.50.0/24 | ACC-OFFICE01 | Genel Ofis |
| WiFi/IoT | 60 | 10.10.60.0/24 | ACC-WIFI01 | Kablosuz Cihazlar |
| Server | 100 | 10.10.100.0/24 | SERVER-SW | İç Sunucular (DHCP/DNS vs) |
| DMZ | 3 | 172.16.10.0/24 | DMZ-SW | Dışa Açık Sunucular |

---

## ⚙️ Kullanılan Cihazlar
- **4× Router:** Cisco 2911 (Edge & ISP Simülasyonu)  
- **2× Firewall:** Cisco ASA 5505  
- **2× Core Switch:** Cisco 3560 (L3 HSRP & Inter-VLAN)  
- **4× Distribution Switch:** Cisco 3560 (VLAN Toplama)  
- **8× Access/Server/DMZ Switch:** Cisco 2960  
- **14× Sunucu:** DHCP, DNS, RADIUS, NTP, Syslog, Web, FTP vs.  

---

## 🎯 Temel Özellikler
- **HSRP & Floating Static Route** ile 0 kesintili yedeklilik (Failover)  
- ASA Firewall üzerinden **DMZ segmentasyonu** ve **NAT/PAT**  
- L3 Switchler ile Inter-VLAN routing ve **DHCP Relay**  
- 802.1Q Trunk bağlantılar üzerinden VLAN taşıma  
- Profesyonel ve kolay anlaşılır 3 katmanlı topoloji tasarımı  

---

## 🔒 Güvenlik & Yönetim
- ASA tarafında **Katı ACL Kuralları** ve Güvenlik Seviyeleri (Security Levels)  
- Access portlarda yetkisiz switch engellemek için **BPDUGuard**  
- AAA altyapısı ile merkezi **RADIUS kimlik doğrulama**  
- **service password-encryption** komutu ile tüm parolalar şifrelendi  
- **banner motd** mesajları ile yasal uyarılar eklendi  

---

## 🧠 Öğrenme Çıktıları
- Layer 2 ve Layer 3 anahtarlama mimarisi (Core/Distribution/Access)  
- HSRP ile sanal ağ geçidi tasarımı  
- Firewall kural yazımı ve DMZ izolasyonu  
- Ağ üzerindeki trafik akışını (paket seviyesinde) analiz etme yeteneği  
- Kurumsal ölçekte bir ofis ağı tasarlama ve belgeleme becerisi  

---

## 👨💻 Tasarım & Katkıda Bulunan
**Proje Tasarımcısı:** Batuhan  
**Katkılar:** Ağ topolojisi tasarımı, L2/L3 yapılandırması, Firewall güvenlik kuralları, Failover test senaryoları.  

---

## 📁 Dosya İçeriği
- `/cod/` klasörü → Tüm cihazların (Core, Dist, Access, ASA, Router) yapılandırma kodları  

---

## 🧩 Lisans
Bu proje yalnızca **öğrenme ve eğitim amaçlıdır.**  
© 2026 Batuhan — Tüm hakları saklıdır.
