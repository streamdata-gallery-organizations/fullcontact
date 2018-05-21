{
  "info": {
    "name": "FullContact Get Account Stats",
    "_postman_id": "9d7feac0-d958-4a09-82fb-2103ad479014",
    "description": "Get Account Stats",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Statistics",
      "item": [
        {
          "id": "493582d6-ba9e-49b1-8322-8d858bd569be",
          "name": "getAccountStats",
          "request": {
            "url": "http://api.fullcontact.com/stats.json?apiKey=%7B%7D&period=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Get Account Stats"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ab4c73eb-f32a-4534-aa9c-b9214054c96e"
            }
          ]
        }
      ]
    }
  ]
}