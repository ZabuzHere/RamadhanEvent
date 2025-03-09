# RamadhanEvent
this fun plugin for pocketmine 5

### Config
```yml
# ================================
# 🎉 Konfigurasi Plugin Ramadhan 🎉
# ================================

# 🕐 Waktu Sahur dan Berbuka (Format: Jam:Menit)
sahur_time: "04:30"
berbuka_time: "18:00"

# Event Command
# /event true or false
command: warp
default: false

# 📅 Event Spesial
events:
  lailatul_qadar: true
  idul_fitri: true
  jumat_berkah: true
  tarawih: true
  berburu_takjil: true
  infaq: true

# 🍽️ Berburu Takjil
takjil_hunt:
  enabled: true
  reward_money: 100
  reward_pahala: 5
  takjil_spawn_count: 10

# 💰 Infaq & Wakaf
infaq:
  enabled: true
  reward_pahala: 10
  announcement: "💰 %player% telah berdonasi untuk pembangunan masjid!"

# 🌙 Lailatul Qadar (Hadiah jika online di malam spesial)
lailatul_qadar:
  enabled: true
  special_reward: 500
  buff: "strength"
  buff_duration: 3600  # Detik (1 jam)

# 🕌 Sistem Pahala & Dosa
pahala_dosa:
  enabled: true
  max_pahala: 1000
  max_dosa: 500
  warning_threshold: 100  # Jika dosa mencapai angka ini, pemain diperingatkan

# 🏆 Reward Ramadhan
rewards:
  sahur: 50
  berbuka: 50
  idul_fitri: 500
  jumat_berkah: 150
  tarawih: 100

# 📜 Pesan Notifikasi
messages:
  sahur: "🌙 Waktunya sahur! Jangan lupa makan sebelum puasa!"
  berbuka: "🍽️ Waktunya berbuka! Semoga puasamu diterima!"
  jumat_berkah: "🤲 Jumat Berkah! Mari perbanyak ibadah!"
```

### Structure
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
