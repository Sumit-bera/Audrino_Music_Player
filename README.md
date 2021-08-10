# Audrino_Music_Player
Our project is to design and construct an Arduino based wireless music player system, to transmit stereo audio from a 3.5 mm jack to play on a pair of speakers. The Arduino in the circuit loads the .wav files from the micro-SD card. It then generates a signal and outputs it through the speaker connected to digital pin 9. This allows the speaker to create sounds and play music. We can also play/Pause the song by pressing the button connected to pin 5. Press it once to pause the song and press it again to play it from where it stopped and we can use the button attached with pin 7 for previous song and pin 6 for next song.

Digital music in the form of MP3 files has exploded in popularity the last few years. Today it is possible to store your whole music collection on a paper-thin card and take it with you anywhere. wireless music player System in which we can play audio file(.wav) on a pair of speakers from a micro-SD card. The Arduino in the circuit loads the .wav files from the micro-SD card. It then generates a signal and outputs it through the speaker connected to digital pin 9. This allows the speaker to create sounds and play music. It can effectively transmit and receive high quality audio (128 kbps) from a 3.5mm jack and play through speakers wirelessly. It is a low power device so that it can be powered with 9V battery and be small and portable. It can produce enough power to speakers to have “loud” music while limiting noise and distortion.
The purpose of project was based on making the wireless music player that is use to play music wirelessly. 
This wireless music player can play music wirelessly so this project can be use in different appliances like making a speaking clock, voice assistant, talking robot, voice alert security system and much more.

![image](https://user-images.githubusercontent.com/61411787/128812464-883675a1-fa7a-4bc0-9b02-642c04999b60.png)

![image](https://user-images.githubusercontent.com/61411787/128812523-0ddcc856-988d-4c90-a5ba-3b35456decf3.png)

We start with making the circuit according to the circuit diagram. The Arduino in the circuit loads the .wav files from the micro-SD card. It then generates a signal and outputs it through the speaker connected to digital pin 9. This allows the speaker to create sounds and play music.
the speaker is connected to Pins 9 and GND. Additionally, we need to connect SD Card Module and 3 Push Buttons.
Since the interface between Arduino UNO and SD Card Module is through SPI Communication, the connections the connections are as follows.
The CS Pin of SD Card Module is connected to Pin 4. Chip Select (CS) pin can be connected to any Digital I/O Pin but the rest of the SPI Pins of SD Card Module must be connected to corresponding SPI Pins of Arduino.
SCK or SPI Clock Pin of SD Card is connected to Pin 13 of Arduino. The MOSI and MISO pins of SD Card Module are connected to Pins 11 and 12 of Arduino UNO respectively.
The power pins i.e. VCC and GND are connected to +5V and GND of Arduino.
Additionally, we have used 3 push buttons to control the music playback. Play / Pause Button is connected to Pin 5, Next Track Button is connected to Pin 6 and Previous Track Button is connected to Pin 7 of Arduino. All these buttons are configured with internal pullups in the program.
We have to convert our audio / music files to WAV format i.e. they should be .wav files. This is because, the supporting libraries. So, our first step is to convert mp3 files to .wav files. For this we can use any audio converter software.
We have to follow the following steps given below to make songs compatible with your Arduino audio player: 
Upload a music file or enter a link for the song or audio file to be converted. 
1.	In optional settings, change bit resolution to 8 bits.
2.	Change sampling rate to 16000 Hz.
3.	Change audio channels to Mono.
4.	Click on "Show advanced options".
5.	Set the PCM format as PCM unsigned 8-bit.
 After making the above-mentioned changes, file will be converted and it’ll be compatible with Arduino. The second important thing is to add a special library called TMRpcm. This project also requires SPI and SD libraries. These are built-in libraries.
We have to format the microSD Card as FAT using any formatting software like SD Memory Card Formatter and copy all the WAV audio files to the card. Insert the card into the slot on the SD Card Module and make all the necessary connections. 
Then we Connect Arduino UNO to computer and in the Arduino IDE, and write the code. We have named all the audio files as song1.wav, song2.wav, etc. and used the same names in the function. 
