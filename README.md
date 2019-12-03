import telebot

bot =telebot.TeleBot('857633506:AAF84MVTquRerTID3JvTiLKrNW1xMJA6RdI')

@bot.message_handler(commands=["inicia"])
def send_welcome (message):
    print(messange)
    chatid= message.chat.id
    nombreUsuiario = message.chat.first_name+"  "+message.chat.last_name
    saludo = "hola,Bienvenido"
    bot.send_messsage(chatind,saludo.format (nombre=nombreUsuario))

@bot.message_handler(commands=["hola"])
def send_welcome(message):
    chatid = message.chat.id
    saludo = "HOLA DAVID, ESTE ES UN NUEVO COMANDO"
    bot.send_message(chatid,saludo)

@bot.message_handler(func=lambda message: True)
def echo_all(message):
    chatid = message.chat.id
    bot.send_message(chatid,"FUNCIONA SOLO CON COMANDOS /INICIA /HELP /HOLA")



print("EL PROGRAMA SE ESTA EJECUTANDO")
bot.polling()
