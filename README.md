function sendTelegramNotify() {
  var token = '7918251682:AAGNtWYMx0U114MFV9TcCFc4NsDHV7K24ZM'; // ใส่ Telegram bot token
  var chatId = '8055798952'; // ใส่ chat ID

  var message = 'AC MAILFAIL'; // ข้อความที่จะส่ง

  var telegramUrl = 'https://api.telegram.org/bot' + token + '/sendMessage';

  var payload = {
    'chat_id': chatId,
    'text': message,
    'parse_mode': 'Markdown'
  };

  var options = {
    'method': 'post',
    'contentType': 'application/json',
    'payload': JSON.stringify(payload)
  };

  UrlFetchApp.fetch(telegramUrl, options);
}
