# NEA-calculations-trajectory-air-to-ground-simulations-
# subroutine for horizonatal calculations
# Slow-printing text for effect
import math 
import time 
import os 
import sys
def delay_print(s):
    for c in s:
        sys.stdout.write(c)
        sys.stdout.flush()
        time.sleep(0.010)

    # Clear the screen
def clear_screen():
    clear = lambda: os.system('clear')
    clear()
def horizontal_targeting():
    import math 
    import time 
    import os 
    import sys
    #accelration due to gravity 
    g = 9.81 
    F = 0 

    # equation for horizontal projectiles 

    # Clear the screen
    def clear_screen():
        clear = lambda: os.system('clear')
        clear()

    # Slow-printing text for effect
    def delay_print(s):
        for c in s:
            sys.stdout.write(c)
            sys.stdout.flush()
            time.sleep(0.010)

    #subroutine section     
    # subroutine for height and intial velocity
    def sub_H_and_U():
        delay_print("please input your know information \n ")
        H = float(input(delay_print("enter height of object \n")))
        U = float(input(delay_print("enter intial velocity \n")))
        t = math.sqrt(2*H/g)
        R = U*t
        delay_print("time object spent in fall was " + str(t) +"s \n")
        delay_print("range of object is " + str(R) + "m \n ")
        delay_print("intial velocity is " + str(U) + "m/s \n")
        delay_print("height at wich object is dropped " + str(H) + "m \n")
        return(t and R)

    # subroutine for height and time 
    def sub_H_and_T():
        delay_print("please input your know information  \n ")
        U = float(input(delay_print("enter know intial speed of object \n")))
        t = float(input(delay_print("enter time spent in free fall ")))
        R = U*t
        H = math.pow(t,2)/(2*g)
        delay_print("time object spent in fall was " + str(t) +"s \n")
        delay_print("range of object is " + str(R) + "m \n ")
        delay_print("intial velocity is " + str(U) + "m/s \n")
        delay_print("height at wich object is dropped " + str(H) + "m \n")
        return(R and H)

    # subroutine for height and range 
    def sub_H_and_R():
        delay_print("please input your know information \n")
        H = float(input(delay_print("enter height of the object being dropped \n")))
        R = float(input(delay_print("enter range of the object being dropped \n")))
        t = math.sqrt(2*H/g)
        U= R/t
        delay_print("time object spent in fall was " + str(t) +"s \n")
        delay_print("range of object is " + str(R) + "m \n ")
        delay_print("intial velocity is " + str(U) + "m/s \n")
        delay_print("height at wich object is dropped " + str(H) + "m \n")
        return (U and t)

    # subroutine for range and intial velocity 
    def sub_R_and_U():
        delay_print("please input your know information \n")
        R = float(input("please input the range of the projectile in meters \n"))
        U = float(input("please input the intial speed of the projectile in m/s \n"))
        t= R/U
        H = 0.5*(g*(pow(t,2)))
        delay_print("time object spent in fall was " + str(t) + "s \n")
        delay_print("range of object is " + str(R) + "m \n ")
        delay_print("intial velocity is " + str(U) + "m/s \n")
        delay_print("height at wich object is dropped " + str(H) + "m \n")
        return(t and H)

    # subroutine for range and time 
    def sub_R_and_t():
        delay_print("please input your know information \n")
        R = float(input("please input the range of the projectile in meters \n"))
        t = float(input("enter time spent in free fall \n"))
        U= R/t
        H= 0.5*(g*(pow(t,2)))
        delay_print("time object spent in fall was " + str(t) + "s \n")
        delay_print("range of object is " + str(R) + "m \n ")
        delay_print("intial velocity is " + str(U) + "m/s \n")
        delay_print("height at wich object is dropped " + str(H) + "m \n")
        return(U and H)
    

    # subroutine for range and time 
    def sub_U_and_T():
        delay_print("please input your know information \n")
        U = float(input("please input the intial speed of the object \n"))
        t = float(input("enter time spent in freel fall \n "))
        R = U*t
        H = 0.5*(g*(pow(t,2)))
        delay_print("time object spent in fall was " + str(t) + "s \n")
        delay_print("range of object is " + str(R) + "m \n ")
        delay_print("intial velocity is " + str(U) + "m/s \n")
        delay_print("height at wich object is dropped " + str(H) + "m \n")
        return(R and H)
    #display screen one 
    delay_print("would do you know about the projectile currently you must know at least two factors \n")
    delay_print("please input either \n")
    delay_print("1 for know height \n")
    delay_print("2 for know range \n")
    delay_print("3 for know intial velocity \n")
    delay_print("4 time spent in orbit \n")
    #personal choice 1
    choice1 = input("")
    clear_screen
    #display screen two
    delay_print("what else do you know about the projectile currently\n")
    delay_print("please input either \n")
    delay_print("1 for know height \n")
    delay_print("2 for know range \n")
    delay_print("3 for know intial velocity \n")
    delay_print("4 time spent in free fall \n")
    #personal choice 1  
    choice2 = input("")
    clear_screen
    if (choice1 == "1" and choice2 == "3") or (choice1 == "3" and choice2 == "1"):
        t=0
        R=0
        sub_H_and_U()
    elif (choice1 == "1" and choice2 == "4") or (choice1 == "4" and choice2 == "1"):
        R=0
        U=0
        sub_H_and_T()
    elif (choice1 == "1" and choice2 == "2") or (choice1 == "2" and choice2 == "1"):
        t=0
        U=0
        sub_H_and_R()
    elif (choice1 == "2" and choice2 == "3") or (choice1 == "3" and choice2 == "2"):
        t=0
        H=0
        sub_R_and_U()
    elif (choice1 == "2" and choice2 == "4") or (choice1 == "4" and choice2 == "2"):
        H=0
        U=0
        sub_R_and_t()
    elif (choice1 == "3" and choice2 == "4") or (choice1 == "4" and choice2 == "3"):
        H=0
        R=0
        sub_U_and_T()
#start interface for the calculation selectiuon 
print ("practise demo for alculations please input the calculation you would like to test")
chosen = False 
while chosen == False:
    print("1. horizantal projections ")
    choice = input("type response here ")
    if choice == "1" :
        horizontal_targeting()
