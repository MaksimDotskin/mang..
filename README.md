import random

while True:
    user_action= input("Tee oma valik – kivi, käärid või paber: ")
    possible_actions = ["kivi", "käärid", "paber"]
    computer_action = random.choice(possible_actions)
    print(f"\nSa tegid oma valiku {user_action}, teine mängija on oma valiku teinud {computer_action}.\n")
    if user_action == computer_action:
        print(f"Mõlemad mängijad valisid {user_action}. viik!")
    elif user_action == "kivi":
        if computer_action == "käärid":
            print("Kivi lööb käärid. Sa võitsid")
        else:
            print("Paber mähib kivi. Sa kaotasid")
    elif user_action == "Paber":
        if computer_action == "Kivi":
            print("Paber mähib kivi. Sa võitsid")
        else:
            print("Käärid lõigatud paber. Sa kaotasid")
    elif user_action == "Käärid":
        if computer_action == "Paber":
            print("Käärid lõigatud paber. Sa võitsid")
        else:
            print("Kivi lööb käärid. Sa kaotasid")
    play_again = ""
    play_again = input("Kas soovite rohkem mängida? (j/e): ")
    if play_again.lower() != "j":
        break
