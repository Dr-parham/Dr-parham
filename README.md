import sys
import cowsay 
import time
import os
import socket
from pytube import YouTube
from pygame import mixer
from playsound import playsound
def text():
	print ('\n'+'\t'*2+'??'*65)
	print ('\t'*2+'*'+'\t'*10+' \t'*1+'                                         '+'?')
	print ('\t'*2+'*'+'\t'*10+' \t'*1+'                                         '+'?') 
	print ('\t'*2+'*'+'\t'*1+'   _____                             _____     ____                                  _____  '' \t'*1+'                         '+'?')
	print ('\t'*2+'*'+'\t'*1+'   \    \                           /    /    |    |                                |     | '' \t'*1+'                         '+'?')
	print ('\t'*2+'*'+'\t'*1+'    \    \                         /    /     |    |                                |     | '' \t'*1+'                         '+'?')
	print ('\t'*2+'*'+'\t'*1+'     \    \                       /    /      |    |                                |     | '' \t'*1+'                         '+'?')
	print ('\t'*2+'*'+'\t'*1+'      \    \        ____         /    /       |    |                                |     | '' \t'*1+'                         '+'?')
	print ('\t'*2+'*'+'\t'*1+'       \    \      /     \      /    /        |    |                           ======     ===== '' \t'*1+'                 '+'?')
	print ('\t'*2+'*'+'\t'*1+'        \    \    /       \    /    /         |    |                           |               | ''                        '+'?')
	print ('\t'*2+'*'+'\t'*1+'         \    \  /         \  /    /          |    |                           ======     ======                         '+'?')
	print ('\t'*2+'*'+'\t'*1+'          \    \/    /\     \/    /           |    |__________        @@@@          |     | '' \t'*1+'                         '+'?')
	print ('\t'*2+'*'+'\t'*1+'           \        /  \         /            |               |     @@@@@@@@        |     | '' \t'*1+'                         '+'?')
	print ('\t'*2+'*'+'\t'*1+'            \      /    \       /             |               |    @@@@@@@@@@       |     | '' \t'*1+'                         '+'?')
	print ('\t'*2+'*'+'\t'*1+'             \    /      \     /              |    ________   |   @@@      @@@      |     | '' \t'*1+'                         '+'?')
	print ('\t'*2+'*'+'\t'*1+'              \__/        \___/               |   |        |  |   @@@      @@@      |     | '' \t'*1+'                         '+'?')
	print ('\t'*2+'*'+'\t'*1+'                                              |   |        |  |   @@@      @@@      |     | '' \t'*1+'                         '+'?')
	print ('\t'*2+'*'+'\t'*1+'                                              |   |        |  |    @@@@@@@@@@@ @    |     | '' \t'*1+'                         '+'?')
	print ('\t'*2+'*'+'\t'*1+'                                              |___|        |__|       @@@@@     @   |_____| '' \t'*1+'                         '+'?')
	print ('\n'+'\t'*2+'??'*65)

def help(what):
	say = cowsay.daemon('Heyyyyyyyyyyyyyy bro what do you want to do just say me')
	print (say)

def remove():
	while  True:
		try:
			rm = input('\t \t What is your path file :')
			rm2 = os.remove(rm)
			print ('\t \t Delete !!!')
		except Exception as e:
			print ('\t \t sorry but can\'t found flie maby path is incorrect !!!')
			break

def rename():
	while  True:
		try:
			re = input('\t \t What is your file names :')
			re1 = input('\t \t New name : ')
			re2 = os.rename(re, re1)
			print ('\t \t rename !!!')
		except Exception as e:
			print ('\t \t sorry but can\'t found flie maby path is incorrect !!!')
			break
def IP():
	while True:
		try:
			na = input('\t \t Just enter the site : ')
			na1 =  socket.gethostbyname(na)
			print('\t \t ', na1)
		except Exception as e:
			print('\t \t sorry site it not find')
			break

def date():
	print ('\t \t ', time.sleep(2))
	print ('\t \t', time.ctime())

def read():
	while True:
		try:
			r = input('\t \t Enter the path with domain : ')
			with open(r) as r1 :
				print('\t \t ', r1.read())
		except Exception as e:
			print ('\t \t sorry but can\'t found flie maby path is incorrect !!!')
			break			

def calculator():
	while True:
		num1 = input('\t \t Enter your first number : ')
		num2 = input('\t \t Enter your second number : ')
		operation = input('\t \t Enter the operation : +, -, *, / : ')
		if operation == '+':
			int = num1
			int = num2
			print('\t \t', num1+num2)
		elif operation == '-':
			int = num1
			int = num2
			print('\t \t', num1-num2)
		elif operation == '*':
			int = num1
			int = num2
			print('\t \t', num1*num2)			
		elif operation == '/':
			int = num1
			int = num2
			print('\t \t', num1/num2)
		else:
			print ('\t \t sorry we don\'t have this option')
			break
def passwordlist():
	name = input('\t \t Enter the name :')
	birth = input('\t \t Enter birth year with month and day :')
	number = input('\t \t Enter the some number like phone number or another number :')
	one = name + birth + number 
	tow = name + number + birth 
	three = birth + name + number
	four = birth + number + name
	five = number + name + birth
	six = number + birth + name
	seven = name + birth
	egiht = name + number
	nine = birth + name
	ten = birth + number
	eleven = number + name
	tewelve = number + birth
	print ('\t \t ', one, '\n \t \t', tow, '\n \t \t ', three, '\n \t \t', four, '\n \t \t', five, '\n \t \t', six, '\n \t \t', seven, '\n \t \t', egiht, '\n \t \t', nine, '\n \t \t', ten, '\n \t \t', eleven, '\n \t \t', tewelve)

def  Youtube():
	link = input('\t \t Enter the link : ')
	video = YouTube(link)
	stream = video.streams.get_highest_resolution()
	stream.download()

def music():
	music = input('\t \t Enter music name with path : ')
	mixer.init(music)
	mixer.music.load(music)
	mixer.music.play(music)

def main():
	text()
	print ('\n'+'\n')
	a1 = '\t \t  1) Do you want delete some file ? '
	a2 = '\t \t  2) Do you want make littel password list ? '
	a3 = '\t \t  3) Do you want IP Adress some website ? '
	a4 = '\t \t  4) Do you want know what time is it ?'
	a5 = '\t \t  5) Do you want calculator ? '
	a6 = '\t \t  6) Do you want rename some file ?'
	a7 = '\t \t  7) Do you want read file ? '
	a8 = '\t \t  8) Do you want Youtube downloader ?'
	a9 = '\t \t  9) Do you want music palyer ?'
	a10 = '\t \t 10) Do you want Code Scripts ? '
	print(a1)
	print(a2)
	print(a3)
	print(a4)
	print(a5)
	print(a6)
	print(a7)
	print(a8)
	print(a9)
	print(a10)
	while True:
		want = input('\n \t \t  root@root# ')
		if want == '1':
			print('\t \t Just do it ')
			remove()
		elif want == '2':
			print('\t \t Just do it')
			passwordlist()
		elif want == '3':
			print('\t \t Just do it ')
			IP()
		elif want == '4':
			print('\t \t Oh sorry now i say')
			date()
		elif want == '5':
			print('\t \t Just do it ')
			calculator()
		elif want == '6':
			print('\t \t Just do it ')
			rename()
		elif want == '7':
			print('\t \t Just do it ')
			read()
		elif want == '8':
			print('\t \t Just do it')
			Youtube()
		elif want == '9':
			print('\t \t Just do it')
			music()
		elif want == '10':
			print ('\t \t Ok you should go my github page \n \t \t @Dr-parham')
		else: 
			print ('\n \t \t sorry bro we don\'t have this item')

try:
	if len(sys.argv) == 2:
		help(sys.argv[1])
	else:
		main()
except KeyboardInterrupt as e:
	print('bye')
	sys.exit()
	
