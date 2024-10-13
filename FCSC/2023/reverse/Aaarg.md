

**Ennoncé** 

Vous devez afficher le flag, quelque soit le moyen utilisé !

**Résolution**

On a un fichier nommé aaarg.
grâce à la commande file on apprend que c'est un fichier ELF.

J'ouvre donc le fichier avec Binary Ninja et j'analyse un peu le code décompilé :
![[Pasted image 20241013190553.png]] 

je décide d'aller voir ce qui est stocké à l'addresse mémoire 0x402010 :

![[Pasted image 20241013190735.png]]  

On apperçoit à droite le format du flag, j'ai donc juste à recopier le flag pour pouvoir valider ce challenge.

**Conclusion**

Après avoir récupéré chaque caractère je me retrouve avec la flag : FCSC{f9a38adace9dda3a9ae53e7aec180c5a73dbb7c364fe137fc6721d7997c54e8d}

Je peux donc valider le challenge.