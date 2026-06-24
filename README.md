import random
import os

# ==========================
# WORDS AND HINTS
# ==========================
word_bank = {
    "Pizza": "Food item",
    "Tiger": "Wild animal",
    "Football": "Popular sport",
    "Laptop": "Electronic device",
    "Beach": "Vacation place",
    "Mountain": "Natural landform",
    "Doctor": "Medical profession",
    "Airplane": "Mode of transport",
    "Chocolate": "Sweet treat",
    "Library": "Place full of books",
    "Cricket": "Outdoor sport",
    "Elephant": "Large animal",
    "School": "Place of learning",
    "Camera": "Used for photography",
    "Train": "Public transport"
}


# ==========================
# CLEAR SCREEN FUNCTION
# ==========================
def clear_screen():
    os.system('cls' if os.name == 'nt' else 'clear')


# ==========================
# GAME START
# ==========================
print("=" * 40)
print("        IMPOSTER WORD GAME")
print("=" * 40)

num_players = int(input("Enter number of players: "))
num_imposters = int(input("Enter number of imposters: "))

while num_imposters >= num_players:
    print("\n❌ Number of imposters must be less than players.")
    num_imposters = int(input("Enter number of imposters again: "))

# Select random word and hint
word = random.choice(list(word_bank.keys()))
hint = word_bank[word]

# Select random imposters
imposters = random.sample(range(1, num_players + 1), num_imposters)

clear_screen()

# ==========================
# SHOW ROLES TO PLAYERS
# ==========================
for player in range(1, num_players + 1):

    print(f"\nPlayer {player}, take the device.")
    input("Press ENTER to reveal your role...")

    clear_screen()

    print("=" * 40)

    if player in imposters:
        print("🚨 YOU ARE THE IMPOSTER 🚨")
        print(f"\nHint: {hint}")
    else:
        print("✅ YOUR SECRET WORD IS:")
        print(f"\n>>> {word} <<<")

    print("=" * 40)

    input("\nPress ENTER to hide your role...")

    clear_screen()

    if player != num_players:
        print("Pass the device to the next player.")
        input("Press ENTER when the next player is ready...")
        clear_screen()

# ==========================
# DISCUSSION PHASE
# ==========================
print("=" * 40)
print(" ALL PLAYERS HAVE SEEN THEIR ROLES ")
print("=" * 40)

input("\nPress ENTER to start the discussion round...")

clear_screen()

print("=" * 40)
print(" DISCUSSION ROUND ")
print("=" * 40)

print("\nDiscuss among yourselves and find the imposters!")
print("When you're ready, reveal the imposters.")

input("\nPress ENTER to reveal the imposters...")

clear_screen()

# ==========================
# REVEAL IMPOSTERS
# ==========================
print("=" * 40)
print("      IMPOSTER REVEALED")
print("=" * 40)

for imposter in imposters:
    print(f"🚨 Player {imposter} was an IMPOSTER!")

print(f"\nSecret Word: {word}")

print("\nThanks for playing!")
print("=" * 40)
