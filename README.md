# assignment-2

import random
import time
from sys import exit

def start():
    print("Are you ready to play the lottery? \'yes\' or \'no\'")
    print("Today the pot is at", {lottery_pot})

    reply = input("~ ")

    while reply != 'yes' and reply != 'no':
        print("I'm sorry what was that?")
        reply = input("~ ")

    if reply == 'yes':
        print("Alright!")
        time.sleep(1)
        your_numbers()

    if reply == 'no':
        print("goodbye")
        exit()


def lottery_pot():
    lottery_pot = {65000000}


def winning_numbers():
    winning_numbers = [random.randint(1, 20), random.randint(1, 20), random.randint(1, 20), random.randint(1, 20), random.randint(1, 20)]
    print(winning_numbers)

def your_numbers():
    print("""Please type in 5 numbers, that are between 1 and 20, for your
lottery numbers.""")

    num1 = input()
    num2 = input()
    num3 = input()
    num4 = input()
    num5 = input()
    time.sleep(1)
    print("And the winning numbers are...")
    time.sleep(2)
    winning_numbers()

    while winning_numbers != your_numbers:
        print("I'm sorry, but you didn't win.")
        print("$10,000,000 is being added to the pot.")
        lottery_pot += 10000000
        print("Better luck next time!")
        time.sleep(1)
        start()

    if winning_numbers == your_numbers:
        print("Congradulations! You've just won", {lottery_pot})
        print("Thanks for playing!")
        time.sleep(1)
        exit()


start()
