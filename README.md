![Bruce Main Menu](./media/pictures/bruce_banner.jpg)

# gradus-firmware

`gradus-firmware` — это форк прошивки `Bruce` с правками сборки, адаптацией под устройства `M5Stack` и дополнительными изменениями под задачи проекта `Gradus`.

Репозиторий подходит для работы с `ESP32`, `Cardputer`, `M5Stick`, `M5Core`, `T-Deck`, `T-Embed` и другими совместимыми платформами.

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
