# BOT-TELEGRAM
criação de bot para o telegram

## pip install telebot
## Conectar a chave API DO TELEGRAM







Para descobrir o API Token do Telegram e criar um bot, siga estes passos:

1. Crie um Bot no Telegram
Você precisará usar o BotFather, que é o bot oficial do Telegram para criar outros bots.

Passo a Passo:
Abra o aplicativo Telegram e procure por "BotFather" na barra de busca.
Inicie uma conversa com o BotFather.
Digite /start para começar.
Digite /newbot para criar um novo bot.
O BotFather pedirá para você dar um nome ao seu bot. Escolha um nome de exibição (pode ser qualquer nome).
Depois, ele pedirá um username para o bot. Esse nome precisa ser único e terminar com "bot" (ex: meubot_legal_bot).
Após definir o nome e o username, o BotFather irá gerar uma mensagem com o Token da API. Essa mensagem terá um formato como:
kotlin
Copiar código
Use this token to access the HTTP API:
123456789:ABCdefGhIjklMnOpqRsTuVwxyz-123456789
Esse é o Token da API que você utilizará no seu script para interagir com o Telegram.

2. Salve o Token
Cuidado: Nunca compartilhe esse token em público, pois qualquer pessoa que tiver acesso a ele pode controlar seu bot.
Você pode copiar esse token e usá-lo no código Python que você criar.
Exemplo de uso do Token no Python:
python
Copiar código
import telebot

API_TOKEN = '123456789:ABCdefGhIjklMnOpqRsTuVwxyz-123456789'  # Seu token aqui
bot = telebot.TeleBot(API_TOKEN)

@bot.message_handler(commands=['start'])
def send_welcome(message):
    bot.reply_to(message, "Bem-vindo ao meu bot!")

bot.polling()
Com o token, você pode começar a desenvolver seu bot e interagir com a API do Telegram.
