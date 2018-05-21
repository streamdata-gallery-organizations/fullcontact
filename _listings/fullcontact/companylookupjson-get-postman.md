{
  "info": {
    "name": "FullContact Get Company",
    "_postman_id": "c8f62517-113b-4208-a358-14daac1526a4",
    "description": "Get Company",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Companies",
      "item": [
        {
          "id": "dbd6e595-ba58-4f79-b56e-0b5a9b16c5e4",
          "name": "getCompany",
          "request": {
            "url": "http://api.fullcontact.com/company/lookup.json?apiKey=%7B%7D&callback=%7B%7D&domain=%7B%7D&keyPeople=%7B%7D&prettyPrint=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Get Company"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "7527a6a6-4330-4ebf-b5f0-702f614dd814"
            }
          ]
        }
      ]
    }
  ]
}