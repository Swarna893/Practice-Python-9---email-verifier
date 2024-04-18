# Practice-Python-7---email-verifier

email = input("Enter your Email id: ")
k = 0
j = 0
d = 0
if len(email) >= 6:
    if email[0].isalpha():
        if ('@' in email) and (email.count("@") == 1):
            if (email[-4] == ".") ^ (email[-3] == "."):
                for i in email:
                    if i == i.isspace():
                        k = 1
                    elif i.isalpha():
                        if i == i.upper():
                            j = 1
                    elif i.isdigit():
                        continue
                    elif i == "_" or i == "." or i == "@":
                        continue
                    else:
                        d = 1
                if k == 1 or j == 1 or d == 1:
                    print("Wrong email 5: due to space or uppercase")
            else:
                print("Wrong email 4: due to '.' distortion!")
        else:
            print("Wrong email 3: due to '@' distortion!")
    else:
        print("Wrong email 2: due to first charater is not alphabet!")
else:
    print("Wrong email 1: due to too short id!")
