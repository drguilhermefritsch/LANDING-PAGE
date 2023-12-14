<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Clínica de Cirurgia Plástica</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4; /* Cor de fundo suave */
            color: #333;
            background-image: url('sua-imagem-de-fundo.jpg'); /* Substitua com o URL da sua imagem de fundo sugestiva para a clínica de cirurgia plástica */
            background-size: cover;
            background-position: center;
            background-repeat: no-repeat;
        }
        header {
            text-align: center;
            padding: 20px;
            background-color: #3498db; /* Cor principal azul suave */
            color: #ffffff;
        }
        section {
            max-width: 600px;
            margin: auto;
            padding: 20px;
            background-color: rgba(255, 255, 255, 0.9); /* Fundo branco semi-transparente */
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            margin-top: 20px;
            border-radius: 5px;
            text-align: center;
        }
        .welcome-text {
            margin-bottom: 20px;
        }
        .social-links {
            text-align: center;
            margin-top: 20px;
        }
        .social-links a {
            display: inline-block;
            margin: 0 10px;
            text-decoration: none;
            color: #3498db; /* Cor de destaque azul suave */
        }
        .profile-picture {
            max-width: 100%;
            border-radius: 50%;
            margin-top: 20px;
        }
        .photo-feed {
            margin-top: 20px;
        }
        .photo-feed img {
            max-width: 100%;
            margin-bottom: 10px;
            border-radius: 5px;
        }
    </style>
</head>
<body>
    <header>
        <h1>Clínica de Cirurgia Plástica</h1>
        <p>Olá, seja bem-vindo à nossa central de agendamento.</p>
        <p>Basta clicar nos links de contato abaixo e você será atendido(a) pela nossa equipe.</p>
    </header>
    
    <section>
        <img class="profile-picture" src="sua-foto.jpg" alt="Sua Foto"> <!-- Substitua com o URL da sua própria foto -->
        
        <div class="social-links">
            <a href="https://api.whatsapp.com/send?phone=5551998877009" target="_blank">WhatsApp</a>
            <a href="https://www.instagram.com/drguilherme.fritsch" target="_blank">Instagram</a>
        </div>

        <div class="photo-feed" id="instagram-feed">
            <h2>Fotos do Feed do Instagram</h2>
        </div>

        <script>
            // Substitua 'SEU_ACCESS_TOKEN' com o token de acesso obtido no Portal de Desenvolvedores do Instagram
            const accessToken = '37260190450090;
            const userId = '@drguilherme.fritsch'; // 'self' para o próprio usuário

            // URL da API do Instagram para obter fotos do feed
            const apiUrl = `https://graph.instagram.com/v12.0/${userId}/media?fields=id,caption,media_type,media_url,thumbnail_url,permalink,timestamp&access_token=${accessToken}`;

            // Função para criar elementos de imagem e adicionar ao feed
            function addImageToFeed(imageUrl) {
                const img = document.createElement('img');
                img.src = imageUrl;
                img.alt = 'Foto do Instagram';
                document.getElementById('instagram-feed').appendChild(img);
            }

            // Solicitar fotos do feed do Instagram
            fetch(apiUrl)
                .then(response => response.json())
                .then(data => {
                    if (data.data) {
                        data.data.forEach(post => {
                            if (post.media_type === 'IMAGE') {
                                addImageToFeed(post.media_url);
                            }
                        });
                    }
                })
                .catch(error => console.error('Erro ao carregar feed do Instagram:', error));
        </script>
    </section>
</body>
</html>
