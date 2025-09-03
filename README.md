<div align="center">
  <h1>Vaultwarden on Render</h1>
  <img src="assets/logo.svg"/>
  <div>Это пример репозитория для запуска последней версии Vaultwarden на Render. Вам необходимо добавить любую бесплатную базу данных используя переменные окружения, предоставленные вики Vaultwarden.</div>
  <div>Ознакомьтесь с их вики-документацией, чтобы узнать больше о переменных окружения и узнать, как их использовать.</div>
</div>

|Переменная|Обязательна?|Формат|Объяснение|
|---|-|-|---|
|ADMIN_TOKEN|Нет|Строка|Административный пароль. Сгенерируется автоматически|
|DATABASE_URL|Да|Строка|Адрес БД. Лол где ему ещё данные хранить?|
|SIGNUPS_ALLOWED|Нет|Логические значения|Возможность регистрации|
|WEB_VAULT_ENABLED|Нет|Логические значения|Даёт возможность пользоваться веб интерфейсом без приложения или расширения|

<div align="center">
  <h2>Деплой</h2>
</div>

[![Deploy to Render](https://render.com/images/deploy-to-render-button.svg)](https://render.com/deploy?repo=https://github.com/msweetdogs/Vaultwarden-Render)

<div align="center">
  <h2>Обновления</h2>
  <div>Используется последняя версия VaultWarden просто обновите экземпляр на render.com</div>
</div>