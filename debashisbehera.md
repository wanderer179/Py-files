
import random

print("   Lets\'s start the game \"Stone,Paper,Scissors")
round=0
win=0
draw=0
list=["Stone","Paper","Scissors"]
print("0-Stone","1-Paper","2-Scissor","Number of turns is equal to 15")
while round<15:
  cpu=random.randint(0,2)
  print("         TURN-",str(round+1),"       ")
  you=int(input("Please enter your choice: "))
  while you>2 or you<0:
    print("Your input is not valid")
    you=int(input("Please insert again: "))
  print("Your choice: ",list[you])
  print("Computer's choice: ",list[cpu])
  if you==cpu:
    print("DRAW.  sab barabar. koi nahi jita/hara..khusi manao...")
    draw+=1
  else:
    if you==0:
      if cpu==1:
        print(" Ooo Noo...Paper,Stone ki face pakda..Stone ko sas laynay may aai dikat...  YOU LOOSE.")
      if cpu==2:
        print(" Badhai hoo...Stone Scissor pay bola hamla and Scissor buritaraha say ghayal..YOU WIN.")
        win+=1

    elif you==1:
      if cpu==0:
        print("Badhai hoo...Paper,Stone ki face pakda..Stone ko sa laynay may aai dikat...  YOU WIN")
        win+=1
      if cpu==2:
        print("Ooo Noo...Scissor Paper ko kata and Paper ka kisha  khatam....YOU LOOSE")

    elif you==2:
      if cpu==0:
        print("Ooo Noo...Stone Scissor pay bola hamla and Scissor buritaraha say ghayal..YOU LOOSE")
      if cpu==1:
        print("Badhai hoo...Scissor Paper ko kata and Paper ka kisha khatam..YOU WIN")
        win+=1

  round+=1

print("       RESULTS       ")
print("You win: ",str(win))
print("Computer win: ",str(15-win-draw))
print("Number of Drawn: ",str(draw))
