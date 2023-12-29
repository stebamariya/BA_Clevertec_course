## REST API Endpoints
- **Endpoint:** `http://93.84.86.69:9099/news_applications/v1/news`
### POST

**Description:** Создание новости

**Request:**
- Method: `POST`
- Headers:
    - Content-Type: application/json
- Body:
  ```json
  {
    "title": "Открытие нового экологического парка в центре города. 29.12.2023",
    "text": "Сегодня в центре города открыт новый экологический парк, который стал уникальным оазисом зелени в суете городской жизни. Парк предлагает посетителям уютные аллеи, современные детские площадки, а также специальные зоны для пикника. Важным моментом является использование экологически чистых материалов в строительстве парка и поддержание биоразнообразия на его территории.",
    "userName": "Мария Стеба"
  }
  ```

**Response:**
- Status: `201 Created`
- Body:
  ```json
  {
    "id": 152,
    "title": "Открытие нового экологического парка в центре города. 29.12.2023",
    "text": "Сегодня в центре города открыт новый экологический парк, который стал уникальным оазисом зелени в суете городской жизни. Парк предлагает посетителям уютные аллеи, современные детские площадки, а также специальные зоны для пикника. Важным моментом является использование экологически чистых материалов в строительстве парка и поддержание биоразнообразия на его территории.",
    "userName": "Мария Стеба",
    "time": "2023-12-29T20:19:25.403046774"
  }
  ```

### GET

**Описание:** Получение новостей от сервиса

**Endpoint:** `?keyword=%25%25&pageNo=0&pageSize=5&sortBy=id` (использовать параметры запроса)

**Request:**
- Method: `GET`

**Response:**
- Status: `200 OK`
- Body:
  ```json
  [
    {
      "id": 1,
      "title": "Economy resumes growth",
      "text": "After several months of decline, the economy is finally showing signs of recovery",
      "userName": "Jak",
      "time": "1970-01-01T09:15:00"
    },
    {
      "id": 2,
      "title": "New electric vehicle sales record",
      "text": "More electric vehicles sold this month than ever before",
      "userName": "Artur",
      "time": "1970-01-01T12:20:30"
    },
    {
      "id": 3,
      "title": "Economy resumes growth!",
      "text": "After several months of decline, the economy is finally showing signs of recovery",
      "userName": "The name of the user who created the news",
      "time": "1970-01-01T19:06:15.292016"
    },
    {
      "id": 4,
      "title": "Technological innovations in healthcare",
      "text": "New technologies can significantly reduce healthcare costs and make it more efficient",
      "userName": "Jan",
      "time": "1970-01-01T14:40:45"
    },
    {
      "id": 5,
      "title": "Celebration of the city's day",
      "text": "Today the city celebrates its birthday, celebrations will take place in all districts of the city",
      "userName": "Judi",
      "time": "1970-01-01T08:00:10"
    }
  ]
  ```

### DELETE

- **Description:** Удаление новости на английском языке.
- **Endpoint:** `http://{{BA-clevertec-cource-domen}}/news_applications/v1/news/145`
- **Request:**
    - Method: `DELETE`
- **Response:**
    - Status: `200`


### КОЛЛЕКЦИЯ В POSTMAN
```json
{
  "info": {
    "_postman_id": "0491d9c1-fd7b-41d1-84a0-b40c0bc67b08",
    "name": "Clevertec_API",
    "schema": "https://schema.getpostman.com/json/collection/v2.1.0/collection.json",
    "_exporter_id": "4533147"
  },
  "item": [
    {
      "name": "Получение новостей",
      "request": {
        "method": "GET",
        "header": [],
        "url": {
          "raw": "http://{{BA-clevertec-cource-domen}}/news_applications/v1/news?keyword=%25%25&pageNo=0&pageSize=5&sortBy=id",
          "protocol": "http",
          "host": [
            "{{BA-clevertec-cource-domen}}"
          ],
          "path": [
            "news_applications",
            "v1",
            "news"
          ],
          "query": [
            {
              "key": "keyword",
              "value": "%25%25"
            },
            {
              "key": "pageNo",
              "value": "0"
            },
            {
              "key": "pageSize",
              "value": "5"
            },
            {
              "key": "sortBy",
              "value": "id"
            }
          ]
        }
      },
      "response": []
    },
    {
      "name": "Создание новости",
      "request": {
        "method": "POST",
        "header": [],
        "body": {
          "mode": "raw",
          "raw": "{\r\n    \"title\": \"Открытие нового экологического парка в центре города. 29.12.2023\",\r\n    \"text\": \"Сегодня в центре города открыт новый экологический парк, который стал уникальным оазисом зелени в суете городской жизни. Парк предлагает посетителям уютные аллеи, современные детские площадки, а также специальные зоны для пикника. Важным моментом является использование экологически чистых материалов в строительстве парка и поддержание биоразнообразия на его территории.\",\r\n    \"userName\": \"Мария Стеба\"\r\n}",
          "options": {
            "raw": {
              "language": "json"
            }
          }
        },
        "url": {
          "raw": "http://{{BA-clevertec-cource-domen}}/news_applications/v1/news",
          "protocol": "http",
          "host": [
            "{{BA-clevertec-cource-domen}}"
          ],
          "path": [
            "news_applications",
            "v1",
            "news"
          ]
        }
      },
      "response": []
    },
    {
      "name": "Удаление новости",
      "request": {
        "method": "DELETE",
        "header": [],
        "url": {
          "raw": "http://{{BA-clevertec-cource-domen}}/news_applications/v1/news/145",
          "protocol": "http",
          "host": [
            "{{BA-clevertec-cource-domen}}"
          ],
          "path": [
            "news_applications",
            "v1",
            "news",
            "145"
          ]
        }
      },
      "response": []
    }
  ],
  "variable": [
    {
      "key": "BA-clevertec-cource-domen",
      "value": "93.84.86.69:9099"
    }
  ]
}
  ```