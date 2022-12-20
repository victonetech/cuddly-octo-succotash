print("*******Rock Paper Scissors***********"'\n')
print("Rock=1, Scissors=2, Paper=3")
#("Rock beats scissors,Scissors beats paper,Paper beats rock"'\n')

#Enter names.
name_1 = input("Enter Player 1 name : "'\n')
name_2 = input("Enter Player 2 name:"'\n')

# function to compare values. 
def compare(name_1,name_2):

# users pick a  option
    user_1 = int(input(f"Hi!! {name_1} , Please choose an option 'Rock'= 1,'Scissors' = 2,'Paper'= 3 :"'\n'))
    user_2 = int(input(f" Hi!! {name_2} , Please choose an option  'Rock' = 1, 'Scissors' = 2, 'Paper' = 3:"'\n'))

# user_1 is the  winner.
    if user_1 == 1  and user_2 ==2 or user_1 == 2  and user_2 == 3 or user_1 == 3 and user_2 == 1:
        print(f"The winner is {name_1}. "'\n')

#  user_2 is the winner.
    elif  user_1 == 2  and user_2 == 1 or user_1 ==3   and user_2 == 2 or user_1 == 1 and user_2 ==3:
        print(f" The winner is {name_2}."'\n')
        
    # In case both pick the same option.
    elif user_1 == user_2:
        print("****** NO WINNER *******"'\n')
  
        compare(name_1,name_2)

keep_playing ="-"

# function to finish the game or keep playing.
def play_again(keep_playing):

    while keep_playing != 'n':
        keep_playing = input(" Do you want to try again?   Yes = Y , No = N "'\n')
        if keep_playing == 'y' or keep_playing =='Y':
# applying the first function in order to repeat the process.
           compare(name_1,name_2)
# game is over
        elif keep_playing == 'n' or keep_playing =='N':
               print(f"thanks for your time {name_1} and {name_2}.")
               break

play_again(keep_playing)
