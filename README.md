<div align="center">
  <img src="./media/pictures/bruce_banner.jpg" alt="gradus-firmware banner" width="100%" />

  <h1>gradus-firmware</h1>
  <p><strong>Кибер-прошивка для ESP32 и M5Stack.</strong> Форк `Bruce` с фикcами сборки, адаптацией под `Gradus` и сценариями для собственных релизов.</p>

  <p>
    <img src="https://img.shields.io/badge/ESP32-firmware-111827?style=for-the-badge&logo=espressif&logoColor=22C55E" alt="ESP32 firmware" />
    <img src="https://img.shields.io/badge/M5Stack-Gradus-111827?style=for-the-badge&logoColor=22C55E" alt="M5Stack Gradus" />
    <img src="https://img.shields.io/badge/Cardputer-supported-111827?style=for-the-badge&logoColor=22C55E" alt="Cardputer" />
    <img src="https://img.shields.io/badge/fork-Bruce-22C55E?style=for-the-badge&labelColor=0B1220" alt="Fork Bruce" />
  </p>
</div>

```text
> branch: gradus-firmware
> mission: build fixes + device adaptation + release workflow
> vibe: offensive tooling meets practical embedded engineering
```

## обзор

Этот форк нужен для задач `Gradus`: собрать стабильные бинарники, поддержать нужные устройства `M5Stack` и встроить прошивку в собственный инструмент прошивки.

## Что изменено в этом форке

- исправления, связанные со сборкой;
- адаптация под устройства `M5Stack`;
- подготовка репозитория под использование вместе с `Gradus Flasher`;
- собственные релизные сценарии и бинарные сборки.

## Установка

### Быстрый способ

Для быстрой прошивки можно использовать Web Flasher upstream-проекта:
- https://bruce.computer/flasher

### Локальная прошивка через `esptool.py`

Если у вас уже есть готовый бинарник, прошивка выполняется так:

```sh
esptool.py --port /dev/ttyACM0 write_flash 0x00000 Bruce-<device>.bin
```

### Устройства `M5Stack`

Если используется `M5Launcher`, для части устройств доступна установка по `OTA`.

Также можно использовать `m5burner tool`:
- https://docs.m5stack.com/en/download

## Документация

- Wiki upstream-проекта: https://github.com/pr3y/Bruce/wiki
- FAQ: https://github.com/pr3y/Bruce/wiki/FAQ

## Основные возможности

### Wi‑Fi

- подключение к Wi‑Fi и режим AP;
- Beacon Spam, Target Attack, deauth-сценарии;
- Wardriving;
- `TelNet`, `SSH`, `TCP Client`, `TCP Listener`;
- `RAW Sniffer`, `Scan Hosts`, `Evil Portal`, `Wireguard Tunneling`.

### BLE

- `BLE Scan`;
- `Bad BLE`;
- BLE-клавиатура для поддерживаемых моделей;
- spam-функции для разных платформ.

### RF / RFID / IR / FM / NRF24

- работа с RF-модулями, включая `CC1101`;
- чтение, запись и клонирование RFID-меток;
- ИК-функции;
- FM и `NRF24` инструменты.

### Дополнительные инструменты

- `JavaScript Interpreter`;
- `SD Card Manager` и `LittleFS Manager`;
- `WebUI`;
- `BADUsb`;
- `Openhaystack`;
- `iButton`;
- LED control;
- часы и NTP;
- обмен файлами и командами через `ESPNOW`.

## Поддерживаемые устройства

Форк сохраняет совместимость с широкой линейкой устройств, включая:
- `M5Stack Cardputer`;
- `M5StickC Plus / Plus2`;
- `M5Core`, `M5Core2`, `M5CoreS3`;
- `JCZN CYD-2432S028`;
- `Lilygo T-Embed`, `T-Deck`, `T-Display-S3` и другие.

Подробности по конкретным аппаратным возможностям лучше смотреть в wiki и таблицах совместимости upstream-проекта.

## Визуально

![Bruce Main Menu](./media/pictures/pic1.png)
![Bruce on M5Core](./media/pictures/core.png)
![Bruce on Stick](./media/pictures/stick.png)
![Bruce on CYD](./media/pictures/cyd.png)

Другие материалы доступны в `./media/`.

## Дисклеймер

Прошивка предназначена только для законных, исследовательских, учебных и авторизованных сценариев использования. Не применяйте ее для несанкционированного доступа, нарушения работы устройств или сетей и любых незаконных действий. Все использование — на ваш риск.

## контакты

<p>
  <a href="https://github.com/GradusXaker"><img src="https://img.shields.io/badge/GitHub-GradusXaker-111827?style=flat-square&logo=github&logoColor=22C55E" alt="GitHub" /></a>
  <a href="https://vk.com/gradus_xaker"><img src="https://img.shields.io/badge/VK-gradus__xaker-111827?style=flat-square&logo=vk&logoColor=22C55E" alt="VK" /></a>
  <a href="mailto:gradus_xaker@mail.ru"><img src="https://img.shields.io/badge/email-write-111827?style=flat-square&logo=gmail&logoColor=22C55E" alt="Email" /></a>
</p>

