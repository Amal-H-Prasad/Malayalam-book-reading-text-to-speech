# Malayalam-book-reading-text-to-speech

To create a text-to-speech program for reading Malayalam books in Python, you would need to use a speech synthesis engine that supports the Malayalam language. One such engine is Google's Text-to-Speech (TTS), which can be accessed through the gTTS module in Python.

To use gTTS, you would need to first convert the text of the book into a string and then pass it as input to the gTTS function. The output of the function will be an audio file containing the synthesized speech.

To play the audio file, you can use the playsound module in Python. First, you would need to initialize playsound and load the audio file. Then, you can use the playsound("file name ") function to play the audio.

Overall, the program would involve three main steps: converting the text to speech using gTTS, saving the audio file, and playing the audio using playsound.


#code
import io
from gtts import gTTS
from playsound import playsound


fp=io.open("book.txt",mode="r",encoding="utf-8")
book_content=fp.read()
ob=gTTS(book_content,lang='ml')
ob.save("book.mp3")
playsound("book.mp3")
