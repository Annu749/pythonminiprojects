# pythonminiprojects
python mini projects
PYTHON MINI PROJECTS


SUBMITTED BY: ANUGRAH JADON
SECTION: BA
GROUP: 1
CLASS ROLL: 12
UNIVERSITY ROLL: 2315000362
SUBMITTED TO: Mrs. GURPREET KAUR MAM
 
1.	#numbers in forward and reverse
n = int(input("Enter the number of elements: "))
l = []
for i in range(n):
    num = int(input(f"Enter number {i+1}: "))
    l.append(num)
print("Forward order: ", l)
print("Reverse order: ", l[::-1])

OUTPUT:-

 



 
2.	# program for voting
a=str(input("enter your name"))
b=int(input("enter your age"))
if(b>=18):
    print(a,"you are eligible for vote")
    print("1-BJP")
    print("2-CON")
    print("3-AAP")
    print("4-JANTA")
    n=int(input("enter a no. for vote"))
    BJP=0
    CON=0
    AAP=0
    JANTA=0
    if(n==1):
        BJP+=1
        print("you have voted for BJP")
    elif(n==2):
        CON+=1
        print("you have voted for CON")
    elif(n==3):
        AAP+=1
        print("you have voted for AAP")
    elif(n==4):
        JANTA+=1
        print("you have voted for JANTA")
    else:
        print("you have not entered the valid no.")
    print("BJP=",BJP)
    print("CON=",CON)
    print("AAP=",AAP)
    print("JANTA=",JANTA)
else:
    print("you are not eligible") 
OUTPUT:-
 
3.	#guess the number
import random
def guess_number():
    secret_number = random.randint(1,100)
    
    attempts = 0
    while True:
        guess = int(input("Guess the number between 1 and 100 "))
        attempts += 1
        
        if guess < secret_number:
            print("Too Low! Try again😞")
        elif guess > secret_number:
            print("Too High! Try again😞")
        else:
            print(f"Congratulations!🥳🥳 You guessed the number {secret_number} correctly!")
            print(f"It took you {attempts} attempts.")
            break
guess_number()
OUTPUT:-

 
 
4.	#Rock, Paper, Scissors
import random
def get_user_choice():
    while True:
        user_choice = input("Enter your choice (rock/paper/scissors): ").lower()
        if user_choice in ['rock', 'paper', 'scissors']:
            return user_choice
        else:
            print("Invalid choice. Please enter 'rock', 'paper', or 'scissors'.")

def get_computer_choice():
    return random.choice(['rock', 'paper', 'scissors'])

def determine_winner(user_choice, computer_choice):
    if user_choice == computer_choice:
        return "It is a tie"
    elif (user_choice == 'rock' and computer_choice == 'scissors') or\
         (user_choice == 'paper' and computer_choice == 'rock') or \
         (user_choice == 'scissors' and computer_choice == 'paper'):
        return "You win!"
    else:
        return "Computer wins!"

def play_game():
    print("Welcome to Rock, Paper, Scissors")
    while True:
        user_choice = get_user_choice()
        computer_choice = get_computer_choice()

        print("You chose:", user_choice)
        print("Computer chose:", computer_choice)

        print(determine_winner(user_choice, computer_choice))

        play_again = input("Do you want to play again? (yes/no): ").lower()
        if play_again != 'yes':
            break
play_game()
OUTPUT:-

 


5.	#basic calculator
def add(x, y):
    return x + y

def subtract(x, y):
    return x - y

def multiply(x, y):
    return x * y

def divide(x, y):
    if y == 0:
        return "Cannot divide by zero"
    else:
        return x / y

print("Select operation that you want to operate:")
print("1. Add")
print("2. Subtract")
print("3. Multiply")
print("4. Divide")

while True:
    choice = input("Enter choice (1/2/3/4): ")

    if choice in ('1', '2', '3', '4'):
        num1 = float(input("Enter first number: "))
        num2 = float(input("Enter second number: "))

        if choice == '1':
            print("Result:", add(num1, num2))
        elif choice == '2':
            print("Result:", subtract(num1, num2))
        elif choice == '3':
            print("Result:", multiply(num1, num2))
        elif choice == '4':
            print("Result:", divide(num1, num2))
    else:
        print("Invalid Input")

    again = input("Do you want to perform another calculation? (yes/no): ")
    if again.lower() != 'yes':
        break
OUTPUT:-


 


6.	#grading system
def grade_calculating(score):
    if score >= 90:
        return 'A'
    elif score >= 80:
        return 'B'
    elif score >= 70:
        return 'C'
    elif score >= 60:
        return 'D'
    else:
        return 'F'

def main():
    try:
        score = float(input("Enter the percentage score: "))
        if score < 0 or score > 100:
            print("Invalid, Please enter a percentage between 0 and 100.")
        else:
            grade = grade_calculating(score)
            print("The grade for the score {:.2f}% is: {}".format(score, grade))
    except ValueError:
        print("Invalid input. Please enter a valid number.")
main()
OUTPUT:-

 

7.	# roll a dice game
import random
def roll_a_dice():
    return random.randint(1, 6)

def roll_dice(num_rolls):
    results = []
    for i in range(num_rolls):
        result = roll_a_dice()
        results.append(result)
    return results
num_rolls = int(input("Enter the number of times you want to roll the dice: "))
results = roll_dice(num_rolls)
print("Results:", results)
OUTPUT:-

 

8.	#inventory system
inventory = {}

def addproduct(item, quanty):
    if item in inventory:
        inventory[item] += quanty
    else:
        inventory[item] = quanty

def removeproduct(item, quanty):
    if item in inventory:
        if inventory[item] >= quanty:
            inventory[item] -= quanty
        elif inventory[item] == 0:
            del inventory[item]
        else:
            print(f"Not enough {item} in stock.")
    else:
        print(f"{item} not found in inventory.")

def totalitems():
    print("Items in Inventory:")
    for item, quanty in inventory.items():
        print(f"{item}: {quanty}")

addproduct("Apples", 10)
addproduct("Bananas", 15)
addproduct("Oranges", 20)

removeproduct("Bananas", 5)
totalitems()
OUTPUT:-
 
9.	#report card
name=str(input("enter name of student:"))
roll_no=int(input("enter roll no. of student"))
clas=(input("enter class of student"))
print("Name:",name)
print("Roll:",roll_no)
print("Class:",clas)
if(name!=str and roll_no!=int(2)):
    print("please enter valid details")

else:
    maths=int(input("enter no. of maths between 0 to 100 "))
    physics=int(input("enter no. of physics between 0 to 100 "))
    biology=int(input("enter no. of biology between 0 to 100 "))
    chemistry=int(input("enter no. of chemistry between 0 to 100 "))
    if(maths<0 or maths>100 or physics<0 or physics>100 or biology<0 or biology>100 or chemistry<0 or chemistry>100):
        print("please enter valid marks")
    else:
        total=maths+physics+biology+chemistry
        print("total marks:",total)
        percentage=total/4
        print("percentage:",percentage)
        if(percentage>=90):
            print("Grade: A")
        elif(percentage>=80):
            print("Grade: B")
        elif(percentage>=70):
            print("Grade: C")
        elif(percentage>=35):
            print("Grade: D")
        else:
            print("Grade: F")
OUTPUT:-
 



