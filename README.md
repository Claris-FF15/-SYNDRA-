3 exo programmation du 3/10/2024

# exo 1 sur TVA 21%  , entrer my chiffres HTVA et afficher le résultat

HTVA = int ( input ( " veuillez entrer un prix hors taxe : " ) )

TVA = ( (HTVA/ 100 ) * 21 )

print( HTVA + TVA)


"""  exo 2 : demander d'encoder 3 longueurs d'un triangle. 
    si la som des 2 cotés > ou = au troisième coté , afficher alors c'est un triangle 
    a l'inverse afficher ce n'est pas un triangle """

A = int (input ( " donnez une longueur1 d'un triangle : "))
B = int ( input (" donnez une longueur2 d'un triangle : "))
C = int ( input ( " donnez une longueur3 d'un triangle : "))

if (A + B) >= C :
     print ( " c'est un triangle " )
else:
     print ( " ce n'est pas un triangle " )


 """ exo 3 : On demande à un utilisateur d’encoder une date: jour, mois année (3 valeurs entières)
- on doit vérifier si l’année est correcte (entre 0 et 2999)
- on doit vérifier si le mois encodé est correct (1 - 12)
- on doit vérifier si le jour est correct: 28, 29, 30 ou 31 jours suivant les conditions suivantes:
* Si le mois a 30 jours (avril, juin, septembre, novembre), le nombre de jours maximum est 30
* Si le mois a 31 jours (janvier, mars, mai, juillet, août, octobre, décembre), le nombre de jours maximum est
31
* Si le mois est février et l’année est bissextile, le nombre de jours maximum est 29.
* Si le mois est février et l’année n’est pas bissextile, le nombre de jours maximum est 28.
Si la date est correcte, afficher «date correcte».
. Si pas,afficher date invalide»."""

Day = int ( input (" enter a day :  ") )
Month = int ( input ( " enter a month : " ) )
Year = int ( input ( " enter a year : ") )

if (Month == 4 or Month == 6  or Month== 9 or Month == 11 ) and Day < 30 :
    print ( " correct date " )
elif ( Month== 1 or Month==3 or Month==5 or Month==7 or Month==9 or Month==10 or Month==12) and Day < 21 :
    print (" correct date ")
elif ( Month == 2 and Year %4==1) and Day < 29 : 
    print (" correct date ")
elif ( Year >= 0 and Year <= 2999 ) and ( Month >= 1 and Month <= 12 ):
    print( " correct date " )
else : 
    print ( " incorrect date ")
