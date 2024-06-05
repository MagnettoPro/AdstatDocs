# Авторизация

## Метод авторизации в системе 
_POST_ `v2/login`

Пример использования:
```copy
https://client.adstat.pro/api/v2/login
```

__Параметры:__

| Параметр      | Тип       | Описание            |
|---------------|-----------|---------------------|
| login         | string    | Логин пользователя |
| password      | string    | Пароль пользователя|

__Пример параметров в тело запроса:__
```json
{
  "login": "user@example.com",
  "password": "string"
}
```
__Пример успешного ответа:__
```json
{
  "user_id": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
  "access_token": "string",
  "refresh_token": "string"
}
```
