#Book : Violent python
# Ported to Python 3 
# Dictionary attack on Zip Files
# How to zip on terminal :: $ zip --password [password] [file.zip] [file to be zipped]
# Threading : absent

import zipfile
import time

def FindPassword():
    i = 0 

    zfile = zipfile.ZipFile("/root/Zip Cracker/file1.zip",'r')
    password_file = open("/root/Zip Cracker/Dictionary.txt",'r')
    
    for line in password_file.readlines()  :
        potential_password= line.strip('\n')
        print(potential_password)
        try:
            
            zfile.extractall(path='/root/Zip Cracker', pwd=potential_password.encode())
            #zfile.extractall(pwd=potential_password.encode('cp850','replace'))
            print('[+] Password = ' + potential_password)
            break
    
        except Exception  :
            i = i+1
            print('Attack attempt' + str(i) + '\n' )
            

if __name__ == "__main__":
    start = time.time()
    FindPassword()
    end=time.time()
    print('run time is ' + str(end-start))
    
    
            
            
