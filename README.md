import random

# Choices for the game
choices = ["stn", "pap", "scs"]
full_names = {
    "stn": "stone",
    "pap": "paper",
    "scs": "scissors"
}

# Function to get and validate player choice
def get_player_choice():
    player_choice = input("Enter your choice (stn, pap, scs) or 'quit' to exit: ").strip()
    return player_choice

# Game loop
while True:
    random_choice = random.choice(choices)  # Randomly selects an element from the list

    # Printing the options for the player
    print("stn = stone, pap = paper, scs = scissors")

    player_choice = get_player_choice()

    if player_choice == 'quit':
        print("Thanks for playing!")
        break

    if player_choice not in choices:
        print("Invalid choice! Please choose stn, pap, or scs.")
        continue

    if player_choice == random_choice:
        print("It's a tie!")
    elif player_choice == "stn" and random_choice == "pap":
        print(f"You chose {full_names[player_choice]} and the computer chose {full_names[random_choice]}. You lose!")
    elif player_choice == "pap" and random_choice == "scs":
        print(f"You chose {full_names[player_choice]} and the computer chose {full_names[random_choice]}. You lose!")
    elif player_choice == "scs" and random_choice == "stn":
        print(f"You chose {full_names[player_choice]} and the computer chose {full_names[random_choice]}. You lose!")
    else:
        print(f"You chose {full_names[player_choice]} and the computer chose {full_names[random_choice]}. You win!")



_ = input("Press Enter to continue or type 'exit' to quit: ")
if _ == 'exit':
    exit()
