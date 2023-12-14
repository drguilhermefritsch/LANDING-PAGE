# LANDING-PAGE<!DOCTYPE html>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Clínica de Cirurgia Plástica - Dr. Guilherme Fritsch</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f8f8f8;
            color: #333;
        }
        header {
            text-align: center;
            padding: 20px;
            background-color: #2c3e50; /* Cor principal do site www.fritschnunes.com */
            color: #ecf0f1;
        }
        section {
            max-width: 600px;
            margin: auto;
            padding: 20px;
            background-color: #ffffff;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            margin-top: 20px;
            border-radius: 5px;
        }
        form {
            display: grid;
            grid-gap: 10px;
        }
        label {
            font-weight: bold;
        }
        input, textarea, select {
            width: 100%;
            padding: 10px;
            margin-top: 5px;
            margin-bottom: 10px;
            box-sizing: border-box;
        }
        button {
            background-color: #e74c3c; /* Cor de destaque do site www.fritschnunes.com */
            color: white;
            padding: 10px 15px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        .social-links {
            margin-top: 20px;
            text-align: center;
        }
        .social-links a {
            display: inline-block;
            margin: 0 10px;
            text-decoration: none;
            color: #3498db; /* Cor de destaque do site www.fritschnunes.com */
        }
    </style>
</head>
<body>
    <header>
        <h1>Clínica de Cirurgia Plástica - Dr. Guilherme Fritsch</h1>
        <p>Agende sua consulta conosco!</p>
    </header>
    
    <section>
        <form>
            <label for="nome">Nome:</label>
            <input type="text" id="nome" name="nome" required>

            <label for="email">E-mail:</label>
            <input type="email" id="email" name="email" required>

            <label for="telefone">Telefone:</label>
            <input type="tel" id="telefone" name="telefone" required>

            <label for="mensagem">Mensagem:</label>
            <textarea id="mensagem" name="mensagem" rows="4"></textarea>

            <button type="submit">Agendar Consulta</button>
        </form>

        <div class="social-links">
            <a href="https://api.whatsapp.com/send?phone=5551998877009" target="_blank">WhatsApp</a>
            <a href="http://www.fritschnunes.com" target="_blank">Site Oficial</a>
            <a href="https://www.instagram.com/drguilherme.fritsch" target="_blank">Instagram</a>
        </div>
    </section>
</body>
</html>
