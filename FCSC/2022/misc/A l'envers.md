**Enoncée :**
Connectez-vous au service distant et pour chaque chaîne de caractères reçue, vous devez renvoyer la chaîne de caractères contenant les caractères dans l’ordre inverse.

**Exemple :** pour la chaîne `ANSSI`, vous devez renvoyer `ISSNA` (note : le respect de la casse est important).

**Résolution**
On comprend grâce au titre et à l'exemple que nous allons nous envoyé des chaînes de caractères et que nous devrons les renvoyés inversé.
Nous pouvons faire cela à la main mais il est plus simple de faire un script qui fait cela à notre place car nous ne savons pas combien de chaine de caractère nous devrions retourner.
Pour ma part j'ai choisi d'utiliser python avec la bibliothèque pwntools, voici mon script :
```
from pwn import *

  

def connect_to_localhost():

try:

conn = remote('localhost', 4000)

print("Connecté avec succès à localhost:4000")

while True :

# Établir une connexion à localhost:4000

response = conn.recvline().decode().split(" ")

response = response[1].split('\n')

response = response[0]

print(response)

chaine= response[::-1]

print(chaine)

conn.sendline(chaine.encode())

response = conn.recvline().decode()

print(response)

  

  

except PwnlibException as e:

print(f"Erreur de connexion : {e}")

finally:

if 'conn' in locals():

conn.close()

print("Connexion fermée")

  

if __name__ == "__main__":

connect_to_localhost()
```

Ce code va recevoir la chaine de caractère, l'afficher et la renvoyé au serveur inversé.

**Conclusion**

Une fois que nous avons inversé toutes les chaines de caractères nous recevons le flag : 
FCSC{7b20416c4f019ea4486e1e5c13d2d1667eebac732268b46268a9b64035ab294d}