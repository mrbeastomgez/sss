<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Crime Revealer</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            margin-top: 50px;
            background-color: #f0f0f0;
        }
        .container {
            max-width: 800px;
            margin: 0 auto;
            padding: 20px;
            background-color: white;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
        }
        button {
            padding: 10px 20px;
            font-size: 16px;
            margin: 10px;
            cursor: pointer;
            background-color: #4CAF50;
            color: white;
            border: none;
            border-radius: 5px;
            transition: background-color 0.3s;
        }
        button:hover {
            background-color: #45a049;
        }
        #crimeImage {
            max-width: 100%;
            margin-top: 20px;
            display: none;
            border-radius: 5px;
        }
        #secondButton {
            display: none;
        }
        .warning {
            color: red;
            font-weight: bold;
            margin: 20px 0;
            display: none;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Welcome to Crime Revealer</h1>
        <p>This website reveals shocking crime evidence. Proceed with caution.</p>
        <p class="warning" id="warningText">WARNING: The following content may be disturbing</p>
        
        <button id="firstButton">Click to see crime</button>
        <button id="secondButton">Really want to see crime? Click on it</button>
        
        <img id="crimeImage" src="https://media.discordapp.net/attachments/1297992278652227666/1353846224872276071/IMG_1601.png?ex=67e3230d&is=67e1d18d&hm=087c38df6e5171e4497b86e9a4dd7e58525b34cd82c406137e6614269d76c09d&=&format=webp&quality=lossless&width=458&height=900" alt="Crime photo">
    </div>

    <script>
        const firstButton = document.getElementById('firstButton');
        const secondButton = document.getElementById('secondButton');
        const crimeImage = document.getElementById('crimeImage');
        const warningText = document.getElementById('warningText');

        firstButton.addEventListener('click', function() {
            firstButton.style.display = 'none';
            secondButton.style.display = 'inline-block';
            warningText.style.display = 'block';
        });

        secondButton.addEventListener('click', function() {
            secondButton.style.display = 'none';
            crimeImage.style.display = 'block';
            warningText.style.display = 'none';
        });
    </script>
</body>
</html>
