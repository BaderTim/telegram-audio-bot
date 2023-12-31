# telegram-audio-bot
This Telegram bot can transcribe audio and voice messages to text. It is written in Python 3 and uses the OpenAI API to transcribe recordings with their [Whisper](https://openai.com/research/whisper) model.

![Demo image](./media/demo.png)

## Usage
1. Clone the repository
2. Install the requirements listed in ``requirements.txt`` with ``pip3 install -r requirements.txt``
3. Create a Telegram bot with [BotFather](https://t.me/botfather)
4. Create a ``.env`` file in the project root directory with the following content:
    ```
    TELEGRAM_BOT_API_KEY=<your_key_here>
    OPENAI_API_KEY=<your_key_here>
    ```
5. Run the bot with ``python3 bot.py``

## Changing the target language
You can change the target language by modifying the OpenAI transcribe API call in the ``transcribe`` function in ``bot.py``. The default target language is German (``de``). 

## Cost
Because the bot uses the OpenAI API, it is not free to use. At the date of writing this, each minute of audio transcription costs 0.006 USD. You can find more information about the pricing [here](https://openai.com/pricing).