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

Установка на ubuntu server 

2. Проверка текущей версии Python:
bash
Копировать
Редактировать
python3 --version
Если версия ниже 3.9 — обновляем.

3. Обновление Python до 3.9+ на Ubuntu
Для Ubuntu 20.04 и новее:

bash
Копировать
Редактировать
sudo apt update
sudo apt install software-properties-common -y
sudo add-apt-repository ppa:deadsnakes/ppa -y
sudo apt update
sudo apt install python3.9 python3.9-venv python3.9-dev -y

1. Устанавливаем git и обновляем пакеты:
bash
Копировать
Редактировать
apt update
apt install git python3.9 python3.9-venv python3.9-dev -y

Установка pip для Python 3:
bash
Копировать
Редактировать
apt update
apt install python3-pip -y

После установки pip, чтобы использовать именно для python3.9, лучше так:
bash
Копировать
Редактировать
python3.9 -m pip install --upgrade pip
python3.9 -m pip install -r requirements.txt

И запускать тоже через python3.9:

bash
Копировать
Редактировать
python3.9 Bot.py




