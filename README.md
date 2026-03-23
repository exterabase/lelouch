# rei_plugins Hub

Сайт-витрина плагинов для ExteraGram/AyuGram, работает на **GitHub Pages**.  
Данные хранятся прямо в `plugins.json` этого репо — никакого бэкенда, никакого SQL.

---

## 🚀 Установка

### 1. Создай новый репозиторий
```
github.com → New repository → Public → назови например rei-plugins
```

### 2. Залей файлы
```
index.html
plugins.json
README.md
```

### 3. Включи GitHub Pages
```
Settings → Pages → Source: Deploy from branch → Branch: main, /root → Save
```

Сайт будет доступен по адресу:  
`https://твой_ник.github.io/rei-plugins/`

---

## 🔑 Как работает Admin

1. Открой сайт
2. Нажми кнопку **⚙** в правом нижнем углу  
3. Введи:
   - **GitHub Owner** — твой ник (например `lyzos`)
   - **Repository** — имя репо (например `rei-plugins`)
   - **Branch** — `main`
   - **GitHub Token** — создай на [github.com/settings/tokens](https://github.com/settings/tokens)  
     Нужны права: **repo** (или минимум `contents:write`)

4. Жми **Войти** — токен хранится только в `sessionStorage` (не в localStorage), очищается при закрытии вкладки

### В Admin-панели можно:
- ➕ Добавить плагин
- ✏ Редактировать (название, версия, описание, теги, ссылки, цвет, иконка)
- ✕ Удалить
- Всё автоматически коммитится в репо

---

## 📦 Структура plugins.json

```json
[
  {
    "id": "hook_inspector",
    "name": "Hook Inspector",
    "version": "12.0",
    "description": "Описание плагина",
    "tags": ["Dev", "Debug"],
    "icon": "⬡",
    "color": "#38bdf8",
    "channel_url": "https://t.me/rei_plugins",
    "download_url": "https://t.me/rei_plugins",
    "status": "stable"
  }
]
```

Поля `status`: `stable` | `beta` | `dev`

---

## ⚠ Важно

- Этот репо **полностью отдельный** от твоего основного сайта на FTP
- Никаких конфликтов с SQL/FTP — это статика на GitHub
- Токен нигде не сохраняется на сервере, только в памяти браузера
