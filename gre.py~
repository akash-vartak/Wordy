#!/usr/bin/env python

from bs4 import BeautifulSoup
from requests import get
from random import randrange
import time
import os
import requests
import pyttsx   # text-to-speech library

def say(n) :
	e = pyttsx.init()   # initiates speech engine
	
	#use the following if you want to hear in random languages
	'''
	voices = e.getProperty('voices')
	i = randrange(0,len(voices))
	e.setProperty('voice', voices[i].id)
	'''
	#e.setProperty('rate',120)
	e.say(n) # loads text into engine
	e.runAndWait()   # THIS LINE IS IMPORTANT, runs the speech engine

say('Please wait')
#Generating request for the specific url
url = "https://quizlet.com/58647605/kaplan-900-flash-cards/"

htmldoc = get(url).text
#Extract the document from the request

soup = BeautifulSoup(htmldoc,'html.parser')
# soup is object of BeautifulSoup

wordlist = soup.find_all('span',{'class':'TermText qWord lang-en'})
meaningslist = soup.find_all('span',{'class':'TermText qDef lang-en'})

words = []
meanings = []		
		
for tag in wordlist:		
    words.append(tag.get_text())

for tag in meaningslist:
    meanings.append(tag.get_text())


index = randrange(0,737)
wo=words[index]
me=meanings[index]
w='"'+wo.upper()+'"'
m='"'+me.upper()+'"'
rest_command = "notify-send -i gre_logo.jpg "+w+" "+m
os.system(rest_command)

time.sleep(1)
say(words[index])
time.sleep(1)
say('Means: ')
say(meanings[index])

time.sleep(1)


say('This word has been added to list of learnt words.')
w='"'+wo+'"'
w="Word: "+w;
command="echo "+w+" >> learnt.txt"
os.system(command)

m='"'+me+'"'
m="Meaning: "+m;
command="echo "+m+" >> learnt.txt"
os.system(command)

line='"-----------------------"';
command="echo "+line+" >> learnt.txt"
os.system(command)


time.sleep(1)

say('Do you want to learn the pronunciation of a different word')
choice=raw_input("Do you want to learn the pronunciation of a different word?(y/n) ")
time.sleep(1)
if(choice=="y" or choice=="Y"):
	say('Enter a word below whose pronunciation you want to know: ')
	pronun=raw_input("Enter word here- ")
	time.sleep(1)
	say('pronounced as: ')
	say(pronun)
	time.sleep(1)
	
	m="Asked pronunciation of: "+pronun;
	m='"'+m+'"'
	command="echo "+m+" >> learnt.txt"
	os.system(command)
	
	line='"-----------------------"';
	command="echo "+line+" >> learnt.txt"
	os.system(command)

print "File containing learnt words is learnt.txt

