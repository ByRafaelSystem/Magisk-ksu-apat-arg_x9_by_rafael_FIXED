<div align="center">
![Image Alt](https://github.com/ByRafaelSystem/Magisk-ksu-apat-arg_x9_by_rafael_FIXED/blob/main/IMG_20260316_093409.jpg?raw=true)
# ⚡ ARG X9
### By_Rafael System

**Auto Game Resolution X9 — Resolución y DPI automáticos para juegos**

[![Version](https://img.shields.io/badge/Version-v2.0-blue?style=flat-square)]()
[![Android](https://img.shields.io/badge/Android-8%2B-green?style=flat-square)]()
[![Root](https://img.shields.io/badge/Root-Magisk%20%7C%20KSU%20%7C%20APatch-blue?style=flat-square)]()
[![Games](https://img.shields.io/badge/Juegos-522%2B-red?style=flat-square)]()
[![License](https://img.shields.io/badge/License-Apache%202.0-orange?style=flat-square)]()
[![Author](https://img.shields.io/badge/Author-By__Rafael_System-purple?style=flat-square)]()

</div>

---

## 🌍 Idiomas / Languages
- 🇪🇸 [Español](#español)
- 🇺🇸 [English](#english)
- 🇧🇷 [Português](#português)
- 🇮🇩 [Indonesia](#indonesia)
- 🇷🇺 [Русский](#русский)

---

## 🇪🇸 Español

### ¿Qué es ARG X9?

ARG X9 detecta automáticamente cuando abrís un juego y baja la resolución y DPI para maximizar los FPS. Cuando cerrás el juego restaura todo a los valores originales. Sin intervención del usuario. Corre un daemon en segundo plano que monitorea los procesos activos en tiempo real.

### ⚡ ¿Cómo funciona?

1. Al arrancar el sistema ARG restaura tu resolución y DPI originales
2. El daemon `argd` queda corriendo en segundo plano monitoreando apps
3. Cuando detecta que abriste un juego de la lista aplica la resolución y DPI configurados
4. Cuando cerrás el juego restaura todo automáticamente

### 🎮 Presets disponibles

| Preset | Resolución | Ideal para |
|---|---|---|
| ⚡ Ultra FPS | 60% | Máximo rendimiento, calidad reducida |
| 🔥 Alto | 70% | Buen FPS con calidad aceptable |
| ⚖️ Equilibrado | 80% | Balance entre FPS y calidad |
| 🖼️ Calidad | 90% | Calidad casi nativa con mejora de FPS |
| ⚙️ Custom | Libre | Resolución y DPI manuales desde WebUI |

### 📋 Lista de juegos

Incluye **522 juegos** preconfigurados entre los que se encuentran:

- Genshin Impact, Honkai: Star Rail, Zenless Zone Zero
- PUBG Mobile, Free Fire, Call of Duty Mobile
- Mobile Legends, Wild Rift, Arena of Valor
- Minecraft, Roblox, Fortnite
- Asphalt, CarX Street, CarX Highway Racing
- Y muchos más títulos populares

### ✨ Características técnicas

- Daemon nativo `argd` en 32 y 64 bit — se instala automáticamente según la arquitectura del dispositivo
- Usa `wm size` y `wm density` nativos de Android — sin root extra ni herramientas adicionales
- DPI ajustado proporcionalmente a la resolución para mantener la UI legible
- Resolución y DPI originales guardados automáticamente en el primer arranque
- Administrado desde **KSU WebUI** — cambiá presets, activá/desactivá y gestioná juegos sin reiniciar

### 📱 Compatibilidad

| Dispositivo | Compatibilidad | Notas |
|---|---|---|
| Xiaomi / Redmi / POCO | ✅ Completa | Probado en HyperOS 2 |
| Samsung | ✅ Completa | Compatible con One UI |
| OnePlus / OPPO | ✅ Completa | Compatible con ColorOS |
| Motorola | ✅ Completa | Compatible con stock |
| Cualquier Android 8+ | ✅ Universal | Usa `wm size` nativo de Android |

### ⚙️ Gestores de root compatibles

| Gestor | Versión mínima | Estado |
|---|---|---|
| Magisk | v20.4+ | ✅ Soportado |
| KernelSU | Cualquiera | ✅ Soportado |
| APatch | Cualquiera | ✅ Soportado |

### 📲 Instalación

1. Descargá el ZIP desde la página oficial
2. Abrí Magisk / KSU / APatch
3. Instalá desde ZIP
4. Reiniciá el dispositivo
5. Abrí **KSU WebUI** → elegí tu preset y activá ARG

> El módulo detecta automáticamente si tu dispositivo es 32 o 64 bit e instala el daemon correcto.

### ❓ Preguntas frecuentes

**¿Tengo que hacer algo cuando abro un juego?**
No. ARG detecta el juego y aplica los cambios automáticamente.

**¿Qué pasa si el juego no está en la lista?**
La resolución no cambia. El juego corre con tu resolución normal.

**¿La UI del sistema se ve rara durante el juego?**
ARG solo actúa dentro del juego. Si bajás mucho la resolución (60%) puede verse pixelado — probá con 70% u 80%.

**¿Afecta apps que no son juegos?**
No. Solo actúa con los paquetes incluidos en la lista de juegos.

**¿Funciona con otros módulos?**
Sí, es compatible con Project Diablo y VisorX del mismo autor.

---

## 🇺🇸 English

### What is ARG X9?

ARG X9 automatically detects when you open a game and lowers resolution and DPI to maximize FPS. When you close the game it restores everything to original values. No user intervention needed. A background daemon monitors active processes in real time.

### ⚡ How it works

1. On boot ARG restores your original resolution and DPI
2. The `argd` daemon runs in background monitoring apps
3. When it detects a game from the list it applies the configured resolution and DPI
4. When you close the game everything is restored automatically

### 🎮 Available presets

| Preset | Resolution | Best for |
|---|---|---|
| ⚡ Ultra FPS | 60% | Maximum performance, reduced quality |
| 🔥 High | 70% | Good FPS with acceptable quality |
| ⚖️ Balanced | 80% | Balance between FPS and quality |
| 🖼️ Quality | 90% | Near-native quality with FPS boost |
| ⚙️ Custom | Free | Manual resolution and DPI from WebUI |

### 📋 Game list

Includes **522 pre-configured games** including Genshin Impact, PUBG Mobile, Free Fire, Mobile Legends, Wild Rift, Minecraft, Roblox, Fortnite, and many more popular titles.

### ✨ Technical features

- Native `argd` daemon in 32 and 64 bit — installed automatically based on device architecture
- Uses native Android `wm size` and `wm density` — no extra tools needed
- DPI adjusted proportionally to resolution to keep UI readable
- Original resolution and DPI saved automatically on first boot
- Managed from **KSU WebUI** — change presets, enable/disable and manage games without rebooting

### 📱 Compatibility

| Device | Compatibility | Notes |
|---|---|---|
| Xiaomi / Redmi / POCO | ✅ Full | Tested on HyperOS 2 |
| Samsung | ✅ Full | One UI compatible |
| OnePlus / OPPO | ✅ Full | ColorOS compatible |
| Motorola | ✅ Full | Stock compatible |
| Any Android 8+ | ✅ Universal | Uses native Android `wm size` |

### ⚙️ Supported root managers

| Manager | Min version | Status |
|---|---|---|
| Magisk | v20.4+ | ✅ Supported |
| KernelSU | Any | ✅ Supported |
| APatch | Any | ✅ Supported |

### 📲 Installation

1. Download the ZIP from the official page
2. Open Magisk / KSU / APatch
3. Install from ZIP
4. Reboot your device
5. Open **KSU WebUI** → choose your preset and enable ARG

### ❓ FAQ

**Do I need to do anything when opening a game?**
No. ARG detects the game and applies changes automatically.

**What if my game isn't in the list?**
Resolution won't change. The game runs at your normal resolution.

**Does it affect non-game apps?**
No. It only acts on packages included in the game list.

**Is it compatible with other modules?**
Yes, compatible with Project Diablo and VisorX from the same author.

---

## 🇧🇷 Português

### O que é ARG X9?

ARG X9 detecta automaticamente quando você abre um jogo e reduz a resolução e DPI para maximizar os FPS. Ao fechar o jogo restaura tudo automaticamente. Sem intervenção do usuário.

### 🎮 Presets disponíveis

| Preset | Resolução | Ideal para |
|---|---|---|
| ⚡ Ultra FPS | 60% | Máximo desempenho |
| 🔥 Alto | 70% | Bom FPS com qualidade aceitável |
| ⚖️ Equilibrado | 80% | Balanço entre FPS e qualidade |
| 🖼️ Qualidade | 90% | Qualidade quase nativa |
| ⚙️ Custom | Livre | Resolução e DPI manuais |

### 📱 Compatibilidade

| Dispositivo | Compatibilidade |
|---|---|
| Xiaomi / Redmi / POCO | ✅ Total |
| Samsung / OnePlus | ✅ Total |
| Qualquer Android 8+ | ✅ Universal |

### 📲 Instalação

1. Baixe o ZIP na página oficial
2. Abra o Magisk / KSU / APatch
3. Instale pelo ZIP
4. Reinicie
5. Abra o **KSU WebUI** → escolha o preset e ative o ARG

---

## 🇮🇩 Indonesia

### Apa itu ARG X9?

ARG X9 secara otomatis mendeteksi saat Anda membuka game dan menurunkan resolusi serta DPI untuk memaksimalkan FPS. Saat menutup game, semuanya dipulihkan secara otomatis.

### 🎮 Preset tersedia

| Preset | Resolusi | Terbaik untuk |
|---|---|---|
| ⚡ Ultra FPS | 60% | Performa maksimal |
| 🔥 Tinggi | 70% | FPS bagus, kualitas oke |
| ⚖️ Seimbang | 80% | Keseimbangan FPS dan kualitas |
| 🖼️ Kualitas | 90% | Kualitas mendekati native |
| ⚙️ Custom | Bebas | Resolusi dan DPI manual |

### 📱 Kompatibilitas

| Perangkat | Kompatibilitas |
|---|---|
| Xiaomi / Redmi / POCO | ✅ Penuh |
| Samsung / OnePlus | ✅ Penuh |
| Android 8+ manapun | ✅ Universal |

### 📲 Instalasi

1. Unduh ZIP dari halaman resmi
2. Buka Magisk / KSU / APatch
3. Pasang dari ZIP
4. Reboot
5. Buka **KSU WebUI** → pilih preset dan aktifkan ARG

---

## 🇷🇺 Русский

### Что такое ARG X9?

ARG X9 автоматически определяет запуск игры и снижает разрешение и DPI для максимальных FPS. При закрытии игры всё автоматически восстанавливается.

### 🎮 Доступные пресеты

| Пресет | Разрешение | Лучше всего для |
|---|---|---|
| ⚡ Ultra FPS | 60% | Максимальная производительность |
| 🔥 Высокий | 70% | Хороший FPS с приемлемым качеством |
| ⚖️ Баланс | 80% | Баланс FPS и качества |
| 🖼️ Качество | 90% | Почти нативное качество |
| ⚙️ Custom | Свободно | Ручное разрешение и DPI |

### 📱 Совместимость

| Устройство | Совместимость |
|---|---|
| Xiaomi / Redmi / POCO | ✅ Полная |
| Samsung / OnePlus | ✅ Полная |
| Android 8+ любой | ✅ Универсальная |

### 📲 Установка

1. Скачайте ZIP с официальной страницы
2. Откройте Magisk / KSU / APatch
3. Установите из ZIP
4. Перезагрузите устройство
5. Откройте **KSU WebUI** → выберите пресет и активируйте ARG

---

## 📄 Licencia / License

Apache License 2.0 — By_Rafael System © 2026
