# Design System — Material 3 Expressive Edition

Офіційна дизайн-система інтерфейсів **DeepSeek**, побудована на гайдлайнах **Material 3 Expressive (M3E)**. Система розроблена для створення емоційного, адаптивного, високоефективного та візуально динамічного середовища взаємодії з штучним інтелектом.

---

## 1. Філософія Material 3 Expressive у DeepSeek

Material 3 Expressive виходить за межі суто функціонального мінімалізму, додаючи в інтерфейс емоційність, динаміку та візуальну чіткість. В контексті DeepSeek це реалізується через 5 ключових стовпів:

1. **Fluid Motion & Spring Physics:** Інтерфейс реагує на дії користувача природно. Використання физики пружин (Springs) замість жорстких лінійних таймінгів створює відчуття живого інструменту.
2. **Expressive Dynamic Shapes:** Скруглення та форми елементів не є статичними. Вони змінюють свій радіус (Shape Morphing) залежно від стану (наприклад, поле введення розширюється, а кнопка відправки трансформується при переході в стан "Thinking").
3. **Intentional Color & AI States:** Колір інформує про стан когнітивних процесів моделі. Різні режими (генерація, пошук у мережі, виконання коду, міркування DeepThink) мають чітку тональну та колірну ідентичність.
4. **Expressive Typography:** Двошарова типографічна ієрархія з вираженими контрастами між акцентними заголовками та числовими/кодовими блоками.
5. **Contextual Layouts:** Компоненти плавно адаптуються до розміру екрана та робочого контексту (від мобільного чату до багатовіконного середовища аналізу даних).

---

## 2. Повна Токенізована Система Кольорів (Color Tokens)

Дизайн-система підтримує подвійну тональну палітру (Light / Dark Mode), розраховану з урахуванням контрастності WCAG AAA.

### 2.1 Core Color Tokens (Основні кольори)

| Токен | Light Mode | Dark Mode | Опис та застосування |
| :--- | :--- | :--- | :--- |
| `md.sys.color.primary` | `#0056C6` | `#A8C7FF` | Головний колір бренду DeepSeek |
| `md.sys.color.on-primary` | `#FFFFFF` | `#002D69` | Текст/іконки поверх Primary |
| `md.sys.color.primary-container` | `#D8E2FF` | `#004397` | Активні елементи, виділені сесії |
| `md.sys.color.on-primary-container` | `#001A43` | `#D8E2FF` | Текст поверх Primary Container |
| `md.sys.color.secondary` | `#535F70` | `#BCC7DB` | Допоміжні контроли, другорядні кнопки |
| `md.sys.color.on-secondary` | `#FFFFFF` | `#253141` | Текст поверх Secondary |
| `md.sys.color.secondary-container` | `#D7E3F8` | `#3B4758` | Бейджі, мета-інформація |
| `md.sys.color.on-secondary-container` | `#101C2B` | `#D7E3F8` | Текст поверх Secondary Container |
| `md.sys.color.tertiary` | `#7E489E` | `#E8B3FF` | Expressive-фіолетовий для брейнштормінгу |
| `md.sys.color.on-tertiary` | `#FFFFFF` | `#4A176B` | Текст поверх Tertiary |
| `md.sys.color.tertiary-container` | `#F6D9FF` | `#643084` | Акцентний фон інструментів |
| `md.sys.color.on-tertiary-container` | `#2D0047` | `#F6D9FF` | Текст поверх Tertiary Container |

### 2.2 Surface & Background Tokens (Поверхні)

| Токен | Light Mode | Dark Mode | Застосування |
| :--- | :--- | :--- | :--- |
| `md.sys.color.surface` | `#F8F9FF` | `#111318` | Базовий фон додатку |
| `md.sys.color.surface-dim` | `#D9DADF` | `#111318` | Приглушений фон |
| `md.sys.color.surface-bright` | `#F8F9FF` | `#37393E` | Яскравий поверхневий шар |
| `md.sys.color.surface-container-lowest` | `#FFFFFF` | `#0C0E13` | Найнижчий шар (карти коду) |
| `md.sys.color.surface-container-low` | `#F2F3FA` | `#191C22` | Бокове меню (Sidebar) |
| `md.sys.color.surface-container` | `#EEF0F8` | `#1D2026` | Картки, баббли повідомлень |
| `md.sys.color.surface-container-high` | `#E8EAF2` | `#282A31` | Floating Input Bar |
| `md.sys.color.surface-container-highest` | `#E2E2E9` | `#33353C` | Активні діалогові панелі |
| `md.sys.color.outline` | `#74777F` | `#8E9099` | Чіткі кордони, роздільники |
| `md.sys.color.outline-variant` | `#C4C6CF` | `#44474F` | М'які рамки інпут-полів |

### 2.3 AI State Tokens (Стани штучного інтелекту)

| Стан AI | Token Name | HEX Light | HEX Dark | Застосування / Візуалізація |
| :--- | :--- | :--- | :--- | :--- |
| **Idle** | `md.sys.color.ai-idle` | `#0056C6` | `#A8C7FF` | Готовність до роботи, дефолтна кнопка |
| **Thinking (CoT)** | `md.sys.color.ai-thinking` | `#7E489E` | `#E8B3FF` | Режим DeepThink (R1). Пульсуючий градієнт |
| **Web Search** | `md.sys.color.ai-search` | `#006874` | `#80D5E5` | Пошук у веб-мережі. Бірюзовий індикатор |
| **Code Execution**| `md.sys.color.ai-exec` | `#2E6A44` | `#97D5A4` | Запуск Python/JS пісочниці. Смарагдовий |
| **Success** | `md.sys.color.ai-success` | `#136D3B` | `#81D899` | Успішне завершення виконання завдання |
| **Error / Fault** | `md.sys.color.ai-error` | `#BA1A1A` | `#FFB4AB` | Помилка API, таймаут, збій мережі |

---

## 3. Розширена Типографіка (Typography Scale)

Використовується мульти-шрифтова система:
* **Primary Sans-Serif:** `Roboto Flex` / `Inter` / `Noto Sans` (універсальний читабельний текст).
* **Monospace (Code & Math):** `JetBrains Mono` / `Fira Code` (для блоків коду, токенів, математичних формул).

| Категорія | Стиль | Розмір (Size) | Line Height | Вага (Weight) | Tracking (Letter Spacing) |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Display** | Large | 57px | 64px | 400 (Regular) | -0.25px |
| | Medium | 45px | 52px | 400 (Regular) | 0px |
| | Small | 36px | 44px | 400 (Regular) | 0px |
| **Headline** | Large | 32px | 40px | 600 (SemiBold) | 0px |
| | Medium | 28px | 36px | 600 (SemiBold) | 0px |
| | Small | 24px | 32px | 500 (Medium) | 0px |
| **Title** | Large | 22px | 28px | 500 (Medium) | 0px |
| | Medium | 16px | 24px | 500 (Medium) | +0.15px |
| | Small | 14px | 20px | 500 (Medium) | +0.1px |
| **Body** | Large | 16px | 24px | 400 (Regular) | +0.5px |
| | Medium | 14px | 20px | 400 (Regular) | +0.25px |
| | Small | 12px | 16px | 400 (Regular) | +0.4px |
| **Label** | Large | 14px | 20px | 500 (Medium) | +0.1px |
| | Medium | 12px | 16px | 500 (Medium) | +0.5px |
| | Small | 11px | 16px | 500 (Medium) | +0.5px |
| **Code/Mono**| Code Body | 14px | 22px | 400 (Regular) | 0px |
| | Code Label| 12px | 16px | 500 (Medium) | 0px |

---

## 4. Відступи, Сітка та Dynamic Shapes

### 4.1 Spacing Tokens (Базовий шаг 8pt / 4pt)

* `space-3xs` (`2px`) — Мікро-інтервали (крапки станів).
* `space-2xs` (`4px`) — Внутрішні зазори іконка + текст.
* `space-xs` (`8px`) — Гап між чипами та тегами.
* `space-s` (`12px`) — Внутрішній паддінг компактних елементів.
* `space-m` (`16px`) — Базовий паддінг карток, бабблів та інпутів.
* `space-l` (`24px`) — Відстань між блоками повідомлень у чаті.
* `space-xl` (`32px`) — Зовнішні відступи контейнерів екрана.
* `space-2xl` (`48px`) — Секційні роздільники.
* `space-3xl` (`64px`) — Відступи від країв у широкоформатних режимах.

### 4.2 Shape Morphing & Scale

У Material 3 Expressive скруглення мають значення рівня емоційності.

```
[None: 0px] -> [XS: 4px] -> [S: 8px] -> [M: 12px] -> [L: 16px] -> [XL: 28px] -> [Full: 9999px]
```

* **Shape None (`0px`):** Повноекранні полотна.
* **Shape Extra Small (`4px`):** Тултипи, кути код-блоків.
* **Shape Small (`8px`):** Меню, випадаючі списки, контекстні підказки.
* **Shape Medium (`12px`):** Внутрішні картки, модальні вікна.
* **Shape Large (`16px`):** Чат-баббли (з можливістю асиметрії: `16px 16px 4px 16px`).
* **Shape Extra Large (`28px`):** Floating Input Bar, великі діалогові вікна.
* **Shape Full (`9999px`):** Pill-кнопки, чипи режимів (DeepThink, Web Search), аватари.

---

## 5. Тіні, Тонування та Матеріали

### 5.1 Elevation Tokens

Тіні в M3E поєднують розмиття (Blur) та тональне забарвлення відповідним кольором поверхні (Surface Tint).

| Elevation Level | Shadow Spec | Surface Tint Overlay | Об'єкти |
| :--- | :--- | :--- | :--- |
| **Level 0** | `none` | 0% | Базовий фон, повідомлення |
| **Level 1** | `0px 1px 2px rgba(0,0,0,0.08), 0px 1px 3px 1px rgba(0,0,0,0.05)` | 5% | Картки історій при ховері |
| **Level 2** | `0px 2px 6px rgba(0,0,0,0.12), 0px 1px 2px 0px rgba(0,0,0,0.08)` | 8% | Floating Input Bar у спокої |
| **Level 3** | `0px 4px 12px rgba(0,0,0,0.15), 0px 2px 4px 0px rgba(0,0,0,0.08)` | 11% | Випадаючі меню, модалки |
| **Level 4** | `0px 6px 16px rgba(0,0,0,0.18), 0px 3px 6px 0px rgba(0,0,0,0.10)` | 13% | Навігаційні плаваючі панелі |
| **Level 5** | `0px 8px 24px rgba(0,0,0,0.22), 0px 4px 8px 0px rgba(0,0,0,0.12)` | 15% | Діалоги вищого пріоритету |

### 5.2 Material FX (Frosted Glass & Blur)

Для стікі-шапок та плаваючого інпуту використовується ефект скляного матування:

* **Glassmorphism Backdrop:** `backdrop-filter: blur(16px) saturate(180%);`
* **Light Glass Surface:** `rgba(248, 249, 255, 0.75)` з рамкою `1px solid rgba(255, 255, 255, 0.4)`
* **Dark Glass Surface:** `rgba(17, 19, 24, 0.75)` з рамкою `1px solid rgba(255, 255, 255, 0.08)`

---

## 6. Сітка Макету та Breakpoints

Макет автоматично підлаштовується під роздільну здатність екрана.

| Назва Breakpoint | Код | Діапазон | Колонок | Margins | Gutters | Навігація |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **Compact** | `sm` | `< 600px` | 4 | 16px | 16px | Bottom Navigation Bar |
| **Medium** | `md` | `600px - 839px` | 8 | 24px | 16px | Navigation Rail |
| **Expanded** | `lg` | `840px - 1199px` | 12 | 32px | 24px | Collapsible Drawer |
| **Large** | `xl` | `1200px - 1599px` | 12 | 40px | 24px | Fixed Navigation Drawer |
| **Extra Large** | `2xl` | `1600px+` | 12 | Auto (Max Content: 1440px) | 32px | Fixed Drawer + Inspector Panel |

---

## 7. Деталізовані UI/UX Патерни

### 7.1 Floating Expressive Input Bar
* **Конструкція:** Плаваюча панель із `Shape Extra Large (28px)` та ефектом `Elevation Level 2`.
* **Розширення:** При фокусі або введенні багаторядкового тексту інпут розширюється вгору за допомогою Spring-анімації.
* **Елементи всередині:**
  * Верхній/Нижній ряд з **Contextual Chips** (`DeepThink R1`, `Web Search`, `File Attach`).
  * Кнопка надсилання: У стані `Idle` — кругла кнопка `40x40px` із заповненням `Primary`. При відсутності тексту — напівпрозора. При наявності тексту — стає активною з мікро-масштабуванням `scale(1.05)`.

### 7.2 Chat Bubbles & Reasoning Blocks (CoT)
* **User Bubble:** 
  * Фон: `primary-container`. 
  * Вирівнювання: Праворуч. 
  * Форма: `16px 16px 4px 16px`.
* **DeepSeek AI Response:**
  * Фон: Прозорий або `surface-container`.
  * Вирівнювання: Ліворуч.
  * Форма: `16px 16px 16px 4px`.
* **Reasoning Block (DeepThink CoT):**
  * Фон: `tertiary-container` (прозорість 12%).
  * Рамка: `1px solid md.sys.color.tertiary`.
  * Header: Анімована іконка ✨ Sparkles, таймер міркування (наприклад, "Думав 4.2 секунди"), кнопка згортання/розгортання accordion-типу.

### 7.3 Code Blocks
* **Стилізація:** Всебічний Dark Mode стиль (`#0D0E12`) навіть у Light-темі для збереження контрасту синтаксису.
* **Toolbar Header:**
  * Ліворуч: Іконка мови + назва (`python`, `tsx`, `cpp`).
  * Праворуч: Кнопки дій: **[Copy Code]**, **[Run / Execute]**, **[Format]**.
* **Синтаксис:** Токени підсвічуються відповідно до палітри M3E (ключові слова — `tertiary`, рядки — `ai-exec`, функції — `primary`).

---

## 8. Анімації та Мікровзаємодії (Motion Physics)

### 8.1 Spring Physics Curves

Замість стандартних CSS Easing реалізовано пружинні безьє:

* **Expressive Spring (М'яка віддача):** `cubic-bezier(0.34, 1.56, 0.64, 1)` — для виклику кнопок, розгортання меню.
* **Standard Damped (Швидке згасання):** `cubic-bezier(0.2, 0.0, 0.0, 1.0)` — для звичайних переходів та скролу.
* **Accelerate (Exit):** `cubic-bezier(0.3, 0.0, 0.8, 0.15)` — для закриття та зникнення елементів.

### 8.2 Duration Tokens

* `duration-short` — `150ms` (Ховери, натискання)
* `duration-medium` — `300ms` (Відкриття дропдаунів, зміна форми)
* `duration-long` — `500ms` (Розгортання блоків міркування, трансформація панелей)

---

## 9. Приклади Інтеграції (Tailwind & CSS Variables)

### 9.1 CSS Variables (`variables.css`)

```css
:root {
  /* Core Colors */
  --md-sys-color-primary: #0056c6;
  --md-sys-color-on-primary: #ffffff;
  --md-sys-color-primary-container: #d8e2ff;
  --md-sys-color-on-primary-container: #001a43;
  
  --md-sys-color-tertiary: #7e489e;
  --md-sys-color-tertiary-container: #f6d9ff;
  
  --md-sys-color-surface: #f8f9ff;
  --md-sys-color-surface-container: #eef0f8;
  --md-sys-color-surface-container-high: #e8eaf2;

  /* AI States */
  --md-sys-color-ai-thinking: #7e489e;
  --md-sys-color-ai-search: #006874;
  --md-sys-color-ai-exec: #2e6a44;

  /* Shapes */
  --md-shape-xs: 4px;
  --md-shape-s: 8px;
  --md-shape-m: 12px;
  --md-shape-l: 16px;
  --md-shape-xl: 28px;
  --md-shape-full: 9999px;

  /* Easing */
  --md-ease-spring: cubic-bezier(0.34, 1.56, 0.64, 1);
}

.dark {
  --md-sys-color-primary: #a8c7ff;
  --md-sys-color-on-primary: #002d69;
  --md-sys-color-primary-container: #004397;
  --md-sys-color-on-primary-container: #d8e2ff;

  --md-sys-color-tertiary: #e8b3ff;
  --md-sys-color-tertiary-container: #643084;

  --md-sys-color-surface: #111318;
  --md-sys-color-surface-container: #1d2026;
  --md-sys-color-surface-container-high: #282a31;
}
```

### 9.2 Tailwind Config (`tailwind.config.js`)

```javascript
/** @type {import('tailwindcss').Config} */
module.exports = {
  darkMode: 'class',
  theme: {
    extend: {
      colors: {
        md: {
          primary: {
            DEFAULT: 'var(--md-sys-color-primary)',
            on: 'var(--md-sys-color-on-primary)',
            container: 'var(--md-sys-color-primary-container)',
            'on-container': 'var(--md-sys-color-on-primary-container)',
          },
          tertiary: {
            DEFAULT: 'var(--md-sys-color-tertiary)',
            container: 'var(--md-sys-color-tertiary-container)',
          },
          surface: {
            DEFAULT: 'var(--md-sys-color-surface)',
            container: 'var(--md-sys-color-surface-container)',
            high: 'var(--md-sys-color-surface-container-high)',
          },
          ai: {
            thinking: 'var(--md-sys-color-ai-thinking)',
            search: 'var(--md-sys-color-ai-search)',
            exec: 'var(--md-sys-color-ai-exec)',
          }
        }
      },
      borderRadius: {
        'm3-xs': 'var(--md-shape-xs)',
        'm3-s': 'var(--md-shape-s)',
        'm3-m': 'var(--md-shape-m)',
        'm3-l': 'var(--md-shape-l)',
        'm3-xl': 'var(--md-shape-xl)',
        'm3-full': 'var(--md-shape-full)',
      },
      transitionTimingFunction: {
        'spring': 'var(--md-ease-spring)',
      }
    },
  },
  plugins: [],
};
```