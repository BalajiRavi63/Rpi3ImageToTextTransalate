# Rpi3ImageToTextTransalate
This is a program that can be used in RPi3 in converting text present in images to characters and translating into a user defined language and publishing as audio output 



This is a program that involves usage of some python libraries namely,

1. gTTS

2. pytesseract

3. googletrans

4. PIL(Pillow)

5. Playsound

Installation:
Open the teminal/command prompt and type the following dependencies

pip install pytesseract
pip install gtts
pip install googletrans
pip install playsound

Optimized for RPi3 

Usage:

Firstly, the input image is converted into a text using pytesseract. 
pytesseract or Python-tesseract is a wrapper for google's Tesseract-OCR, and python installer package consist of both PIL and pytessaract.
Since many of the versions needs its own standalone package, it can be downloaded from the link 


 
https://github.com/tesseract-ocr/tesseract/wiki 


Next, we need to insert our excutable path to this python file which corresponds to pytesseract installed locally

 
Next, the input image which holds the text is converted into characters using pytesseract.image_to_string() Function and validated using print

then a object transalator is assigned to function call Transalator()

Library translator.translate() takes 3 args
1. input
2. source or input image language
3. destination or final transalated language, and validated.

Then an object is created to store the audio file generated out of gTTS and using playsound, the output audio file is played
automatically without the need of playing it from root folder.


Language Tested:
English to Tamil(Other languages are also supported, Change the arguments accordingly).
Accuracy rate:
text_to_string - depends upon quality of image and fonts.
gTTS - Accuracy is about 90% but on the other hand, the grammer refelcted upon obtained as transalation is not proper.

Tested Platform:
Windows 10 PC 
Raspberry Pi Model 3B

