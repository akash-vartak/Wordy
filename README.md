# Wordy
Wordy is your personal vocabulary trainer.

Meet Wordy, your new vocabulary trainer.  <br>
All you need to do is run 
`python gre.py`
 and Wordy will look up a random word and display the word and it's meaning as a pop notification.  <br>
Another feature, specialy for non-native speakers of the English language, is the pronunciation tool :sound:.
After scraping for a word, and displaying it, Wordy will also pronounce the word and the meaning. It shall also ask you if there is
another word whose pronunciation you want.

The words looked up are stored in the text file: `learnt.txt` within the same directory as the code `gre.py`

##Usage
1. Download the zip of this repository or  <br>
`git clone https://github.com/akash-vartak/Wordy`  <br>
2. Change to root login via `sudo -i` *Ubuntu*  <br>
or `su`
3. `sh install_dependencies.sh` This shall install the required libraries, namely **BeautifulSoup** and **pyttsx**
4. Now you can easily use `python gre.py` and run Wordy

##Libraries
I have used the BeautifulSoup4 and pyttsxlibraries for scraping and audio(pronunciations) respectively.

##Contribution
Issues and Pull requests are always welcome. Please send in any suggestions too.  <br>
Also, don't forget to fork and star this repository. :smile:

####Future Work
I made this repostory to primarily help me in improving my vocabulary and simultaneously my scriping skills.  <br>
Thus the further improvement of the script is stopped as of now. Although you are welcome to work on it as you please.

##License
Released under the MIT License
