# 📦 Установка профиля-визитки для akoffice933-maker

Оформление в стиле [MahdiKordian/MahdiKordian](https://github.com/MahdiKordian/MahdiKordian), адаптировано под ваши проекты и резюме.

## Что в пакете

| Файл | Назначение |
|------|-----------|
| `README.md` | Сам профиль-визитка (шапка, typing-анимация, бейджи, о себе, скиллы, проекты, статистика) |
| `.github/workflows/snake.yml` | GitHub Action: генерирует «змейку» из графика контрибьютов |
| `.gitignore` | Служебный |
| `LICENSE` | MIT (как в примере) |

## Шаг 1. Создайте репозиторий профиля

1. Откройте: **https://github.com/new**
2. Repository name: **`akoffice933-maker`** — строго как ваш логин, иначе визитка не покажется.
3. **Public**, поставьте галочку **Add a README file** → *Create repository*.
4. GitHub сам предложит: «You can add a README to your profile» — это оно и есть.

## Шаг 2. Загрузите файлы

**Вариант А — через веб-интерфейс (проще):**

1. Зайдите в созданный репозиторий → **Add file → Upload files**.
2. Перетащите `README.md`, `LICENSE`, `.gitignore`.
3. Отдельно создайте файл `.github/workflows/snake.yml`: **Add file → Create new file**, введите имя `.github/workflows/snake.yml`, вставьте содержимое, **Commit**.

**Вариант Б — через git:**

```bash
cd github-profile
git init
git add .
git commit -m "Add profile README and snake workflow"
git branch -M main
git remote add origin https://github.com/akoffice933-maker/akoffice933-maker.git
git push -u origin main
```

## Шаг 3. Включите GitHub Actions (для змейки)

1. Репозиторий → вкладка **Actions**. Если есть кнопка **I understand my workflows, go ahead and enable them** — нажмите её.
2. Воркфлоу **Generate Snake** запустится автоматически после пуша и создаст ветку `output` с картинками змейки.
3. Проверить: **Actions → Generate Snake** должен стать зелёным (1–2 минуты).

> Если змейка в профиле не появилась сразу — просто обновите страницу профиля через пару минут: картинка подтягивается из ветки `output`.

## Шаг 4. Проверьте контакты

- **Email** указан как `Akoffice933@gmail.com` — исправьте в `README.md`, если хотите другой.

## Что получится

- 🌊 Анимированная шапка (тёмно-синий + неоновый голубой, тема tokyonight — как в примере)
- ⌨️ Печатающиеся строки: стек и направления работы
- 🏷️ Бейджи контактов + счётчик просмотров профиля
- 👋 **About Me** — текст на русском под ваш профиль
- 🛠️ **Technical Skills** — 12 иконок (Python, TypeScript, React, FastAPI, Docker…) + теги специализаций
- 🚀 **Featured Projects** — 8 ваших лучших проектов из репозиториев (вместо разделов «Образование/Курсы», как договорились)
- 📊 **Статистика**: карточки активности, языкы, streak, змейка

## Как редактировать дальше

- **Добавить проект** → скопируйте любой `<td>`-блок в таблице «Featured Projects».
- **Сменить скилл** → замените иконку: список всех иконок — [devicon.dev](https://devicon.dev), URL вида `https://cdn.jsdelivr.net/gh/devicons/devicon/icons/<имя>/<имя>-original.svg`.
- **Сменить цвета** → во всех ссылках `capsule-render` и `streak-stats` коды `0A192F / 112240 / 00B4D8`; у карточек параметр `theme=`.
- **Строки печатающегося текста** → в ссылке `readme-typing-svg` параметр `lines=` (строки через `;`, пробелы — `+`, `|` — `%7C`, `&` — `%26`).
