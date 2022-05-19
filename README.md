# game
import random
print("you will get only two chance to play this game")
options=("Stone","paper","Scissors")
humanpoint=0
computerpoint=0
chance=2
noofchance=0
while noofchance<10:
    userinput=input("\t\nstone,paper,Scisssors:")
    computerinput=random.choice(options)

    if userinput=="stone" and computerinput=="paper":
        print("Computer input is",computerinput)
        print("computer win the game")
        computerpoints = computerpoints + 1
        print("#Your point is", humanpoints)
        print("#Computer point is", computerpoints)
        noofchance = noofchance + 1
    elif userinput=="stone" and computerinput=="Stone":
        print("Computer input is", computerinput)
        print("tie! you both Choose the same")
        computerpoints = computerpoints + 1
        print("#Your point is", humanpoints)
        print("#Computer point is", computerpoints)
        noofchance = noofchance + 1
    elif userinput=="stone" and computerinput=="Scissors":
        print("Computer input is", computerinput)
        print("you win the game")
        computerpoint = 0
        humanpoint = 1

    elif userinput == "paper" and computerinput == "Scissors":
        print("Computer input is", computerinput)
        print("computer win the game")
        computerpoint = 1
        humanpoint = 0
    elif userinput == "paper" and computerinput == "paper":
        print("Computer input is", computerinput)
        print("tie! you both Choose the same")
        computerpoint = 0
        humanpoint = 0
    elif userinput == "paper" and computerinput == "stone":
        print("Computer input is", computerinput)
        print("you win the game")
        computerpoint = 0
        humanpoint = 1

    elif userinput == "Scissors" and computerinput == "stone":
        print("Computer input is", computerinput)
        print("computer win the game")
        computerpoint = 1
        humanpoint = 0
    elif userinput == "Scissors" and computerinput == "Scissors":
        print("Computer input is", computerinput)
        print("tie! you both Choose the same")
        computerpoint = 0
        humanpoint = 0
    elif userinput == "Sciossors" and computerinput == "paper":
        print("Computer input is", computerinput)
        print("you win the game")
        computerpoint = 0
        humanpoint = 1
    else:
        print("you enter invalid choice")

print(humanpoints)
print(computerpoints)
if humanpoints>computerpoints:
    print("Human points are more than Computer .So Human wins")
if humanpoints<computerpoints:
    print("Computer points is more than Human points .So Computer wins")
print("Your point is",humanpoints,"And computer points is",computerpoints)
if noofchance==chance:
    print("GAME OVER ^_~")
    if noofchance==10:
        quit()
