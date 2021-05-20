# Rock_paper_scissors-
import random
import sys


def game(this_human):
    options = ['rock', 'paper', 'scissors']
    cranium = options[random.randint(0, 2)]
    if cranium == this_human:
        print(" i chose " + cranium + " and you chose " + this_human)
        return "\n it's a tie"

    elif cranium == "rock" and this_human == "paper":
        print(" i chose " + cranium + " and you chose " + this_human)
        return "you win"

    elif cranium == "rock" and this_human == "scissors":
        print(" i chose " + cranium + " and you chose " + this_human)
        return "you lose"

    elif cranium == "paper" and this_human == "rock":
        print(" i chose " + cranium + " and you chose " + this_human)
        return "you lose"

    elif cranium == "paper" and this_human == "scissors":
        print(" i chose " + cranium + " and you chose " + this_human)
        return "you win"

    elif cranium == "scissors" and this_human  == "rock":
        print(" i chose " + cranium + " and you chose " + this_human)
        return " you win"

    elif cranium == "scissors" and this_human == "paper":
        print("i chose " + cranium + " and you chose " + this_human)
        return "you lose"


print(" hi, i'm cranium.....let's play rock paper scissors\n follow the instructions below to continue")

print(" enter 'rock' to choose rock\n enter 'paper' to choose paper")

print(" enter 'scissors' to choose scissors\n enter 'quit' to stop program ")
loop = input(' How many times do you wanna go: ')

human_score = 0
cranium_score = 0
ref = 1


while ref <= int(loop):
    response = input(" write your choice here: ")
    if response == "quit":
        sys.exit()
    elif response == "rock":
        outcome = game("rock")
        print(outcome)
        if outcome == " you win":
        	human_score += 1
        elif outcome == 'you lose':
        	cranium_score += 1
        ref += 1
        continue
    elif response == "paper":
        outcome = game("paper")
        print(outcome)
        if outcome == 'you win':
        	human_score += 1
        elif outcome == 'you lose':
        	cranium_score += 1
        ref += 1
        continue
    elif response == "scissors":
        outcome = game("scissors")
        print(outcome)
        if outcome == 'you win':
        	human_score += 1
        elif outcome == 'you lose':
        	cranium_score += 1
        else:
        	cranium_score = cranium_score
        	human_score = human_score
        ref += 1
        continue
    else:
        print(" error!!!\n Dumb human, just type your guess.....rock, paper or scissors")
sassy_cranium = [' Puny humans', ' this is how the computers will take over the world!', ' You didn\'t stand a chance, human!! ']
cranium_beaten = ["  You haven't seen the last of me!", " Well, i'm gonna postpone taking over the world ", " You were just lucky human"]
r_num = random.randint(0, 2)
if cranium_score > human_score:
	print( ' cranium says:' + sassy_cranium[r_num])
elif cranium_score < human_score:
	print(' cranium says:' +  cranium_beaten[r_num])
elif cranium_score == human_score:
	print(' cranium says: ' +'Good game!!')
print(' human: '+str(human_score))
print(' cranium: '+str(cranium_score))
