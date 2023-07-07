import random
import time
health = 100
choices = ["a","b","c","d"]

print("your health is", health)
boolean = True
print("YOU'VE BEEN HIT! ")
dmg = random.randint(
    40,
    40,
) + 40
health = health - dmg
print("your health is now: ", (health))
Small_Potion = 3 
Medium_Potion = 3
Big_Potion = 3
Max_Health_Potion = 3
while boolean == True:
  
    comchoice = random.choice(choices)
    print(comchoice)
    time.sleep(2)
    print(f'You have {Small_Potion} Small Potions, {Medium_Potion} Medium Potions, {Big_Potion} Big Potions, {Max_Health_Potion} Max Health Potions left')
    print("Which ones would you like to use? ")
    print(
        "a = Small Potion (20hp), b = Medium Potion(40hp), c = Big Potion(60hp), d = Max_Health_Potion(100hp)"
    )
    choice = input()
    if choice == "a":
        if Small_Potion == 0:
            print("Empty")
        else:
            health = health + 20
            if health > 100:
             health = 100
            Small_Potion = Small_Potion - 1
            print("your health is", health)
            print(f"Small Potions left: {Small_Potion}")

    elif choice == "b":
        if Medium_Potion == 0:
            print("Empty")
        else:
            health = health + 40
            if health > 100:
             health = 100
            Medium_Potion = Medium_Potion - 1
            print("your health is", health)
            print(f"Medium Potions left: {Medium_Potion}")

    elif choice == "c" or choice == "C":
        if Big_Potion == 0:
            print("Empty")
        else:
            health = health + 60
            if health > 100:
             health = 100
            Big_Potion = Big_Potion - 1
            print("your health is", health)
            print(f"Big Potions left: {Big_Potion}")

    elif choice == "d":
        if Max_Health_Potion == 0:
            print("Empty")
        else:
            health = health + 100
            if health > 100:
             health = 100
            Max_Health_Potion = Max_Health_Potion - 1
            print("your health is", health)
        print(f"Max Health Potions left: {Max_Health_Potion}")
    else:
        print("Invalid choice")
