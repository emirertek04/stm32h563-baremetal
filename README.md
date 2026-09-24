# STM32H563ZI Bare-Metal Hardware Abstraction Layer (HAL)

Bu proje, **STM32H563ZI** (Arm Cortex-M33) mikrodenetleyicisi için herhangi bir harici kütüphane (STM32Cube HAL, LL, CMSIS vb.) veya IDE kullanılmadan, tamamen register düzeyinde geliştirilmekte olan modüler ve eksiksiz bir bare-metal çevre birimi sürücü mimarisidir.

Geliştirme süreci ST **RM0481 Reference Manual** referans alınarak yürütülmektedir.

---

## Proje Durumu: Faz 1 (RCC ve Çekirdek Başlatma)

Şu anki geliştirme adımı, sistemin tüm saat dağıtımından, veri yollarından ve osilatörlerinden sorumlu olan **Reset and Clock Control (RCC)** modülüne odaklanmaktadır.

### Mevcut Dosya Yapısı

```text
├── drivers/
│   ├── inc/
│   │   └── rcc.h       # RCC register tanımları, bit maskeleri ve sürücü API bildirimleri
│   └── src/
│       └── rcc.c       # RCC yapılandırma, osilatör yönetimi ve clock-gating fonksiyonları
├── app/
│   └── main.c          # Sistem giriş noktası ve sürücü doğrulama/test alanı
└── README.md
