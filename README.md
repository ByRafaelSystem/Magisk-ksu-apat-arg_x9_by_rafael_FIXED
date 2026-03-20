<div align="center">

![Repo Banner](https://github.com/ByRafaelSystem/Magisk-ksu-apat-arg_x9_by_rafael_FIXED/blob/main/IMG_20260320_090348.jpg?raw=true)

# ⚡ ARG X9 — Auto Game Resolution
### By_Rafael System

[![Version](https://img.shields.io/badge/Version-v3.0-00e87a?style=flat-square)](https://github.com/ByRafaelSystem/Magisk-ksu-apat-arg_x9_by_rafael_FIXED/releases)
[![Android](https://img.shields.io/badge/Android-8%2B-green?style=flat-square)](https://github.com/ByRafaelSystem/Magisk-ksu-apat-arg_x9_by_rafael_FIXED)
[![Root](https://img.shields.io/badge/Root-Magisk%20%7C%20KSU%20%7C%20APatch-blue?style=flat-square)](https://github.com/ByRafaelSystem/Magisk-ksu-apat-arg_x9_by_rafael_FIXED)
[![Games](https://img.shields.io/badge/Games-522%2B-red?style=flat-square)](https://github.com/ByRafaelSystem/Magisk-ksu-apat-arg_x9_by_rafael_FIXED)
[![License](https://img.shields.io/badge/License-Apache%202.0-orange?style=flat-square)](LICENSE)
[![Author](https://img.shields.io/badge/Author-By__Rafael__System-purple?style=flat-square)](https://t.me/proyect_diablo)

**Detección automática de juegos · Resolución y DPI optimizados · WebUI integrado**

[📥 Descargar v3.0](https://github.com/ByRafaelSystem/Magisk-ksu-apat-arg_x9_by_rafael_FIXED/releases/latest) · [✈️ Canal Telegram](https://t.me/proyect_diablo) · [🐙 GitHub](https://github.com/ByRafaelSystem)

</div>

---

## 🌍 Idiomas / Languages

[🇪🇸 Español](#-español) · [🇺🇸 English](#-english) · [🇧🇷 Português](#-português) · [🇮🇩 Indonesia](#-indonesia) · [🇷🇺 Русский](#-русский)

---

## 🇪🇸 Español

### ¿Qué es ARG X9?

ARG X9 es un módulo para Android rooteado que detecta automáticamente cuando abrís un juego y ajusta la resolución y DPI en tiempo real para maximizar los FPS. Al cerrar el juego todo vuelve a los valores originales sin que hagas nada.

Corre un daemon nativo (`argd`) en segundo plano que monitorea los procesos activos leyendo directamente el kernel de Android — funciona con el juego en primer plano o minimizado.

### ✨ Novedades en v3.0

| Feature | Descripción |
|---|---|
| 🔍 **Detección universal** | Lee `/proc/[pid]/oom_score_adj` — funciona con juego en background |
| 📊 **Juego activo en WebUI** | El panel muestra en tiempo real qué juego está corriendo |
| ✏️ **Presets editables** | Cada preset tiene valores custom guardados permanentemente |
| ↺ **Reset a automático** | Un toque devuelve el preset al cálculo automático por porcentaje |
| 👾 **Gamelist con nombre** | Cada juego puede tener un nombre personalizado además del paquete |
| 🖥️ **ROOT · CHIP · ANDROID** | La tarjeta de status muestra información del sistema |
| 🗑️ **Borrar gamelist** | Botón para limpiar todos los juegos de la lista |

### ⚡ ¿Cómo funciona?

```
Boot → Restaura resolución original
  ↓
argd + service.sh corren en segundo plano
  ↓
Cada 2 segundos: escanea /proc buscando un juego activo
  ↓
¿Juego detectado en gamelist?
  ├── SÍ → aplica resolución y DPI de juego
  └── NO → mantiene resolución original
  ↓
¿Juego cerrado?
  └── SÍ → restaura resolución y DPI originales
```

### 🎮 Presets

| Preset | Resolución | DPI | Ideal para |
|---|---|---|---|
| ⚡ Ultra FPS | 60% | +67% | Máximo rendimiento, juegos competitivos |
| 🔥 Alto FPS | 70% | +43% | Buen balance FPS / calidad |
| ⚖️ Equilibrado | 80% | +25% | FPS mejorado con calidad aceptable |
| 💎 Calidad | 90% | +11% | Calidad casi nativa con FPS levemente mejor |
| ✏️ Custom | Libre | Libre | Valores manuales desde el WebUI |

> Los presets calculan automáticamente los valores según la resolución de tu dispositivo. También podés editarlos manualmente y se guardan permanentemente.

### 🎯 Detección de juego activo

A diferencia de versiones anteriores que usaban `dumpsys activity`, la v3.0 escanea directamente `/proc` del kernel:

- Lee `oom_score_adj` de cada proceso — detecta apps en foreground Y en background
- Lee `cmdline` para obtener el nombre del paquete
- Compara contra el gamelist cada 2 segundos
- **Funciona aunque el juego esté minimizado** (accediste a notificaciones, etc.)
- Universal en todos los dispositivos rooteados con Android 4+

### 📱 Chips detectados

El WebUI detecta automáticamente el SoC de tu dispositivo:

| Fabricante | Chips detectados |
|---|---|
| MediaTek | `mt[num]`, Helio, Dimensity |
| Qualcomm | `sm[num]`, Snapdragon, MSM |
| Samsung | Exynos, `s5e` |
| Google | Tensor, `gs[num]` |
| Unisoc | Unisoc, UMS |
| HiSilicon | Kirin, `hi[num]` |

### 📋 Gamelist — 522+ juegos incluidos

El gamelist cubre los títulos más populares de cada categoría:

**Battle Royale:** Free Fire, PUBG Mobile, Call of Duty Mobile, Fortnite, Battlegrounds Mobile India

**MOBA:** Mobile Legends, Wild Rift, Honor of Kings, Pokémon UNITE

**RPG / Open World:** Genshin Impact, Honkai: Star Rail, Zenless Zone Zero, Tower of Fantasy

**FPS / TPS:** Modern Strike Online, Critical Ops, Standoff 2, Shadowgun Legends

**Casual / Hypercasual:** Subway Surfers, Temple Run, Candy Crush, Clash of Clans

**Racing:** Asphalt 9, CarX Street, Real Racing 3, Need for Speed

Y muchos más. También podés agregar cualquier juego manualmente desde el WebUI.

### 🖥️ WebUI

El panel de control se abre desde KSU → Módulos → ARG X9:

| Sección | Qué hace |
|---|---|
| **Status** | Daemon · Resolución actual · Juego activo · ROOT · CHIP · Android |
| **Presets** | 4 presets de un toque + modo edición con valores custom |
| **Configuración** | Resolución sistema, DPI sistema, resolución juego, DPI juego, intervalo |
| **Gamelist** | Ver, agregar (nombre + paquete) y eliminar juegos |
| **Daemon** | Start · Stop · Restart · Refresh manual |

### ⚙️ Compatibilidad

| Gestor de root | Versión | Estado |
|---|---|---|
| Magisk | v20.4+ | ✅ Soportado |
| KernelSU | Cualquiera | ✅ Soportado |
| APatch | Cualquiera | ✅ Soportado |

| Android | Estado |
|---|---|
| Android 8 – 15 | ✅ Soportado |
| HyperOS 1 / 2 | ✅ Probado |
| One UI | ✅ Soportado |
| ColorOS | ✅ Soportado |
| Stock AOSP | ✅ Soportado |

### 📲 Instalación

1. Descargá el ZIP desde [Releases](https://github.com/ByRafaelSystem/Magisk-ksu-apat-arg_x9_by_rafael_FIXED/releases/latest)
2. Abrí Magisk / KSU / APatch
3. Instalá desde ZIP
4. Reiniciá el dispositivo
5. Abrí **KSU WebUI** → tocá el módulo ARG X9
6. Elegí un preset y el módulo está activo

> El módulo detecta automáticamente la arquitectura del dispositivo (32 o 64 bit) e instala el daemon correcto.

### ❓ Preguntas frecuentes

**¿Tengo que hacer algo cuando abro un juego?**
No. ARG detecta el juego automáticamente y aplica los cambios.

**¿El juego no está en la lista. ¿Qué hago?**
Abrí el WebUI → Gamelist → ingresá el nombre y el nombre del paquete (ej: `com.dts.freefireth`) → Agregar.

**¿Cómo sé el paquete de un juego?**
Buscalo en Play Store, la URL tiene el formato `?id=com.paquete.juego`. También podés usar apps como APK Info.

**¿Ultra FPS se ve pixelado?**
Es normal — al 60% la imagen es menos nítida. Probá con Alto FPS (70%) o Equilibrado (80%) para mejor balance.

**¿El preset no aplica los valores que edité?**
Los valores custom se guardan en el navegador del WebUI. Si borrás datos del navegador se pierden — tendrías que volver a configurarlos.

**¿Funciona con juegos que no son de Play Store?**
Sí, cualquier APK instalado. Agregá el paquete manualmente al gamelist.

**¿Afecta apps que no son juegos?**
No. Solo actúa con paquetes incluidos en el gamelist.

**¿Es compatible con Project Diablo?**
Sí, son del mismo autor y se pueden usar juntos.

---

## 🇺🇸 English

### What is ARG X9?

ARG X9 is a module for rooted Android that automatically detects when you open a game and adjusts resolution and DPI in real time to maximize FPS. When you close the game everything returns to original values automatically.

A native daemon (`argd`) runs in the background monitoring active processes by reading directly from the Android kernel — works with the game in foreground or minimized.

### ✨ What's new in v3.0

| Feature | Description |
|---|---|
| 🔍 **Universal detection** | Reads `/proc/[pid]/oom_score_adj` — works with game in background |
| 📊 **Active game in WebUI** | Panel shows in real time which game is running |
| ✏️ **Editable presets** | Each preset has permanently saved custom values |
| ↺ **Reset to automatic** | One tap returns preset to automatic percentage calculation |
| 👾 **Gamelist with name** | Each game can have a custom name alongside the package |
| 🖥️ **ROOT · CHIP · ANDROID** | Status card shows system information |
| 🗑️ **Clear gamelist** | Button to remove all games from the list |

### ⚡ How it works

```
Boot → Restores original resolution
  ↓
argd + service.sh run in background
  ↓
Every 2 seconds: scans /proc looking for active game
  ↓
Game found in gamelist?
  ├── YES → applies game resolution and DPI
  └── NO  → keeps original resolution
  ↓
Game closed?
  └── YES → restores original resolution and DPI
```

### 🎮 Presets

| Preset | Resolution | DPI | Best for |
|---|---|---|---|
| ⚡ Ultra FPS | 60% | +67% | Maximum performance, competitive games |
| 🔥 High FPS | 70% | +43% | Good FPS / quality balance |
| ⚖️ Balanced | 80% | +25% | Improved FPS with acceptable quality |
| 💎 Quality | 90% | +11% | Near-native quality with slight FPS boost |
| ✏️ Custom | Free | Free | Manual values from WebUI |

### 🎯 Game detection

Unlike previous versions that relied on `dumpsys activity`, v3.0 scans the kernel `/proc` directly:

- Reads `oom_score_adj` from each process — detects foreground AND background apps
- Reads `cmdline` to get the package name
- Compares against the gamelist every 2 seconds
- **Works even when the game is minimized**
- Universal on all rooted devices with Android 4+

### 🖥️ WebUI

The control panel opens from KSU → Modules → ARG X9:

| Section | What it does |
|---|---|
| **Status** | Daemon · Current resolution · Active game · ROOT · CHIP · Android |
| **Presets** | 4 one-tap presets + edit mode with custom values |
| **Config** | System res, system DPI, game res, game DPI, interval |
| **Gamelist** | View, add (name + package) and remove games |
| **Daemon** | Start · Stop · Restart · Manual refresh |

### ⚙️ Compatibility

| Root manager | Version | Status |
|---|---|---|
| Magisk | v20.4+ | ✅ Supported |
| KernelSU | Any | ✅ Supported |
| APatch | Any | ✅ Supported |

### 📲 Installation

1. Download the ZIP from [Releases](https://github.com/ByRafaelSystem/Magisk-ksu-apat-arg_x9_by_rafael_FIXED/releases/latest)
2. Open Magisk / KSU / APatch
3. Install from ZIP
4. Reboot your device
5. Open **KSU WebUI** → tap the ARG X9 module
6. Choose a preset — the module is now active

### ❓ FAQ

**Do I need to do anything when opening a game?**
No. ARG detects the game automatically and applies the changes.

**My game isn't in the list. What do I do?**
Open WebUI → Gamelist → enter the name and package name (e.g. `com.dts.freefireth`) → Add.

**Ultra FPS looks pixelated.**
That's normal at 60%. Try High FPS (70%) or Balanced (80%) for better balance.

**Does it work with sideloaded games?**
Yes, any installed APK. Add the package manually to the gamelist.

**Does it affect non-game apps?**
No. It only acts on packages included in the gamelist.

---

## 🇧🇷 Português

### O que é ARG X9?

ARG X9 é um módulo para Android com root que detecta automaticamente quando você abre um jogo e ajusta a resolução e DPI para maximizar os FPS. Ao fechar o jogo, tudo é restaurado automaticamente.

Um daemon nativo (`argd`) roda em segundo plano monitorando os processos ativos lendo diretamente do kernel do Android — funciona com o jogo em primeiro plano ou minimizado.

### ✨ Novidades na v3.0

| Feature | Descrição |
|---|---|
| 🔍 **Detecção universal** | Lê `/proc/[pid]/oom_score_adj` — funciona em background |
| 📊 **Jogo ativo no WebUI** | Painel mostra em tempo real qual jogo está rodando |
| ✏️ **Presets editáveis** | Cada preset tem valores custom salvos permanentemente |
| ↺ **Reset automático** | Um toque volta o preset ao cálculo automático por percentual |
| 👾 **Gamelist com nome** | Cada jogo pode ter nome personalizado além do pacote |
| 🖥️ **ROOT · CHIP · ANDROID** | Card de status mostra informações do sistema |

### 🎮 Presets

| Preset | Resolução | Ideal para |
|---|---|---|
| ⚡ Ultra FPS | 60% | Máximo desempenho, jogos competitivos |
| 🔥 Alto FPS | 70% | Bom balanço FPS / qualidade |
| ⚖️ Equilibrado | 80% | FPS melhorado com qualidade aceitável |
| 💎 Qualidade | 90% | Qualidade quase nativa |
| ✏️ Custom | Livre | Valores manuais pelo WebUI |

### 📲 Instalação

1. Baixe o ZIP em [Releases](https://github.com/ByRafaelSystem/Magisk-ksu-apat-arg_x9_by_rafael_FIXED/releases/latest)
2. Abra o Magisk / KSU / APatch
3. Instale pelo ZIP
4. Reinicie o dispositivo
5. Abra o **KSU WebUI** → toque no módulo ARG X9
6. Escolha um preset — o módulo já está ativo

### ❓ Perguntas frequentes

**Preciso fazer algo quando abrir um jogo?**
Não. ARG detecta automaticamente e aplica as mudanças.

**Meu jogo não está na lista. O que faço?**
Abra o WebUI → Gamelist → insira o nome e o pacote (ex: `com.dts.freefireth`) → Adicionar.

**Ultra FPS parece pixelado.**
Normal a 60%. Tente Alto FPS (70%) ou Equilibrado (80%) para melhor balanço.

---

## 🇮🇩 Indonesia

### Apa itu ARG X9?

ARG X9 adalah modul untuk Android yang sudah di-root yang secara otomatis mendeteksi saat Anda membuka game dan menyesuaikan resolusi serta DPI untuk memaksimalkan FPS. Saat menutup game, semuanya dipulihkan otomatis.

Daemon native (`argd`) berjalan di latar belakang memantau proses aktif dengan membaca langsung dari kernel Android — bekerja dengan game di foreground maupun diminimalkan.

### ✨ Yang baru di v3.0

| Fitur | Deskripsi |
|---|---|
| 🔍 **Deteksi universal** | Membaca `/proc/[pid]/oom_score_adj` — bekerja di background |
| 📊 **Game aktif di WebUI** | Panel menampilkan game yang sedang berjalan secara real time |
| ✏️ **Preset yang bisa diedit** | Setiap preset memiliki nilai custom yang disimpan permanen |
| ↺ **Reset otomatis** | Satu ketukan mengembalikan preset ke kalkulasi otomatis |
| 👾 **Gamelist dengan nama** | Setiap game bisa punya nama kustom selain nama paket |
| 🖥️ **ROOT · CHIP · ANDROID** | Kartu status menampilkan info sistem |

### 🎮 Preset

| Preset | Resolusi | Terbaik untuk |
|---|---|---|
| ⚡ Ultra FPS | 60% | Performa maksimal, game kompetitif |
| 🔥 FPS Tinggi | 70% | FPS bagus dengan kualitas layak |
| ⚖️ Seimbang | 80% | FPS lebih baik dengan kualitas oke |
| 💎 Kualitas | 90% | Kualitas mendekati native |
| ✏️ Custom | Bebas | Nilai manual dari WebUI |

### 📲 Instalasi

1. Unduh ZIP dari [Releases](https://github.com/ByRafaelSystem/Magisk-ksu-apat-arg_x9_by_rafael_FIXED/releases/latest)
2. Buka Magisk / KSU / APatch
3. Pasang dari ZIP
4. Reboot perangkat
5. Buka **KSU WebUI** → ketuk modul ARG X9
6. Pilih preset — modul sudah aktif

### ❓ FAQ

**Apakah saya perlu melakukan sesuatu saat membuka game?**
Tidak. ARG mendeteksi game secara otomatis dan menerapkan perubahan.

**Game saya tidak ada di daftar. Apa yang harus dilakukan?**
Buka WebUI → Gamelist → masukkan nama dan nama paket (contoh: `com.dts.freefireth`) → Tambah.

---

## 🇷🇺 Русский

### Что такое ARG X9?

ARG X9 — модуль для рутированного Android, который автоматически определяет запуск игры и снижает разрешение и DPI для максимальных FPS. При закрытии игры всё восстанавливается автоматически.

Нативный демон (`argd`) работает в фоне, отслеживая активные процессы через прямое чтение ядра Android — работает когда игра свёрнута или открыта.

### ✨ Что нового в v3.0

| Функция | Описание |
|---|---|
| 🔍 **Универсальное определение** | Читает `/proc/[pid]/oom_score_adj` — работает в фоне |
| 📊 **Активная игра в WebUI** | Панель показывает запущенную игру в реальном времени |
| ✏️ **Редактируемые пресеты** | Каждый пресет хранит пользовательские значения навсегда |
| ↺ **Сброс к авто** | Одно нажатие возвращает пресет к автоматическому расчёту |
| 👾 **Gamelist с именами** | Каждой игре можно дать имя помимо имени пакета |
| 🖥️ **ROOT · ЧИП · ANDROID** | Карточка статуса показывает информацию о системе |

### 🎮 Пресеты

| Пресет | Разрешение | Лучше всего для |
|---|---|---|
| ⚡ Ultra FPS | 60% | Максимальная производительность |
| 🔥 Высокий FPS | 70% | Хороший баланс FPS / качество |
| ⚖️ Баланс | 80% | Улучшенный FPS с приемлемым качеством |
| 💎 Качество | 90% | Почти нативное качество |
| ✏️ Custom | Свободно | Ручные значения из WebUI |

### 📲 Установка

1. Скачайте ZIP из [Releases](https://github.com/ByRafaelSystem/Magisk-ksu-apat-arg_x9_by_rafael_FIXED/releases/latest)
2. Откройте Magisk / KSU / APatch
3. Установите из ZIP
4. Перезагрузите устройство
5. Откройте **KSU WebUI** → нажмите на модуль ARG X9
6. Выберите пресет — модуль активен

### ❓ Частые вопросы

**Нужно ли что-то делать при запуске игры?**
Нет. ARG определяет игру автоматически и применяет изменения.

**Моей игры нет в списке. Что делать?**
Откройте WebUI → Gamelist → введите имя и имя пакета (например: `com.dts.freefireth`) → Добавить.

**Ultra FPS выглядит пикселизировано.**
Нормально при 60%. Попробуйте Высокий FPS (70%) или Баланс (80%) для лучшего соотношения.

---

## 📄 Licencia / License

```
Copyright 2026 By_Rafael System

Licensed under the Apache License, Version 2.0
```

---

<div align="center">

**By_Rafael System © 2026**

[![Telegram](https://img.shields.io/badge/Telegram-Canal%20Oficial-blue?style=flat-square&logo=telegram)](https://t.me/proyect_diablo)

*ARG X9 v3.0 · Auto Game Resolution · Universal*

</div>
