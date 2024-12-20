import random

def spielen():
print("Willkommen bei 'Tebak Angka'!")
zahl = random.randint(1, 100)
versuche = 0

while True:
versuche += 1
eingabe = input("Rate eine Zahl zwischen 1 und 100: ")
if not eingabe.isdigit():
print("Bitte gib eine Zahl ein!")
elif int(eingabe) < zahl:
print("Die Zahl ist höher!")
elif int(eingabe) > zahl:
print("Die Zahl ist niedriger!")
else:
print(f"Glückwunsch! Du hast die Zahl in {versuche} Versuchen erraten!")
break

def main():
spielen()
spielen_nochmal = input("Möchtest du nochmal spielen? (ja/nein): ")
if spielen_nochmal.lower() == "ja":
main()
else:
print("Danke für das Spielen!")

if *name* == "*main*":
main()