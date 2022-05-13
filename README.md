# social-media-clone
#email_verification phase 1

def account_verification():
    while True:
        try:
            email_account = input("Enter your email here: {ex. add(@gmail.com): makui@gmail.com}: ").lower()
            password_verify = int(input("Enter your password here: exclude(value : 0)/ (int: 1,2,3...) : "))

            if email_account == "shikisenri@gmail.com":
                if password_verify == 9329424670:
                    print('the input credential is correct! , moving through the main page...')
                    welcome_page()
                    break
                else:
                    print("==================== error ==================================")
                    print("you input a wrong password, please try again... ")
                    print("=============================================================")

            else:
                print("==================== error ==================================")
                print("you input a wrong email, please try again... ")
                print("=============================================================")

        except ValueError as e:
            print("==================== error ==================================")
            print(f"the input is should be an integer (not include: letter,float or zero as value) : {e}")


#profile set_up_functions
def nickname():
    pass
def email():
    pass
def log_out():
    pass

#profile setup
def set_up_profile():
    print("====================== < set-up profile > ============================")
    print("choose facemash set up available below: ")
    print('1.) nickname')
    print('2.) email')
    print('3.) log out')

    input_set_up_profile = int(input("Enter the set up function: (integers only(1,2,3 and 4):  "))
    while True:
        try:

            if input_set_up_profile == 1:
                nickname()

            elif input_set_up_profile == 2:
                email()

            elif input_set_up_profile == 3:
                log_out()
            else:
                print("input a wrong credentials or not included function, please try again")
        except ValueError:
            print("don't use letter, use numerical values or integers only (ex.1,2,3 or 4...): ")

#profile
def profile():
    print("========================== < profile > ================================")
    print("hello, welcome to profile!")
    print("profile show commands (/prof) ")
    while True:
        try:
            input_profile = input(" Enter the command here: ").lower()

            if input_profile != "/prof":
                print("the command is incorrect, please try again...")
            else:
                print("entering the profile set-up...")
        except ValueError:
            print("don't use number(int,float,etc.) use = '/prof' instead")



#bio
def bio():
    print("========================== < bio > ==================================")
    print("hello, welcome to bio!")

#info
def info():
    print("========================== < info > =================================")
    print("hello, welcome to info!")

#settings
def settings():
    print("=======================================================================")
    print("hello, welcome to settings!")


#welcome page
def welcome_page():
    print("========================== < WELCOME > ================================")
    print('                      welcome to facemash!                             ')
    print("A.)Profile")
    print("B.)Bio")
    print("C.)Info")
    print("D.)Settings")
    print("=======================================================================")

    while True:
        try:
            input_facemash = input("Enter the page you want to enter in: (A,B,C or D) : ").upper()

            if input_facemash == "A":
                print("=======================================================================")
                print("Entering profile...")
                print("=======================================================================")
                profile()
                break
            elif input_facemash == "B":
                print("=======================================================================")
                print("Entering the bio...")
                print("=======================================================================")
                bio()
                break
            elif input_facemash == "C":
                print("=======================================================================")
                print("Entering the info...")
                print("=======================================================================")
                info()
                break
            elif input_facemash == "D":
                print("=======================================================================")
                print("Entering the settings...")
                print("=======================================================================")
                settings()
                break
            else:
                print("input a wrong credentials or not included function, please try again")
        except ValueError as e:
            print(f"The error is: {e} ")


account_verification()
