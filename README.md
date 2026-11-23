# Дневник тренировок — установка

Программы тренировок, план наперёд, запись в зале и статистика. Одно и то же приложение на всех устройствах, работает без интернета. Данные между устройствами сводятся через GitHub.

| Устройство | Как поставить |
|---|---|
| **Android** | Скачай [`training-diary.apk`](https://github.com/Bablakov/training-diary-app/releases/latest/download/training-diary.apk) с телефона и установи (разреши установку из этого источника). |
| **Windows** | Скачай [`training-diary-setup.exe`](https://github.com/Bablakov/training-diary-app/releases/latest/download/training-diary-setup.exe) и запусти. Права администратора не нужны, ярлык появится на рабочем столе и в «Пуске». |
| **iPhone** | Открой https://bablakov.github.io/training-diary/ в Safari → «Поделиться» → «На экран „Домой“». |

Все версии: [Releases](https://github.com/Bablakov/training-diary-app/releases).

## Обновления

- **Windows и Android** сами проверяют, вышла ли новая версия. Если вышла — всплывёт сообщение, а в «Справочнике» появится кнопка «Скачать». Установи поверх: данные и настройки сохранятся.
- **iPhone** обновляется сам при следующем открытии с интернетом.

## Синхронизация между устройствами

Данные лежат в приватном репозитории `Bablakov/training-data`. На каждом устройстве один раз:

1. GitHub → Settings → Developer settings → Personal access tokens → **Fine-grained tokens** → Generate new token.
2. Repository access: **Only select repositories** → `training-data`.
3. Permissions → Repository permissions → **Contents: Read and write**.
4. В приложении: «Справочник» → «Синхронизация через GitHub» → вставь токен → «Проверить доступ».

Дальше синхронизация идёт сама: через пару секунд после изменений в плане и программах, после начала и окончания тренировки, при сворачивании и открытии приложения и раз в 3 минуты, пока оно открыто. Без интернета всё работает, изменения уйдут, когда связь появится.

Без GitHub данные можно перенести файлом: «Справочник» → «Перенос данных» → «Поделиться файлом» (например, себе в Telegram), на другом устройстве — «Выбрать файл» → «Объединить».

## Где хранятся данные

- Android и iPhone — внутри приложения на телефоне.
- Windows — `%APPDATA%\Дневник тренировок` (остаётся при обновлении и при удалении программы).

Исходный код: [Bablakov/training-diary](https://github.com/Bablakov/training-diary).
