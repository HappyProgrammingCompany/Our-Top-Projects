# Our-Top-Projects
Only the best of the best, Norwegian Moose-Approved, projects.
# Import modules
import os


# Initialize all variables
eachTime = 0
countTime = 0

o = ""
g = ""
gAll = ""
k = ""
f = ""
fAll = ""
r = ""
rAll = ""

allowed = 0
loginsignup = ""
username = ""
password = ""
both = ""
ch = ""
ordValue = 0
DISTANCE = -21
cipherValue = 0
bothEncrypt = ""

options = ""

fileName = ""
content = ""

removeCheck = 0
remove = ""

topOrBottom = ""
tbCheck = 0

newName = ""

listFile = []
file = ""

fileSize = 0

sum = 0

again = ""
againCheck = 0


# Begin program


print("Welcome to TextFileEditor V 2.0")
print()
print()

for eachTime in range(12500000):
  countTime += 1
    
print("Designed by Happy Programming Company")
print()

for eachTime in range(12500000):
  countTime += 1

print("Distrubuted by Happy Programming Company")
print()

for eachTime in range(12500000):
  countTime += 1

print("And special thanks to Happy Programming Company")
print()

for eachTime in range(12500000):
  countTime += 1

print("And special special thanks to the Society for the Wellness of Ecuadorian Alpacas")
print()

for eachTime in range(12500000):
  countTime += 1

print()
print()


# Ask for username/password


if os.path.isdir("Text File Editor") == False:
  os.mkdir("Text File Editor")
  os.chdir("Text File Editor")

else:
  os.chdir("Text File Editor")

if os.path.isfile("usernames_and_passwords.txt") == False:
  o = open("usernames_and_passwords.txt", 'w')
  o.close()


while allowed == 0:
  loginsignup = input("Would you like to log in or sign up? ")
  loginsignup = loginsignup.lower()
  print()
  
  if "sign up" in loginsignup:
    username = input("Enter username: ")
    password = input("Enter password: ")
    print()

    both = username + password
    bothEncrypt = ""
    
    for ch in both:
      ordValue = ord(ch)
      cipherValue = ordValue + DISTANCE
      bothEncrypt += chr(cipherValue)
    
    g = open("usernames_and_passwords.txt", 'r')
    gAll = g.read()
    g.close()

    if bothEncrypt in gAll:
      print("Error. Username and Password combination taken.")
      print()

    else:
      k = open("usernames_and_passwords.txt", 'w')
      k.write(gAll)
      k.write(bothEncrypt)
      k.write("\n")
      k.close()

      os.mkdir(username)

      print()    
      print("Account Created")
      print("All of your work saved in this account will be saved in the directory called: " + username)
    
      allowed = 1
    
  elif "log in" in loginsignup:
    username = input("Enter username: ")
    password = input("Enter password: ")
    print()
    
    g = open("usernames_and_passwords.txt", 'r')
    gAll = g.read()

    both = username + password
    bothEncrypt = ""

    for ch in both:
      ordValue = ord(ch)
      cipherValue = ordValue + DISTANCE
      bothEncrypt += chr(cipherValue)
    
    if bothEncrypt in gAll and os.path.isdir(username):
      allowed = 1
      g.close()

    else:
      print("Incorrect username or password")
      print()
      
  else:
    print("Enter a valid answer")
    print()


# Begin editing text files


os.chdir(username)


while allowed == 1:

  print()
  print()
  print("Do you want to:")
  print("Create a file")
  print("Remove a file")
  print("Add on to a file")
  print("Rename a file")
  print("View a list of your files")
  print("Open a file")
  print("Get the size (in bytes) of a file")
  print()
  print("Exit")
  print()
  options = input()
  options = options.lower() 


  if options.count("create") > 0:

    while fileName.endswith(".txt") == False:
      print()
      print()
      print("Enter file name. End the name with '.txt'.")
      print("Be sure to use an unused name.")
      fileName = input()
      print()

    while os.path.isfile(fileName) == True:
      print()
      print()
      print("Enter file name. End the name with '.txt'.")
      print("Be sure to use an unused name.")
      fileName = input()
      print()

    f = open(fileName, 'w')
    print()
    print("Your file has been created.")

    print()
    print()
    print("Enter the text. Press Enter when finished.")
    content = input()
  
    f.write(content)

    f.close()

    print()
    print()
    print("Your text has been saved in " + fileName + ". You may edit the file name and content.")
    print()
      
    fileName = ""
    againCheck = 0


  elif options.count("remove") > 0:

    while fileName.endswith(".txt") == False:
      print()
      print()
      print("Enter file name. End the name with '.txt'.")
      print("Be sure to use a used name.")
      fileName = input()
      print()
      
    while os.path.isfile(fileName) == False:
      print()
      print()
      print("Enter file name. End the name with '.txt'.")
      print("Be sure to use a used name.")
      fileName = input()
      print()

    removeCheck = 0
    while removeCheck == 0:
      print("Are you sure you want to remove " + fileName + "?")
      remove = input("This action can not be undone. ")
      print()
      remove = remove.lower()
      
      if "yes" in remove:
        os.remove(fileName)
        
        print()
        print()
        print("You have removed " + fileName + ".")
        print()
        
        fileName = ""
        removeCheck = 1
        againCheck = 0

      elif "no" in remove:
        print("This action has been cancelled.")
        print()
        fileName = ""
        removeCheck = 1
        againCheck = 0

      else:
        print("Enter a valid answer")
        print()
        removeCheck = 0
     
      
  elif options.count("add") > 0:
      
    while fileName.endswith(".txt") == False:
      print()
      print()
      print("Enter file name. End the name with '.txt'.")
      print("Be sure to use a used name.")
      fileName = input()
      print()
      
    while os.path.isfile(fileName) == False:
      print()
      print()
      print("Enter file name. End the name with '.txt'.")
      print("Be sure to use a used name.")
      fileName = input()
      print()

    f = open(fileName, 'r')
    fAll = f.read()

    f.close
    
    f = open(fileName, 'w')
    print()
    print("Your file has been opened.")

    tbCheck = 0
    while tbCheck == 0:
      print()
      topOrBottom = input("Would you like to add the text to the top or bottom of the text file? ")
      topOrBottom = topOrBottom.lower()
      print()
      
      if topOrBottom.count("bottom") > 0:
        tbCheck = 1
      elif topOrBottom.count("top") > 0:
        tbCheck = 1
      else:
        print("Enter a valid answer")
        print()
        tbCheck = 0

    print()
    print()
    print("Enter the text. Press Enter when finished.")
    content = input()

    if topOrBottom.count("bottom") > 0:
      f.write(fAll)
      f.write(content)

    else:
      f.write(content)
      f.write(fAll)

    f.close()

    print()
    print()
    print("Your additions have been saved in " + fileName + ". You may edit the file name and content.")
    print()
        
    fileName = ""
    againCheck = 0


  elif options.count("rename") > 0:
      
    while fileName.endswith(".txt") == False:
      print()
      print()
      print("Enter file name. End the name with '.txt'.")
      print("Be sure to use a used name.")
      fileName = input()
      print()
      
    while os.path.isfile(fileName) == False:
      print()
      print()
      print("Enter file name. End the name with '.txt'.")
      print("Be sure to use a used name.")
      fileName = input()
      print()
      
    while newName.endswith(".txt") == False:
      print()
      print()
      print("Enter the new file name. End the name with '.txt'.")
      print("Be sure to use an unused name.")
      newName = input()
      print()

    while os.path.isfile(newName) == True:
      print()
      print()
      print("Enter the new file name. End the name with '.txt'.")
      print("Be sure to use a unused name.")
      newName = input()
      print()

    os.rename(fileName, newName)

    print()
    print()
    print("You have renamed " + fileName + " as " + newName + ". You may edit the file name and content.")
    print()

    fileName = ""
    newName = ""
    againCheck = 0


  elif options.count("list") > 0:

    print()
    print()
    print("Files in directory: " + username)
    print()
    listFile = os.listdir()

    if listFile == []:
      print("No files found")
      print()
      
    else:
      for file in listFile:
        print(file)
      print()

    againCheck = 0

  
  elif options.count("open") > 0:
    while fileName.endswith(".txt") == False:
      print()
      print()
      print("Enter file name. End the name with '.txt'.")
      print("Be sure to use a used name.")
      fileName = input()
      print()
      
    while os.path.isfile(fileName) == False:
      print()
      print()
      print("Enter file name. End the name with '.txt'.")
      print("Be sure to use a used name.")
      fileName = input()
      print()

    r = open(fileName, 'r')
    rAll = r.read()
    r.close()

    print("File: " + fileName)
    print()
    print(rAll)
    print()
    
    fileName = ""
    againCheck = 0

  
  elif options.count("size") > 0:
      
    while fileName.endswith(".txt") == False:
      print()
      print()
      print("Enter file name. End the name with '.txt'.")
      print("Be sure to use a used name.")
      fileName = input()
      print()
      
    while os.path.isfile(fileName) == False:
      print()
      print()
      print("Enter file name. End the name with '.txt'.")
      print("Be sure to use a used name.")
      fileName = input()
      print()

    fileSize = os.path.getsize(fileName)
    
    print()
    print()
    print("The size of " + fileName + " is " + str(fileSize) + " bytes.")
    print()
        
    fileName = ""
    againCheck = 0

  elif options.count("hate") > 0:
    sum = 2
    while True:
      print(str(sum))
      sum **= 2
    
  elif options.count("exit") > 0:
    allowed = 2
    againCheck = 1

    
  else:
    print("Enter a valid answer")
    againCheck = 1

        
  while againCheck == 0:
    again = input("Press ENTER to start again or press 'x' to exit ")
    print()

    if again == "":
      againCheck = 1
      allowed = 1
    elif again == "x":
      againCheck = 1
      allowed = 2
    else:
      print("Enter a valid answer")
      print()
      againCheck = 0


# End
