Difficulté : intro

Cette épreuve vous propose de déchiffrer un message chiffré avec la méthode inventée par [Blaise de Vigénère](https://fr.wikipedia.org/wiki/Chiffre_de_Vigen%C3%A8re). La clé est `FCSC` et le message chiffré est :

```
Gqfltwj emgj clgfv ! Aqltj rjqhjsksg ekxuaqs, ua xtwk
n'feuguvwb gkwp xwj, ujts f'npxkqvjgw nw tjuwcz
ugwygjtfkf qz uw efezg sqk gspwonu. Jgsfwb-aqmu f
Pspygk nj 29 cntnn hqzt dg igtwy fw xtvjg rkkunqf.
```

Le flag est le nom de la ville mentionnée dans ce message.

**Solution :**

On a ce message chiffré : 

*"Gqfltwj emgj clgfv ! Aqltj rjqhjsksg ekxuaqs, ua xtwk
n'feuguvwb gkwp xwj, ujts f'npxkqvjgw nw tjuwcz
ugwygjtfkf qz uw efezg sqk gspwonu. Jgsfwb-aqmu f
Pspygk nj 29 cntnn hqzt dg igtwy fw xtvjg rkkunqf."*

On nous dis dans l'énoncé que le message a été chiffré grâce à la méthode inventé par Blaise de Vigenère avec la clé qui est FCSC.
Une petite recherche sur internet nous permet de trouvé un décodeur en ligne qui nous donne ce message : 

*"Bonjour cher agent ! Votre prochaine mission, si vous
l'acceptez bien sur, sera d'infiltrer le reseau
souterrain ou se cache nos ennemis. Rendez-vous a
Nantes le 29 avril pour le debut de votre mission."*

**Conclusion :**

On Conclue donc que la ville mentionné dans le message est Nantes.
