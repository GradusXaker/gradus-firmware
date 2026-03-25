# Gradus Firmware: сборка для M5Stick S3

```text
> repo: gradus-firmware
> doc: RELEASE_NOTES
> purpose: Первая успешная сборка под M5Stick S3
```


Первая успешная сборка `Bruce-m5stack-sticks3.bin` для `M5Stick S3`.

## Что сделано

- добавлен новый board/env `m5stack-sticks3`
- собран merged bin для прошивки по смещению `0x0`
- сохранены ранее сделанные фиксы сборки для `m5stack-cplus2`

## Готовый артефакт

- `Bruce-m5stack-sticks3.bin`

## Сборка

```bash
.venv/bin/platformio run -e m5stack-sticks3
```
