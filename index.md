<!DOCTYPE_5 html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Decolonization project_1</title>
</head>
<body>
    <form id="myForm">
        <label for="message">Message:</label><br>
        <input type="text" id="message" name="message"><br><br>
        <button type="submit">Send Message</button>
    </form>
    <script>
        document.getElementById('myForm').addEventListener('submit', function(e) {
            e.preventDefault();
            
            const message = document.getElementById('message').value; // Get the value of the text field
            
            const url = 'https://functions.yandexcloud.net/d4ejmqn8brddsad1npka'; // Specify the URL of your server to send the message
            const data = { message: message }; // Create an object for sending
            
            fetch(url, {
                method: 'POST',
                headers: {
                    'Content-Type': 'text/plain' 
                },
                body: JSON.stringify(data)
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
        });
    </script>
</body>
</html>
