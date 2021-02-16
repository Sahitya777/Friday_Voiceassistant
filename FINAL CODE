import speech_recognition as sr
import pyttsx3
import pyjokes
import datetime
import random
import pywhatkit
import wikipedia
import webbrowser
import time
from translate import Translator
from gtts import gTTS
import os
import wolframalpha
import pyautogui
from pyfiglet import Figlet
from datetime import date

def friday():
    text = Figlet(font='digital')
    os.system('cls')
    os.system('mode con: cols=30 lines=15')
    print(text.renderText("FRIDAY"))



engine = pyttsx3.init('sapi5')


def take(text):
    engine.say(text)
    engine.runAndWait()

def wishme():
    hour = int(datetime.datetime.now().hour)
    if hour >= 0 and hour < 12:
        take("Good Morning Sir !")

    elif hour >= 12 and hour < 18:
        take("Good Afternoon Sir !")

    else:
        take("Good Evening Sir !")

    assname = ("Friday 1 point o")
    take("I am your Assistant")
    take(assname)
    take("How may i help you")

def talk(command):
    engine.say(command)
    engine.runAndWait()

def take_command():
    listener = sr.Recognizer()
    with sr.Microphone() as source:
        print("listening....")
        listener.pause_threshold = 1
        voice = listener.listen(source)
    try:
        command = listener.recognize_google(voice, language='en-in')
        command = command.lower()

    except Exception as e:
        print("Say the command again")
        return "None"
    return command

if __name__ == "__main__":
    friday()
    wishme()
    while True:
        command = take_command()

        if 'play' in command:
            song = command.replace('play', '')
            talk('playing'+song)
            pywhatkit.playonyt(song)
            time.sleep(10)

        elif 'time' in command:
            time = datetime.datetime.now().strftime('%H %M %p')
            print(time)
            talk("Current time is"+time)

        elif 'date' in command:
            date = date.today()
            print(date)
            talk(date)

        elif 'who is' in command:
            person = command.replace("who is", '')
            info = wikipedia.summary(person, 2)
            print(info)
            talk(info)

        elif 'joke' in command:
            joke = pyjokes.get_joke()
            print(joke)
            talk(joke)

        elif 'roll a dice' in command:
            choices = [1, 2, 3, 4, 5, 6]
            output = random.choice(choices)
            print(output)
            talk("The output is {}".format(output))

        elif 'flip a coin' in command:
            choices = ['Tails', 'Heads']
            output = random.choice(choices)
            print(output)
            talk("The outcome is"+output)

        elif 'are you single' in command:
            talk("sorry i have a girlfriend")
            print("Sorry I Have a girlfriend")

        elif "will you go on a date with me" in command:
            print("No i have Fever")
            talk("No i have fever")

        elif 'open youtube' in command:
            webbrowser.open("youtube.com")
            time.sleep(6)

        elif 'open google' in command:
            webbrowser.open("google.com")
            time.sleep(6)

        elif 'open stackoverflow' in command:
            webbrowser.open("stackoverflow.com")
            time.sleep(6)

        elif 'how are you' in command:
            print("I am fine,Thank you")
            talk("I am fine,Thank you")
            print("How are you?")
            talk("How are you?")

        elif "who created you"  in command:
            print("I was created by JV2S")
            talk("I was created by JV2S")

        elif 'who i am' in command:
            print("If you are talking and giving me commands then you are definitely human")
            talk("If you are talking and giving me commands then you are definitely human")

        elif "why you came to this world" in command:
            print("This is a secret i am not willing to tell")
            talk("This is a secret i am not willing to tell")

        elif "hello testing 123" in command:
            print("I am completely operational and all my circuits are working properly")
            talk("I am completely operational and all my circuits are working properly")

        elif "can i call you jarvis" in command:
            print("I think you have mistaken me for another intelligent assistant")
            talk("I think you have mistaken me for another intelligent assistant")
            print('Mr Stark is that you?')
            talk('Mr Stark is that you?')

        elif 'can you dance with me' in command:
            print("No these guilty feet have got no rhythm,Wait i have no feet")
            talk("No these guilty feet have got no rhythm,Wait i have no feet")

        elif "when will the world end" in command:
            print('''Well,Unix 32-bit time overflows
                        on January 19,2038.Maybe then,''')
            talk("Well,Unix 32-bit time overflows on January 19,2038.Maybe then,")

        elif 'how much wood would a woodchuck chuck if a woodchuck could chuck chuck wood' in command:
            talk("42?,That cant be right")
            print("42?,That cant be right")
            talk("How about another tongue twister")
            print("How about another tongue twister")
            take_command()
            if 'ok' in command:
                talk("""Peter Piper picked a peck of pickled pepper
                A peck of pickled peppers Peter Piper picked
                If Peter Piper picked a peck of pickled peppers
                Where’s the peck of pickled peppers Peter Piper picked?""")
                print("""Peter Piper picked a peck of pickled pepper
                A peck of pickled peppers Peter Piper picked
                If Peter Piper picked a peck of pickled peppers
                Where’s the peck of pickled peppers Peter Piper picked? """)
            else:
                print("Ok next time")
                talk("Ok next time")


        elif "exit" in command:
            print("Thanks for giving me your time")
            talk('Thanks for giving me your time')
            exit()

        elif "quit" in command:
            print("Thanks for giving me your time")
            talk('Thanks for giving me your time')
            exit()

        elif "where is" in command:
            command = command.replace("where is", "")
            location = command
            print("User asked to locate")
            talk("User asked to Locate")
            print(location.upper())
            talk(location)
            webbrowser.open("https://www.google.co.in/maps/place/" +command + "")
            time.sleep(6)

        elif "translate" in command:
            command = command.replace("translate", "")
            print("Which language do you want to translate in ?")
            talk("Which language do you want to translate in ?")
            command1 = take_command()

            if "german" in command1:
                translator = Translator(to_lang="German")
                translation = translator.translate(command)
                obs = gTTS(text=translation, lang='de', slow=False)
                obs.save('german.mp3')
                print("In German{} is {}".format(command, translation))
                talk("In German"+command+"is")
                os.system('german.mp3')
                time.sleep(3)

            elif 'french' in command1:
                translator = Translator(to_lang="French")
                translation = translator.translate(command)
                obs1 = gTTS(text=translation, lang='fr', slow=False)
                obs1.save("french.mp3")
                print("In French{} is {}".format(command, translation))
                talk("In French"+command+"is")
                os.system('french.mp3')
                time.sleep(3)

            elif 'italian' in command1:
                translator = Translator(to_lang="Italian")
                translation = translator.translate(command)
                obs2= gTTS(text=translation, lang='it', slow=False)
                obs2.save("italian.mp3")
                print("In Italian{} is {}".format(command, translation))
                talk("In Italian"+command+"is")
                os.system('italian.mp3')
                time.sleep(3)

            elif 'russian' in command1:
                translator = Translator(to_lang="Russian")
                translation = translator.translate(command)
                my = gTTS(text=translation, lang='ru', slow=False)
                my.save("russia.mp3")
                print("In Russian{} is {}".format(command, translation))
                talk("In Russian"+command+"is")
                os.system('russia.mp3')
                time.sleep(3)

            elif "japanese" in command1:
                translator = Translator(to_lang="Japanese")
                translation = translator.translate(command)
                my1 = gTTS(text=translation, lang='ja', slow=False)
                my1.save("japanese.mp3")
                print("In Japanese{} is {}".format(command, translation))
                talk("In Japanese"+command+"is")
                os.system('japanese.mp3')
                time.sleep(3)

            elif "hindi" in command1:
                translator = Translator(to_lang="Hindi")
                translation = translator.translate(command)
                myobj = gTTS(text=translation, lang='hi', slow=False)
                myobj.save("welcome.mp3")
                print("In Hindi{} is {}".format(command, translation))
                talk("In Hindi"+command+"is")
                os.system("welcome.mp3")
                time.sleep(3)

        elif "calculate" or 'what is' in command:
            question = command
            command = command.replace("calculate" or "add" or 'what is', "")
            client = wolframalpha.Client('Q25UJH-7HU99AVT32')
            res = client.query(question)
            answer = next(res.results).text
            print("The answer is " + answer)
            talk("The answer is " + answer)

        elif 'screenshot' in command:
            screenshot = pyautogui.screenshot()
            screenshot.save("screen.png")

        elif 'friday' in command:
            wishme()
