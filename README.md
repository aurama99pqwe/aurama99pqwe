<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Petal Blog</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background: #f8f0f5;
            color: #333;
            overflow-x: hidden; /* Prevent horizontal scroll due to animations */
        }
        header {
            background: #d81b60;
            color: white;
            padding: 1rem;
            text-align: center;
        }
        .container {
            margin: 2rem auto;
            max-width: 800px;
            padding: 1rem;
            background: white;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            border-radius: 8px;
        }
        footer {
            text-align: center;
            padding: 1rem;
            margin-top: 2rem;
            background: #d81b60;
            color: white;
        }
        /* Petals animation */
        .petal {
            position: fixed;
            top: -10%;
            width: 15px;
            height: 15px;
            background: pink;
            border-radius: 50%;
            opacity: 0.8;
            animation: fall 10s linear infinite;
        }
        .petal:nth-child(odd) {
            background: #f06292;
        }
        @keyframes fall {
            0% {
                transform: translateX(0) rotate(0deg);
                opacity: 1;
            }
            100% {
                transform: translateX(-300px) rotate(360deg);
                top: 110%;
                opacity: 0.5;
            }
        }
    </style>
</head>
<body>
    <header>
        <h1>Welcome to My Petal Blog</h1>
    </header>
    <div class="container">
        <h2>Blog Post Title</h2>
        <p>
            This is an example of a simple blog with falling petals in the background.
            You can replace this text with your own content.
        </p>
        <p>
            Enjoy the soft, soothing visuals of petals gently falling as you read through your content.
        </p>
    </div>
    <footer>
        <p>© 2025 My Petal Blog</p>
    </footer>

    <!-- Falling petals script -->
    <script>
        for (let i = 0; i < 50; i++) {
            let petal = document.createElement('div');
            petal.className = 'petal';
            petal.style.left = Math.random() * 100 + '%';
            petal.style.animationDuration = Math.random() * 5 + 5 + 's';
            petal.style.animationDelay = Math.random() * 5 + 's';
            document.body.appendChild(petal);
        }
    </script>
</body>
</html>
