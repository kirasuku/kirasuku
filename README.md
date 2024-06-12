<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Abdul Fazil's Personal Webpage</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
            color: #333;
        }
        header {
            background-color: #333;
            color: #fff;
            padding: 10px 0;
            text-align: center;
        }
        .container {
            width: 80%;
            margin: 0 auto;
            padding: 20px;
            background-color: #fff;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        h1, h2 {
            color: #333;
        }
        .about-me, .contact {
            margin: 20px 0;
        }
        footer {
            text-align: center;
            padding: 10px 0;
            background-color: #333;
            color: #fff;
            position: fixed;
            bottom: 0;
            width: 100%;
        }
        .overlay {
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background-color: rgba(0, 0, 0, 0.8);
            display: flex;
            justify-content: center;
            align-items: center;
            color: #fff;
            z-index: 1000;
        }
        .overlay button {
            margin: 0 10px;
            padding: 10px 20px;
            font-size: 16px;
            cursor: pointer;
            border: none;
            background-color: #444;
            color: #fff;
        }
        .hidden {
            display: none;
        }
        .message {
            text-align: center;
            font-size: 24px;
            color: #fff;
        }
    </style>
</head>
<body>

<div class="overlay" id="language-selection">
    <div>
        <p>English or Spanish?</p>
        <button onclick="selectLanguage('english')">English</button>
        <button onclick="selectLanguage('spanish')">Spanish</button>
    </div>
</div>

<div class="overlay hidden" id="gay-question">
    <div>
        <p>Are you gay?</p>
        <button onclick="answerGayQuestion('yes')">Yes</button>
        <button onclick="answerGayQuestion('no')">No</button>
    </div>
</div>

<div class="overlay hidden" id="gay-pedophile-question">
    <div>
        <p>Are you a gay pedophile?</p>
        <button onclick="answerGayPedophileQuestion('yes')">Yes</button>
        <button onclick="answerGayPedophileQuestion('no')">No</button>
    </div>
</div>

<div class="overlay hidden" id="final-message">
    <div class="message">
        <p>GAMBERE GAMBERE</p>
    </div>
</div>

<header>
    <h1 id="name">Abdul Fazil</h1>
    <p id="nickname">Papa's Boy</p>
</header>

<div class="container">
    <section class="about-me">
        <h2 id="about-title">About Me</h2>
        <p id="about-content">I'm also gay and since you've reached here, we can be a gay couple now, please contact me via below contact.</p>
    </section>

    <section class="contact">
        <h2 id="contact-title">Contact</h2>
        <p id="contact-content">If you wish to reach out to me, please use the following contact information:</p>
        <ul id="contact-info">
            <li>Email: batman@fiji.com</li>
            <li>Phone: (679) 2970634</li>
        </ul>
    </section>
</div>

<footer>
    <p>&copy; 2024 Abdul Fazil. All rights reserved.</p>
</footer>

<script>
    function selectLanguage(language) {
        var elements = {
            name: document.getElementById('name'),
            nickname: document.getElementById('nickname'),
            aboutTitle: document.getElementById('about-title'),
            aboutContent: document.getElementById('about-content'),
            contactTitle: document.getElementById('contact-title'),
            contactContent: document.getElementById('contact-content'),
            contactInfo: document.getElementById('contact-info')
        };
        
        if (language === 'spanish') {
            elements.name.textContent = 'Abdul Fazil';
            elements.nickname.textContent = 'Papa\'s Boy';
            elements.aboutTitle.textContent = 'Sobre mí';
            elements.aboutContent.textContent = 'También soy gay y, dado que has llegado hasta aquí, podemos ser una pareja gay ahora. Por favor, contáctame a través de la información de contacto a continuación.';
            elements.contactTitle.textContent = 'Contacto';
            elements.contactContent.textContent = 'Si deseas comunicarte conmigo, utiliza la siguiente información de contacto:';
            elements.contactInfo.innerHTML = '<li>Correo electrónico: batman@fiji.com</li><li>Teléfono: (679) 2970634</li>';
        } else {
            elements.name.textContent = 'Abdul Fazil';
            elements.nickname.textContent = 'Papa\'s Boy';
            elements.aboutTitle.textContent = 'About Me';
            elements.aboutContent.textContent = 'I\'m also gay and since you\'ve reached here, we can be a gay couple now, please contact me via below contact.';
            elements.contactTitle.textContent = 'Contact';
            elements.contactContent.textContent = 'If you wish to reach out to me, please use the following contact information:';
            elements.contactInfo.innerHTML = '<li>Email: batman@fiji.com</li><li>Phone: (679) 2970634</li>';
        }
        
        document.getElementById('language-selection').classList.add('hidden');
        document.getElementById('gay-question').classList.remove('hidden');
    }

    function answerGayQuestion(answer) {
        if (answer === 'yes') {
            document.getElementById('gay-question').classList.add('hidden');
            document.getElementById('gay-pedophile-question').classList.remove('hidden');
        } else {
            alert("You cannot proceed further.");
        }
    }

    function answerGayPedophileQuestion(answer) {
        if (answer === 'yes') {
            document.getElementById('gay-pedophile-question').classList.add('hidden');
            document.getElementById('final-message').classList.remove('hidden');
            setTimeout(function() {
                document.getElementById('final-message').classList.add('hidden');
            }, 3000); // Show message for 3 seconds before hiding it
        } else {
            alert("You cannot proceed further.");
        }
    }
</script>

</body>
</html>
