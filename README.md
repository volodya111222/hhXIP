# hhXIPE

'''Python
import telebot
from telebot import types


bot = telebot.TeleBot('7689811901:AAG4kDTQhq5EM0jIJGjubyoFiKD50ZqnlaY')


@bot.message_handler(commands=['start'])
def start(message):
    markup = types.InlineKeyboardMarkup()

    file = open('ххэшка11.jpg', 'rb')
    bot.send_photo(message.chat.id, file, reply_markup=markup)

    button = types.InlineKeyboardButton(text='пройти проф тест!', callback_data='test')

    markup.add(button)

    bot.send_message(message.chat.id, 'приветсвтую тебя мой юный друг!'
                                      'до сих пор расстраиваещься что в 11 лет не получил заветное письмо из Хогвартса?'
                                      'не переживай, мы вместе с Ххэшкой поможем тебе найти свое призвание!', reply_markup=markup)
'''                                      
+ импортировал библиотеки, записал токен в пересенную, сделал ответ на команду старт с отправкой первого сообщения
---
                                      

    markup1 = types.InlineKeyboardMarkup()
    markup2 = types.InlineKeyboardMarkup()
    markup4 = types.InlineKeyboardMarkup()
    markup5 = types.InlineKeyboardMarkup()
    markup6 = types.InlineKeyboardMarkup()
    markup7 = types.InlineKeyboardMarkup()
    markup8 = types.InlineKeyboardMarkup()

    markup3 = types.InlineKeyboardMarkup()


    button1 = types.InlineKeyboardButton(text='Работать в команде', callback_data='жж')
    button2 = types.InlineKeyboardButton(text='Работать самостоятельно', callback_data='жж')
    button3 = types.InlineKeyboardButton(text='Я готов рисковать', callback_data='дд')
    button4 = types.InlineKeyboardButton(text='Я не люблю риск', callback_data='дд')
    button6 = types.InlineKeyboardButton(text='Kреативные задачи', callback_data='pp')
    button7 = types.InlineKeyboardButton(text='Логические задачи', callback_data='pp')
    button8 = types.InlineKeyboardButton(text='Лицом к лицу', callback_data='oo')
    button9 = types.InlineKeyboardButton(text='через мессенджер', callback_data='oo')
    button10 = types.InlineKeyboardButton(text='Я люблю изучать новое', callback_data='ii')
    button11 = types.InlineKeyboardButton(text='я не люблю учиться', callback_data='ii')
    button12 = types.InlineKeyboardButton(text='Гибкий график', callback_data='uu')
    button13 = types.InlineKeyboardButton(text='Стандартный график', callback_data='uu')
    button14 = types.InlineKeyboardButton(text='творческий подход', callback_data='yy')
    button15 = types.InlineKeyboardButton(text='финансовая стабильность', callback_data='yy')

    button5 = types.InlineKeyboardButton(text='жми!', url='http://hhstudenttest.tilda.ws/designer')
    
+ создал кнопки с их текстом

    markup1.add(button1, button2)
    markup2.add(button3, button4)
    markup4.add(button6, button7)
    markup5.add(button8, button9)
    markup6.add(button10, button11)
    markup7.add(button12, button13)
    markup8.add(button14, button15)
    markup3.add(button5)

+ добавил кнопки

    @bot.callback_query_handler(func=lambda call: True)
    def callback_inline(call):

        if call.data == 'test':
            bot.send_message(message.chat.id, 'Какой вид деятельности вам больше нравится?', reply_markup=markup1)

        if call.data == 'жж':
            bot.send_message(message.chat.id, 'Как вы относитесь к риску?', reply_markup=markup2)

        if call.data == 'дд':
            bot.send_message(message.chat.id, 'Какой тип задач вам более интересен?', reply_markup=markup4)

        if call.data == 'pp':
            bot.send_message(message.chat.id, 'Как вы предпочитаете общаться с людьми?', reply_markup=markup5)

        if call.data == 'oo':
            bot.send_message(message.chat.id, 'Как вы относитесь к обучению и саморазвитию?', reply_markup=markup6)

        if call.data == 'ii':
            bot.send_message(message.chat.id, 'Какой рабочий график вам больше подходит?', reply_markup=markup7)

        if call.data == 'uu':
            bot.send_message(message.chat.id, ' Что для вас важнее в работе?', reply_markup=markup8)


        if call.data == 'yy':
            bot.send_message(message.chat.id, 'дорогой друг! поздравляю тебя с успешно пройденным проф тестом! по результатам этого теста могу сказать, что тебе очень подойдут проффесии связанные с дизайном! подробнее ознакомиться со списком проффесий подходящей именно тебе ты модешь озннакомиться по ссылке ниже. переходи скорее!', reply_markup=markup3

bot.polling(none_stop=True, interval=0)
+ сделал ответы на кнопки, с отправкой последующих сообщений
