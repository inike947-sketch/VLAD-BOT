# 🚀 Инструкция: Telegram Mini App для @wayforhim

## ШАГ 1 — Публикуем webapp.html на GitHub Pages (БЕСПЛАТНО)

### 1.1 Создай репозиторий
1. Зайди на github.com → **New repository**
2. Название: `vladbot-webapp`
3. Выбери **Public** (это нужно для GitHub Pages)
4. ✅ Поставь галочку "Add README"
5. → **Create repository**

### 1.2 Загрузи файл
1. В репозитории нажми **Add file → Upload files**
2. Перетащи `webapp.html`
3. Переименуй его в `index.html` (или переименуй до загрузки)
4. **Commit changes**

### 1.3 Включи GitHub Pages
1. Settings → Pages (слева)
2. Source: **Deploy from a branch**
3. Branch: **main / root**
4. → **Save**
5. Через 1-2 минуты появится ссылка:
   `https://ТВОЙ_НИК.github.io/vladbot-webapp/`

---

## ШАГ 2 — Создаём Telegram Mini App бота

### 2.1 Создай нового бота через BotFather
```
/newbot
→ имя: VladBot Wayforhim
→ username: wayforhim_app_bot (или любой свободный)
```
Сохрани токен.

### 2.2 Создай меню кнопку (Menu Button)
```
/setmenubutton
→ выбери своего бота
→ введи URL: https://ТВОЙ_НИК.github.io/vladbot-webapp/
→ введи текст кнопки: 🎯 Гайды и VladBot
```

### 2.3 Настрой описание бота
```
/setdescription → @твой_бот
→ текст: "AI-ассистент Влада Белоярцева. Получи бесплатные гайды по AI-маркетингу и поговори с VladBot прямо здесь."

/setabouttext → @твой_бот  
→ текст: "🔥 Гайды по AI-маркетингу | VladBot | Канал @wayforhim"
```

---

## ШАГ 3 — Добавляем бота в канал @wayforhim

1. Открой канал → **Управление каналом → Администраторы**
2. Добавь бота → дай права **Отправка сообщений**
3. Готово!

### 3.1 Закрепи приветственное сообщение в канале
Напиши в канале:
```
🤖 VladBot теперь здесь!

Нажми кнопку меню ↓ или напиши боту @wayforhim_app_bot

🎁 Там:
— Бесплатные гайды
— VladBot — спросить про AI-маркетинг
— Подборка обучения VladCoding

t.me/wayforhim_app_bot
```

---

## ШАГ 4 — Добавляем AI в VladBot

В файле `webapp.html` найди строку:
```javascript
'x-api-key': apiKey || '__REPLACE_WITH_YOUR_KEY__',
```

Замени `__REPLACE_WITH_YOUR_KEY__` на свой Anthropic API ключ:
```javascript
'x-api-key': 'sk-ant-api03-ВАШ_КЛЮЧ',
```

ИЛИ — сделай модальное окно с вводом ключа (как на сайте МОЗГИ).

---

## ШАГ 5 — Настрой уведомления о лидах

В файле найди:
```javascript
fetch(`https://api.telegram.org/bot7993773888:AAH3KlHgbbM6y2nWq4W4O1ek6nEv5rV9PkA/sendMessage`,{
  ...
  body:JSON.stringify({chat_id:'370993773', ...})
```

Это уже настроено на твои данные из исходного сайта! При каждом заполнении воронки тебе придёт уведомление.

---

## ВОРОНКА — как это работает

```
Пользователь заходит в бота/канал
        ↓
Нажимает кнопку меню или ссылку
        ↓
Mini App открывается (твой сайт)
        ↓
Главная → кнопка "Получить бесплатный гайд"
        ↓
ШАГИ ВОРОНКИ:
  1. Выбирает тему гайда (3 варианта)
  2. Вводит имя + нишу + цель
  3. Ты получаешь уведомление в TG
  4. Его направляют в @wayforhim за гайдом
  5. Бонус: ссылка на @Svamivladi для разбора
        ↓
VladBot — отвечает на вопросы 24/7
        ↓
Переходит в Обучение → записывается
```

---

## 💡 Альтернатива: Без GitHub Pages (ещё проще)

Используй **Telegraph** (telegra.ph):
1. Зайди на telegra.ph
2. Создай страницу
3. Вставь содержимое через Edit HTML
→ Бесплатно, мгновенно, работает как Mini App

Или **Netlify Drop**:
1. Зайди на netlify.com/drop
2. Перетащи папку с index.html
3. Получи ссылку вида `random-name.netlify.app`
→ Тоже бесплатно!

---

## Итог

✅ Mini App на GitHub Pages — БЕСПЛАТНО навсегда
✅ Воронка с 3 гайдами
✅ VladBot с AI
✅ Уведомления о лидах тебе в Telegram
✅ Обучение VladCoding
✅ Стиль 1-в-1 как сайт МОЗГИ
