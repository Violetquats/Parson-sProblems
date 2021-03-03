# Parson-sProblems
import random
dieRolls = []
cardPicked = []
cardNumbers = ["A",
            "2",
            "3",
            "4",
            "5",
            "6",
            "7",
            "8",
            "9",
            "10",
            "J",
            "Q",
            "K",]
cardSuits = ["of spades",
             "of hearts",
             "of diamonds",
             "of clubs"]
            
while True:
    dieOrCards = input('Halla, friend! Would you like to roll a die (1) or pick a card (2)?')
    if dieOrCards == '1':
        dieSides = input('How many sides would you like your die to have?')
        dieTimes = input('How many time would you like to roll this {} sided die?'.format(dieSides))

        for x in range(0,int(dieTimes)):
            dieRolls.append(random.randint(1,int(dieSides)))
        
        print("You rolled {}".format(dieRolls))
        
        dieRolls.clear()
        terminate = input("Would you like to roll more dice?")
        if terminate == ("no"):
            cards = input("Would you like to pick a card then?")
        if cards == ("no"):
            break
        elif terminate == ("yes"):
            dieOrCards == "1"
