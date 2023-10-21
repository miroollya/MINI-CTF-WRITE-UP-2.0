UITM CYBERHEROES CLUB

Holllaaaa..

hello im back ./hackboredzz!!! can you help me find the anonymous that steal my private key :) help me to find it by using all the techniques that you learn today. The bounty is waiting for the winners so reach meeeee :)

hint:31 35 37 2e 32 34 35 2e 31 35 34 2e 35 37

sooo this clook soo intresting lets explore how to exploit this hehehe...

from the hint we given so number but its look like hex right? lets try cook with my favourite decode tools https://gchq.github.io/CyberChef/ sooo..

![image](https://github.com/miroollya/MINI-CTF-WRITE-UP-2.0/assets/129681351/5563bd58-02f6-4101-ac84-51dbe7e3a047)

soo from here i figure out this is ip address intresting why not we google it?

soo i google it and appear login page :(

![image](https://github.com/miroollya/MINI-CTF-WRITE-UP-2.0/assets/129681351/9294caf9-0177-4d39-8f2a-d6880037efea)

soo lets try fuzzing by using robots.txt hehehe...

![image](https://github.com/miroollya/MINI-CTF-WRITE-UP-2.0/assets/129681351/308c5f38-6945-4fc9-9ad2-9051aa1901ac)

from here we got something lets try decode its look like base 64?

![image](https://github.com/miroollya/MINI-CTF-WRITE-UP-2.0/assets/129681351/04a5eca9-7d56-470d-a5bb-e01eaee69d4a)

ohhh i think we got it the flag lets see..
NAHHHHH

![image](https://github.com/miroollya/MINI-CTF-WRITE-UP-2.0/assets/129681351/5ee962bc-72c8-4bae-8900-be0321a0903e)

my bad hmmmm lets try some auth bypass maybe the author name? from description given its look like hackboredzz lets try

wow we got so qr code lets try scan

![image](https://github.com/miroollya/MINI-CTF-WRITE-UP-2.0/assets/129681351/64b36fdc-ca13-4ac9-a047-1f7942c87740)

noooo we got rick rollll!!!

![image](https://github.com/miroollya/MINI-CTF-WRITE-UP-2.0/assets/129681351/7cbac8bd-3490-4bad-bddb-0b1cfdbb19fa)

soo annoying soo after thinking lets try sql injection auth bypass with this help of https://github.com/payloadbox/sql-injection-payload-list soo lets tryy

![image](https://github.com/miroollya/MINI-CTF-WRITE-UP-2.0/assets/129681351/b7e46631-2f72-4957-8899-1be1f66d696b)

try by using the list and this payload i manage to bypass the login page :)
you guys also can bruteforce :)

sooo after we manage to bypass the login page its look like there are some pic intresting lets download the picture and find something maybe hidden message?
i try to use https://stylesuxx.github.io/steganography/

![image](https://github.com/miroollya/MINI-CTF-WRITE-UP-2.0/assets/129681351/0cafa4ed-7d38-4731-ae3d-c970808c99a1)

soo from here i got the hidden message and its look like hidden directoryyyy

![image](https://github.com/miroollya/MINI-CTF-WRITE-UP-2.0/assets/129681351/f12a38ea-b912-430a-bd77-64b66abda900)

NOHHH ROKIAHHH 
weird textttt noooo

![image](https://github.com/miroollya/MINI-CTF-WRITE-UP-2.0/assets/129681351/268801ff-6a08-432d-966c-0019b39a26c5)

i saw something == soo i remember the speaker told me that its must be base64 or base 32 soo i try both...first i try base64 and its not soo i try base 32 and i see the decode message is decreasing soo i try many time and finalllyyyy i got something

![image](https://github.com/miroollya/MINI-CTF-WRITE-UP-2.0/assets/129681351/b23dd753-158b-4571-aa71-e31d322b0c3d)

BOOM we got the link after decode it like 18 times i guess?

soo we got the the instagram and discover it OSINT TIMEEEE!!!

soo first i see that the owner ig upload some story that contains weird sound soo maybe its a clue? 

![image](https://github.com/miroollya/MINI-CTF-WRITE-UP-2.0/assets/129681351/646c8f99-6094-4342-8277-8bb3c7461635)

soo I ANALYZEE every post and find out some fishy gdrive link :)

![image](https://github.com/miroollya/MINI-CTF-WRITE-UP-2.0/assets/129681351/c3801d16-5e64-4399-b0a1-1101c7b9dbbb)

soo we got to the link and we retrieved .wav and the first time i hear it i know THIS IS MORSE CODEE TIMEE!!!
soo i download the file and use this tool https://morsecode.world/international/decoder/audio-decoder-adaptive.html

![image](https://github.com/miroollya/MINI-CTF-WRITE-UP-2.0/assets/129681351/780cca95-fb8f-48dc-a392-c60ae5dc2137)

we got the hidden keyy but remember the author said that o=0 sooo the final flag is UCC{R04DT0WH1T3H4T2.0}

enjoy playing? dont forget to follow and share with your friends -boredzz-











