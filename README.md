# Battle-Bros-Game
Two characters choose superpowers and skins and go against each other in battle.
print("⚔Battle Bros⚔")
import random
import time
player1 = input("Enter name for Player 1: ")
player2 = input("Enter name for Player 2: ")
super_powers = ["Invisibility", "Super Strength", "Flight", "Telepathy", "Time Manipulation"]
power1 = random.choice(super_powers)
power2 = random.choice(super_powers)
print(f"{player1} has the super power: {power1}")
print(f"{player2} has the super power: {power2}")
skins = ["Dragon Skin", "Shadow Cloak", "Golden Armor", "Ice Shield", "Fire Aura"]
skin1 = random.choice(skins)
skin2 = random.choice(skins)
print(f"{player1} is equipped with: {skin1}")   
print(f"{player2} is equipped with: {skin2}")
health1 = 100
health2 = 100
while health1 > 0 and health2 > 0:
    attack1 = random.randint(10, 30)
    attack2 = random.randint(10, 30)
    health2 -= attack1
    health1 -= attack2
    print(f"{player1} attacks {player2} for {attack1} damage. {player2}'s health: {max(health2, 0)}")
    print(f"{player2} attacks {player1} for {attack2} damage. {player1}'s health: {max(health1, 0)}")
    time.sleep(1)
if health1 <= 0 and health2 <= 0:
    print("It's a draw!")
elif health1 <= 0:
    print(f"{player2} wins!")
else:
    print(f"{player1} wins!")
    
