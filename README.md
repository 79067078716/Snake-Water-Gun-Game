# Snake-Water-Gun-Game

import random
lst = ['s', 'w', 'g']

chance = 10
no_of_chance = 0
computer_points = 0
human_points = 0
print("\t\t\t Snake Water Game\n\n")
print("s for snake\nw for water\ng for gun\n")

#While loop entering
while no_of_chance<chance:
    _input = input("snake,water,Gun")
    _random = random.choice(lst)

    if _input == random:
        print("Tie Both of you got 0 ponts")
# if user enter S
    elif _input == "s" and _random == "g":
        computer_points = computer_points + 1
        print(f"your guess {_input} and computer guess {_random} \n")
        print("computer get 1 point \n")
        print(f"computer points is {computer_points} and your point is {human_points} \n")

    elif _input == "s" and _random == "w":
        human_points = human_points + 1
        print(f"your guess {_input} and computer guess {_random} \n")
        print("you got 1 point \n")
        print(f"human points is {human_points} and computer points is {computer_points} \n")
#if uses enter "g"
    elif _input == "g" and _random == "s":
        human_points = human_points + 1
        print(f"your guess {_input} and computer guess {_random} \n")
        print("you got 1 point \n")
        print(f"human points is {human_points} and computer points is {computer_points} \n")

    elif _input == "g" and _random == "w":
        computer_points = computer_points + 1
        print(f"computer guess {_random} and you guess {_input} \n")
        print("Computer got 1 point \n")
        print(f"computer points is {computer_points} and human points is {human_points} \n")
#if user enters "w"
    elif _input == "w" and _random == "s":
        computer_points = computer_points + 1
        print(f"computer guess {_random} and you guess {_input} \n")
        print("Computer got 1 point \n")
        print(f"computer points is {computer_points} and human points is {human_points} \n")

    elif _input == "w" and _random == "g":
        human_points = human_points + 1
        print(f"your guess {_input} and computer guess {_random} \n")
        print("you got 1 point \n")
        print(f"human points is {human_points} and computer points is {computer_points} \n")

    else:
        print("You Entered wrong input")

    no_of_chance = no_of_chance + 1
    print(f"{chance - no_of_chance} is left out of {chance} \n")

print("game over")

if human_points == computer_points:
    print("The game is Tie")
elif human_points > computer_points:
    print("You win and computer loose")
elif human_points < computer_points:
    print("You loose computer won")

print(f"your point is {human_points} and computer point is {computer_points} \n")
