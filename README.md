# Rock-Papel-Shears
This is a simple python game that plays "rock, paper scissors" with you vs the computer!
from random import randint
#create a list of different play options
s = ['rock', 'paper', 'scissors']

#assign a random player to the computer
computer = s[randint(0, 2)]

#set the payer to false
player = False

while player == False:
    player = input(['rock', 'paper', 'scissors'])
    if player == computer:
        print('Tie!')
    elif player == 'rock':
        if computer == 'paper':
            print('You lose! ', computer, 'covers ', player)
        else:
            print("You win! ", player, "smashes ", computer)
    elif player == 'paper':
        if computer == 'scissors':
            print("You lose! ", computer, "cuts", player)
        else:
            print("You win! ", player, "covers ", computer)
    elif player == 'scissors':
        if computer == 'rock':
            print("You lose! ", computer, "smashes ", player)
        else:
            print("You win! ", player, "cuts ", computer)
    else:
        print("That's not a valid answer. Check your spelling!")

    player = False
    computer = s[randint(0, 2)]

