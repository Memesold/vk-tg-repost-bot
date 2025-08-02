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

```bash
git clone https://github.com/yourusername/vk-to-telegram-multibot.git
cd vk-to-telegram-multibot
python -m venv venv
source venv/bin/activate   # или venv\Scripts\activate для Windows
pip install -r requirements.txt
```

## 📦 Зависимости

Файл `requirements.txt` должен включать:
```
python-telegram-bot==20.3
vk-api
requests
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

## 🧠 Структура проекта

```
📦 vk-to-telegram-multibot
├── bot.py               # Основной скрипт
├── user_data.db         # SQLite база данных
├── requirements.txt     # Зависимости
└── README.md            # Этот файл
```

## 💡 Советы

- Можно настроить несколько Telegram-ботов для разных каналов
- Все конфиги хранятся в `user_data.db`
- Лимит Telegram на медиагруппу — 10 фото



