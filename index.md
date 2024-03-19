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

    <div class="container">
		<div id="fh5co-intro">
			<div class="row animate-box">
				<div class="col-md-8 col-md-offset-2 col-md-pull-2">
					<h2>Contact Us</h2>
				</div>
			</div>
		</div>
		<div id="fh5co-contact">
			<div class="row">
				<div class="col-md-4 animate-box">
					<h3>Contact Information</h3>
					<ul class="contact-info">
						<li><i class="icon-location4"></i>198 West 21th Street, Suite 721 New York NY 10016</li>
						<li><i class="icon-phone3"></i>+ 1235 2355 98</li>
						<li><i class="icon-location3"></i><a href="#">info@yoursite.com</a></li>
						<li><i class="icon-globe2"></i><a href="#">www.yoursite.com</a></li>
					</ul>
				</div>
				<div class="col-md-8 animate-box">
					<div class="form-wrap">
						<div class="row">
							<div class="col-md-12">
								<div class="form-group">
									<input type="text" class="form-control" placeholder="Name">
								</div>
							</div>
							<div class="col-md-12">
								<div class="form-group">
									<input type="text" class="form-control" placeholder="Email">
								</div>
							</div>
							<div class="col-md-12">
								<div class="form-group">
									<textarea name="" class="form-control" id="" cols="30" rows="15" placeholder="Message"></textarea>
								</div>
							</div>
							<div class="col-md-12">
								<div class="form-group">
									<input type="submit" value="Send Message" class="btn btn-primary btn-modify">
								</div>
							</div>
						</div>
					</div>
				</div>
			</div>
		</div>
	</div><!-- END container -->




<script>
    document.getElementById('myForm').addEventListener('submit', function(e) {
        e.preventDefault();
        
        const message = document.getElementById('message').value; // Получаем значение текстового поля
        
        const url = 'https://functions.yandexcloud.net/d4ejmqn8brddsad1npka'; // Укажите URL вашего сервера, на который будет отправляться сообщение
        const data = { message: message }; // Создаем объект для отправки
        
        fetch(url, {
            method: 'POST',
            headers: {
                'Content-Type': 'application/json' // Устанавливаем тип контента как JSON
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
    });
</script>

</body>
</html>
