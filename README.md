# 🤖 VK ➜ Telegram Multi-Bot Reposter

Бот на Python для автоматического репоста новых постов из **VK групп** в **Telegram-каналы**. Поддерживает несколько ботов на одного пользователя, удобное меню и автоматическую проверку новых записей.

## 🚀 Возможности

- Мультибот (до 3 настроек на пользователя)
- Репост текста и изображений
- Поддержка вложений (в том числе медиагрупп)
- Умная проверка новых постов
- Интерфейс с кнопками Telegram
- Автозапуск и работа в фоне
- SQLite база для хранения конфигурации

## 🔧 Установка
Обновите python до версии 3.9 и выше

```Открыть bot.py в текстовом редакторе

Найти строку с токеном

Заменить на свой токен:

python
BOT_TOKEN = 'YOUR_BOT_TOKEN'  # Замените этот токен
Как получить токен бота Telegram
Найти в Telegram @BotFather

Отправить команду /newbot

Следовать инструкциям (придумать имя бота и username)

Получить токен вида 123456789:AAFm2f5sdf...t
```

## 📦 Зависимости которые нужно установить перед началом

Файл `requirements.txt` должен включать:
```
pip install python-telegram-bot==20.3
pip install vk-api==11.9.9
pip install requests==2.31.0
pip install python-dotenv==1.0.0
pip install aiohttp==3.8.5
```

## ⚙️ Настройка

1. **Создай Telegram-бота** через `@BotFather`  
   Получи токен и вставь его в `bot.py`:
   ```python
   BOT_TOKEN = 'YOUR_BOT_TOKEN'  # Замените на ваш токен
   ```

2. **Запусти бота:**
   ```bash
   python bot.py
   ```

3. **Открой чат с ботом в Telegram** и нажми `/start`

4. **Добавь до 3 конфигураций**:
   - 🔐 VK токен (Standalone-приложение: https://vk.com/apps?act=manage)
   - 🆔 ID группы VK (например `-123456`)
   - 🤖 Токен Telegram-бота, который будет публиковать
   - 📢 ID или username канала (например `@mychannel` или `-1001234567890`)
   - Не забудь дать боту права администратора в канале

5. Бот будет автоматически проверять новые посты каждые 30 секунд и пересылать в телеграм-канал.

## 🛠 Пример ID группы VK

- `vk.com/club123456` → `-123456`
- `vk.com/public123456` → `-123456`


## 💡 Советы

- Можно настроить несколько Telegram-ботов для разных каналов
- Все конфиги хранятся в `user_data.db`
- Лимит Telegram на медиагруппу — 10 фото

# Установка бота vk-tg-repost-bot на Ubuntu Server

## Шаг 1. Обновляем пакеты и устанавливаем git и Python 3.9 с нужными модулями:

```bash
sudo apt update
sudo apt install git python3.9 python3.9-venv python3.9-dev software-properties-common -y
```

---

## Шаг 2. Если Python 3.9 не установлен, добавляем репозиторий и ставим его:

```bash
sudo add-apt-repository ppa:deadsnakes/ppa -y
sudo apt update
sudo apt install python3.9 python3.9-venv python3.9-dev -y
```

---

## Шаг 3. Проверяем версию Python:

```bash
python3.9 --version
```

---

## Шаг 4. Устанавливаем pip для Python 3:

```bash
sudo apt install python3-pip -y
```

---

## Шаг 5. Клонируем репозиторий с ботом:

```bash
git clone https://github.com/PIOSzzz/vk-tg-repost-bot.git
cd vk-tg-repost-bot
```

---

## Шаг 6. Создаем виртуальное окружение и активируем его:

```bash
python3.9 -m venv venv
source venv/bin/activate
```

---

## Шаг 7. Обновляем pip внутри виртуального окружения и ставим зависимости:

```bash
pip install --upgrade pip
pip install -r requirements.txt
```

Если в процессе появится ошибка с `JobQueue`, установи дополнительно:

```bash
pip install "python-telegram-bot[job-queue]"
```

---

## Шаг 8. Редактируем токен бота:

```bash
nano Bot.py
```

- Найди строку с токеном:  
  `TOKEN = "YOU_BOT_TOKEN"` (примерно)  
- Замени на свой токен.  
- Сохрани: `Ctrl+O` → `Enter` → `Ctrl+X`

---

## Шаг 9. Запускаем бота:

```bash
python3.9 Bot.py
```

---

Если будут вопросы — пиши, разберёмся!  
Бля братан, так всё четко и понятно.





