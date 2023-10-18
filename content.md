## Izveidot number guessing spēli ar Python programmēšanas valodu
### Dokumenta saturs
#### Spēles apraksts
#### Spēles loģika

Dators nejauši ģenerē vienu skaitli no 1 līdz 100. Tālāk, piedāvā spēlētājam uzminēt to skaitli Un t.t.
Speles loģika ir labi aprakstīta šajā kodā:
```py
 import random
 
repeat = True

while repeat:
    number = random.randint(1, 100)
    guess = 0
    tries = 0


while guess != number:
    if guess < number:
        print("Pamēģini lielāku skaitli!")
    else:
        print("Pamēģini mazāku skaitli!")

    guess = int(input("Uzmini skaitli: "))
    tries += 1
else:
    if tries < 4:
        print(f"WOW! Tu uzminēji pēc {tries} reizēm!")
    elif tries < 7:
        print(f"Nav slikti,uzminēji pēc {tries} reizēm!")
    else:
        print(f"Hmm.... slikti,uzminēji pēc {tries} reizēm!")

response = input("Vai gribi turpināt? y/n:") 
if response == "y":
    repeat = True
elif response == "n":
    repeat = False
    print("Paldies par spēli! Bye, bye!")
else:
    repeat = False
    print("Paldies par spēli! Bye, bye!")
```
#### 3. Un t.t
