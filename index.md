<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Decolonization project</title>
</head>
<body>
    <h1>Decolonization project</h1>
    <img src="main/map.jpg" alt="Map of the project" width="500">
{
  "schema": {
    "message": {
      "type": "string",
      "title": "Сообщение"
    },
    "author": {
      "type": "object",
      "title": "Автор",
      "properties": {
        "name": {
          "type": "string",
          "title": "Имя"
        },
        "gender": {
          "type": "string",
          "title": "Пол",
          "enum": [ "male", "female", "alien" ]
        },
        "magic": {
          "type": "integer",
          "title": "Магический номер",
          "default": 42
        }
      }
    }
  }
}
    
</body>
</html>
