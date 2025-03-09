# 🕌 RamadhanEvent Plugin for PocketMine API 5  

**RamadhanEvent** adalah plugin spesial untuk server PocketMine yang menghadirkan berbagai event dan aktivitas khas bulan Ramadhan, seperti **sahur, berbuka, Lailatul Qadar, Tarawih, Jumat Berkah, berburu takjil, infaq, dan banyak lagi**!  

Plugin ini mendukung **konfigurasi penuh** melalui `config.yml`, sehingga admin dapat dengan mudah mengatur waktu event, hadiah, pahala, serta fitur lainnya.  

---

## 📌 Fitur Utama  

### 🌙 1. Sistem Sahur & Berbuka  
- Pemain akan mendapatkan **notifikasi** saat waktu **sahur** dan **berbuka** tiba.  
- Bisa diatur melalui `config.yml`:  
  ```yaml
  sahur_time: "04:30"
  berbuka_time: "18:00"


---

### 🕌 2. Event Lailatul Qadar

Setiap malam di 10 hari terakhir Ramadhan, pemain yang online bisa mendapatkan buff spesial dan hadiah besar.

Efek buff dapat dikonfigurasi dalam config.yml:
```yml
lailatul_qadar:
  enabled: true
  special_reward: 500
  buff: "strength"
  buff_duration: 3600  # dalam detik (1 jam)
```

---

### 📿 3. Tarawih & Pahala

Pemain bisa mengikuti ibadah Tarawih dan mendapatkan pahala.

Sistem pahala & dosa memungkinkan pemain mengumpulkan pahala dan menghindari dosa.
```yml
pahala_dosa:
  enabled: true
  max_pahala: 1000
  max_dosa: 500
  warning_threshold: 100  # Jika dosa mencapai angka ini, pemain diperingatkan
```

---

### 🎁 4. Event Idul Fitri

Saat Idul Fitri, semua pemain akan mendapatkan hadiah spesial!

Bisa dikonfigurasi di config.yml:
```yml
rewards:
  idul_fitri: 500
```
---

### 🍩 5. Berburu Takjil

Pemain bisa mencari takjil yang tersebar di seluruh map sebelum berbuka.

Hadiah setelah menemukan takjil bisa dikonfigurasi:
```yml
takjil_hunt:
  enabled: true
  reward_money: 100
  reward_pahala: 5
  takjil_spawn_count: 10
```
---

### 💰 6. Infaq & Wakaf

Pemain bisa berdonasi (infaq) dan mendapatkan pahala tambahan.

Setiap infaq akan diumumkan ke seluruh server:
```yml
infaq:
  enabled: true
  reward_pahala: 10
  announcement: "💰 %player% telah berdonasi untuk pembangunan masjid!"
```
---

### 📅 7. Event Jumat Berkah

Setiap hari Jumat, semua pemain yang online akan mendapatkan bonus pahala.

Bisa dikonfigurasi:
```yml
jumat_berkah:
  enabled: true
  reward_pahala: 150
```
---

### 🛍️ 8. Toko Ramadhan (RamadhanShop.php)

Pemain bisa menukarkan pahala dengan hadiah di Ramadhan Shop.

Item yang tersedia bisa dikonfigurasi dalam toko.yml.


---

### 📜 9. Doa Harian & Kajian (DoaManager.php & UstadzNPC.php)

Pemain bisa membaca doa harian yang tersimpan di resources/doa.txt.

NPC Ustadz akan memberikan kajian dan informasi tentang Islam.

---

### 📂 Struktur Plugin
```
RamadhanEvent/
├── src/RamadhanEvent/
│   ├── Main.php
│   ├── command/
│   │   ├── RamadhanCommand.php
│   ├── event/
│   │   ├── PlayerListener.php
│   ├── task/
│   │   ├── SahurTask.php
│   │   ├── BerbukaTask.php
│   │   ├── LailatulQadarTask.php
│   │   ├── IdulFitriTask.php
│   │   ├── TarawihTask.php
│   │   ├── ReminderTask.php
│   │   ├── JumatBerkahTask.php
│   │   ├── TakjilHuntTask.php
│   │   ├── InfaqTask.php
│   ├── utils/
│   │   ├── RewardManager.php
│   │   ├── MissionManager.php
│   │   ├── LeaderboardManager.php
│   │   ├── BarakahManager.php
│   │   ├── DoaManager.php
│   │   ├── InfaqManager.php
│   │   ├── PahalaManager.php
│   ├── entity/
│   │   ├── ImamNPC.php
│   │   ├── PedagangNPC.php
│   │   ├── UstadzNPC.php
│   ├── shop/
│   │   ├── RamadhanShop.php
├── resources/
│   ├── doa.txt
│   ├── misi.yml
│   ├── rewards.yml
│   ├── leaderboard.yml
│   ├── toko.yml
│   ├── musik/
│   │   ├── azan.ogg
│   │   ├── islami.ogg
├── plugin.yml
```
---

### 📜 Cara Install

1. Download plugin ini dan ekstrak ke dalam folder plugins/ di server PocketMine.

2. Sesuaikan pengaturan di config.yml sesuai dengan kebutuhan server.

3. Jalankan ulang server, dan plugin akan langsung aktif!

---

### 🎯 Rencana Update Berikutnya

✅ Sistem Khataman Quran – Pemain bisa menyelesaikan ayat dan mendapatkan hadiah.
✅ Sistem Zakat Fitrah – Pemain wajib membayar zakat sebelum Idul Fitri.
✅ Custom Quest Ramadhan – Misi harian untuk mendapatkan pahala tambahan.
✅ NPC Kajian Islam – NPC yang memberikan ceramah dan motivasi Islami.

---

### 💡 Kontribusi & Feedback

Jika ada saran, bug, atau request fitur baru, silakan hubungi VsrStudio.
Kami selalu terbuka untuk pengembangan lebih lanjut agar plugin ini semakin baik!

---

Terima kasih telah menggunakan RamadhanEvent! Semoga Ramadhan kali ini lebih seru dan penuh keberkahan! 🌙
