# Number-Guessing-Game



import random
import math

LB=int(input("Enter Lower bond: "))    #Lower Bound/range
UB=int(input("Enter Upper bond: "))    #Upper bound/range

x=random.randint(LB,UB)
print("\n\t YOU HAVE ONLY ",round(math.log(UB-LB + 1,2)), " CHANCES TO GUESS THE INTEGER!\n")

Count=0
while Count<math.log(UB-LB+1,2):
    Count += 1
    guess=int(input("Guess a number: "))
    if x==guess:
        print("Congratulations you did it in ",Count, "try")
        break
    elif x>guess:
        print("You guessed too small!")
    elif x<guess:
        print("You guessed too high!")


if Count >= math.log(UB-LB+1,2):
    print("\nThe number is %d"%x)
    print("\tBetter Luck Next Time!")
