# @avil13/eslint-config

Набор правил для eslint - для разработки

# Установка

```bash
npm i -D @avil13/eslint-config
```

Подключаете в `.eslintrc.cjs`

```js

/* eslint-env node */
require('@rushstack/eslint-patch/modern-module-resolution');

module.exports = {
  root: true,
  extends: [
     // ... тут оставляете ваши настройки

    '@avil13/eslint-config', // добавляете этот плагин
  ],
  parserOptions: {
    ecmaVersion: 'latest',
  },
  rules: {
    // Если что то надо переопределить
    'no-console': process.env.NODE_ENV === 'production' ? 'error' : 'off',
    'no-debugger': process.env.NODE_ENV === 'production' ? 'error' : 'off',
  },
};

```
