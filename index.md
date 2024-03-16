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
            const formData = new FormData(this);
            fetch('https://functions.yandexcloud.net/d4ejmqn8brddsad1npka', {
                method: 'POST',
                body: formData
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
