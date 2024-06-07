# Работа с объявлениями

## <span id="advertisements">Метод получения кампаний</span>


_GET_ `v2/advertisement/?show_deleted=false&period=today&offset=0&limit=50&advertisement_titles=&campaign_names=`

Пример использования:
```http request
https://client.adstat.pro/api/v2/advertisement/?show_deleted=false&period=today&offset=0&limit=50&advertisement_titles=&campaign_names=
```

__Описание query-параметров:__


| Параметр             | Тип     | Описание                                                                                                  |
|----------------------|---------|-----------------------------------------------------------------------------------------------------------|
| show_deleted         | Boolean | Параметр, определяющий, нужно ли показывать удаленные объявления. Возможные значения: `true` или `false`. |
| period               | Строка  | Период, за который необходимо получить данные. Например, `today`, `yesterday`, `all`, `starts_months`.    |
| offset               | Число   | Смещение в результирующем списке объявлений.                                                              |
| limit                | Число   | Максимальное количество объявлений в ответе.                                                              |
| advertisement_titles | Строка  | Фильтрация по названию объявления.                                                                        |
| campaign_names       | Строка  | Фильтрация по названию объявления.                                                                        |




__Пример успешного ответа:__
```json
{
  "data": [
    {
      "id": 0,
      "account_name": "string",
      "campaign_name": "string",
      "advertisement_title": "string",
      "status": "string",
      "object": "string",
      "ad_text": "string",
      "cpm": 0,
      "target_topics": [
        "string"
      ],
      "balance": 0,
      "cps": 0,
      "created_dt": "string",
      "status_updated_dt": "2024-06-07T11:50:05.475Z",
      "ad_type": "target_channels",
      "goals": 0,
      "impressions": 0,
      "cpc": 0,
      "ctr": 0,
      "spent": 0,
      "clicks": 0
    }
  ]
}
```


__Описание параметров успешного ответа:__

| Поле              | Тип                | Описание                                                                  |
|-------------------|--------------------|---------------------------------------------------------------------------|
| id                | Число              | Уникальный идентификатор объявления.                                      |
| account_name      | Строка             | Название аккаунта, которому принадлежит объявление.                       |
| campaign_name     | Строка             | Название кампании, к которой относится объявление.                        |
| advertisement_title | Строка           | Название объявления.                                                      |
| status            | Строка             | Текущий статус объявления.                                                |
| object            | Строка             | Объект рекламирования.                                                    |
| ad_text           | Строка             | Текст креатива объявления.                                                |
| cpm               | Число              | Стоимость тысячи показов (CPM).                                           |
| target_topics     | Массив строк       | Список топиков, на которые таргетируется объявление.                      |
| balance           | Число              | Баланс объявлением.                                                       |
| cps               | Число              | Стоимость за цель (CPS).                                                  |
| created_dt        | Строка             | Дата и время создания объявления в формате строки.                        |
| status_updated_dt | Строка             | Дата и время последнего обновления статуса объявления в формате ISO 8601. |
| ad_type           | Строка             | Тип объявления <br/>(например, `"target_channels"`, `target_users`).           |
| goals             | Число              | Количество достигнутых целей.                                             |
| impressions       | Число              | Количество показов объявления.                                            |
| cpc               | Число              | Стоимость за клик (CPC).                                                  |
| ctr               | Число              | Коэффициент кликабельности (CTR).                                         |
| spent             | Число              | Сумма потраченных средств.                                                |
| clicks            | Число              | Количество кликов по объявлению.                                          |

