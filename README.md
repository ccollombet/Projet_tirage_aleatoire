# Projet_tirage_aleatoire

#Coder un jeu de hasard

#Soit 10.000 lancers d'un dé équilibré classique (à 6 faces). Parmi ces 10.000 lancers, on en prend 1.000 aléatoirement.
On réalise 5 fois cette expérience, et on note m la moyenne des fréquences de 6 obtenus sur les 10.000 lancers et n la moyenne des fréquences de 4 obtenus dans le sous-échantillon.
Quelles seraient les valeurs de m et n à l'issue de cette expérience ?



Import random


m = 0
n = 0

for i in range(5): listeDe = []
j = 0

while j < 10000:
listeDe.append(random.randint(1, 6))
j += 1
sousEchantillonDe = random.sample(listeDe, 1000) m += listeDe.count(6)/10000
n += sousEchantillonDe.count(4)/1000

print("m =", m/5, "et n =", n/5)
