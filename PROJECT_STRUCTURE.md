# Структура проекту qwen3-code

## Опис
Мінімальний MVP дизайн для сайту електрика на React + Tailwind CSS (без Next.js)

## Структура файлів

```
kamyanets-electrician/
├── public/
│   └── index.html
├── src/
│   ├── components/
│   │   ├── Header.jsx
│   │   ├── HeroSection.jsx
│   │   ├── ServicesSection.jsx
│   │   ├── BenefitsSection.jsx
│   │   ├── StatsSection.jsx
│   │   ├── Testimonials.jsx
│   │   ├── ContactForm.jsx
│   │   └── Footer.jsx
│   ├── App.jsx
│   ├── index.jsx
│   └── index.css
├── package.json
├── tailwind.config.js
├── postcss.config.js
└── README.md
```

## Встановлення

```bash
# 1. Клонувати репозиторій
git clone https://github.com/AlexSnig/qwen3-code.git
cd qwen3-code

# 2. Встановити залежності
npm install

# 3. Створити файли згідно зі структурою нижче

# 4. Запустити проект
npm start
```

## Файли для створення

### public/index.html
```html
<!DOCTYPE html>
<html lang="uk">
  <head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <title>Електрик Кам'янець-Подільський</title>
  </head>
  <body>
    <div id="root"></div>
  </body>
</html>
```

### postcss.config.js
```javascript
module.exports = {
  plugins: {
    tailwindcss: {},
    autoprefixer: {},
  },
}
```

### src/index.css
```css
@tailwind base;
@tailwind components;
@tailwind utilities;

body {
  font-family: 'Inter', sans-serif;
}

html {
  scroll-behavior: smooth;
}
```

### src/index.jsx
```jsx
import React from 'react';
import ReactDOM from 'react-dom/client';
import './index.css';
import App from './App';

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(
  <React.StrictMode>
    <App />
  </React.StrictMode>
);
```

### src/App.jsx
```jsx
import React from 'react';
import Header from './components/Header';
import HeroSection from './components/HeroSection';
import ServicesSection from './components/ServicesSection';
import BenefitsSection from './components/BenefitsSection';
import StatsSection from './components/StatsSection';
import Testimonials from './components/Testimonials';
import ContactForm from './components/ContactForm';
import Footer from './components/Footer';

function App() {
  return (
    <div className="min-h-screen bg-neutral-50">
      <Header />
      <main>
        <HeroSection />
        <ServicesSection />
        <BenefitsSection />
        <StatsSection />
        <Testimonials />
        <ContactForm />
      </main>
      <Footer />
    </div>
  );
}

export default App;
```

Детальний код всіх компонентів можна знайти в коментарях нижче або в окремих файлах компонентів. Повний код включає:

- **Header.jsx**: Навігаційна панель з логотипом та контактами
- **HeroSection.jsx**: Головна секція з заголовком та CTA кнопками
- **ServicesSection.jsx**: Три картки послуг (аварійний виїзд, заміна проводки, розумний дім)
- **BenefitsSection.jsx**: Чотири переваги компанії
- **StatsSection.jsx**: Статистика (проекти, досвід, клієнти)
- **Testimonials.jsx**: Відгуки клієнтів
- **ContactForm.jsx**: Форма зворотного зв'язку
- **Footer.jsx**: Підвал з контактною інформацією

## Запуск проекту

Після створення всіх файлів:

```bash
npm start
```

Проект буде доступний за адресою http://localhost:3000

## Збірка для продакшну

```bash
npm run build
```
