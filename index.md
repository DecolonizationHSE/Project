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


    <form id="myForm">
        <label for="message">Message:</label><br>
        <input type="text" id="message" name="message"><br><br>
        <button type="submit">Send Message</button>
    </form>

<script>
    document.getElementById('myForm').addEventListener('submit', function(e) {
        e.preventDefault();
        
        const message = document.getElementById('message').value; // Получаем значение текстового поля
        
        const url = 'https://functions.yandexcloud.net/d4ejmqn8brddsad1npka'; // Укажите URL вашего сервера, на который будет отправляться сообщение
        const data = { message: message }; // Создаем объект для отправки
        
       fetch(url, {
    method: 'POST',
    headers: {
        'Content-Type': 'text/plain'  // Используем 'application/json' для типа содержимого
    },
    body: JSON.stringify(data) // Преобразуем объект в формат JSON
})
.then(response => {
    if (response.ok) {
        alert('Message sent successfully!');
    } else {
        alert('Failed to send message.');
    }
})
.catch(error => {
    console.error('Error:', error);
});
</script>
</body>
</html>
