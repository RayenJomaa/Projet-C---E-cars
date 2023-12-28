
![](Aspose.Words.5ea7dd9a-2e8c-4dda-9a21-72bfc151e25a.002.jpeg)

République Tunisienne
#### Université de la Mannouba
#### École Nationale des Sciences de l’Informatique
#### ENSI



![ref2]

**Projet C : Application de gestion d’une agence de location des voitures**

**E-Cars**

![ref2]






Réalisé par :

**Mohamed Rayen Jomaa**

**Groupe II1C**

` `**Encadré par :**


**Dr. Hatem Aouadi**



Année universitaire : **2023-2024**




**Table des matières**

[**Introduction générale**](#_bookmark0)	**1**

1. [Les structures](#_bookmark1)	2
   1. [Structure Date](#_bookmark2)	2
   1. [Structure Voiture](#_bookmark4)	2
   1. [Structure Location](#_bookmark6)	3
   1. [Structure Client](#_bookmark8)	3
   1. [Structure Resultat](#_bookmark10)	4

1. [Menu de l’application](#_bookmark12)	4
1. [Les prototypes](#_bookmark17)	6
1. [Realloc](#_bookmark18)	7
1. [Tableau dynamique d’adresses](#_bookmark21)	8
1. [Les fichiers](#_bookmark25)	9
1. [Les traitements](#_bookmark35)	17
   1. [La gestion des voitures](#_bookmark36)	17
   1. [La gestion des clients](#_bookmark43)	22

[**Conclusion générale**](#_bookmark50)	**25**

[**Annexes**](#_bookmark51)	**26**

**
![](Aspose.Words.5ea7dd9a-2e8c-4dda-9a21-72bfc151e25a.005.png)

**Table des figures**

1. [Code du structure Date](#_bookmark3)	2
1. [Code du structure Voiture](#_bookmark5)	3
1. [Code du structure Location](#_bookmark7)	3
1. [Code du structure Client](#_bookmark9)	4
1. [Code du structure Resultat](#_bookmark11)	4
1. [Menu principal](#_bookmark13)	5
1. [Menu de la gestion des clients](#_bookmark14)	5
1. [Menu de la gestion des voitures](#_bookmark15)	6
1. [La navigation entre les menus.](#_bookmark16)	6
1. [Prototypes des fonctions](#_bookmark19)	7
1. [Fonction realloc](#_bookmark20)	7
1. [Déclaration et allocation du tableau dynamique d’adresses](#_bookmark22)	8
1. [Remplissage du tableau résultat](#_bookmark23)	8
1. [Prototype du fonction du remplissage du tableau résultat](#_bookmark24)	9
1. [Création du fichier](#_bookmark26)	10
1. [Remplissage du fichier](#_bookmark27)	10
1. [Affichage du fichier](#_bookmark28)	10
1. [Lecture d’un client du fichier](#_bookmark29)	11
1. [Ecriture d’un client dans un fichier](#_bookmark30)	12
1. [Affichage du fichier clients](#_bookmark31)	13
1. [Affichage du fichier ClientsIndex](#_bookmark32)	14
1. [Modification d’un client à partir de sa position dans le fichier](#_bookmark33)	15
1. [Affichage du fichier apres modification](#_bookmark34)	16
1. [Code du tableau remplissage des voitures](#_bookmark37)	17
1. [Exécution du remplissage du tableau voitures](#_bookmark38)	18
1. [Modification d’une voiture](#_bookmark39)	19
1. [Exécution de modification d’une voiture](#_bookmark40)	20
1. [Suppression d’une voiture](#_bookmark41)	21
1. [Exécution de la suppression d’une voiture](#_bookmark42)	21
1. [Code de remplissage du tableau clients](#_bookmark44)	22
1. [Exécution du remplissage du tableau clients](#_bookmark45)	22
1. [Code d’affichage du tableau clients](#_bookmark46)	23
1. [Exécution de l’affichage du tableau clients](#_bookmark47)	23
1. [Code d’affichage du client qui a le plus grand nombre de locations](#_bookmark48)	24
1. [Exécution d’affichage du client qui a le plus grand nombre de locations](#_bookmark49)	24



# <a name="introduction_générale"></a><a name="_bookmark0"></a>**Introduction générale**

Les applications de gestion jouent un rôle crucial dans la rationalisation des opérations commerciales, et dans le secteur de la location de voitures, elles deviennent un outil inestimable pour optimiser l’efficacité opérationnelle. Dans le monde en constante évolution de la mobilité, les agences de location de voitures font face à des défis complexes liés à la gestion de flotte, à la réservation, à la maintenance des véhicules, à la satisfaction client, et à la croissance économique.

Dans ce rapport je vais présenter mon application de gestion d’une agence de location des voitures, nommée E-cars, réalisée en langage C.


![](Aspose.Words.5ea7dd9a-2e8c-4dda-9a21-72bfc151e25a.006.png)

1. ## <a name="_bookmark1"></a>**Les structures**
   1. ### <a name="_bookmark2"></a>**Structure Date**
La structure Date est composée par 3 champs : jour qui est de type **int**, mois de type

**int** et annee de type **int**. Elle permet de stocker une date.

La figure [1](#_bookmark3) ci-jointe représente une capture d’écran du code de définition du structure Date.

![](Aspose.Words.5ea7dd9a-2e8c-4dda-9a21-72bfc151e25a.007.jpeg)

<a name="_bookmark3"></a>**Fig. 1 : Code du structure Date**


1. ### <a name="_bookmark4"></a>**Structure Voiture**
La structure Voiture est composée par 5 champs : code qui est de type **int**, modele de type **char[50]**, marque de type **char[50]**, annee de type **int** qui désigne l’année de fabrication de la voiture et prixLocation de type **float**. Elle permet de stocker une voiture. La figure [2](#_bookmark5) ci-aprés représente une capture d’écran du code de définition du structure Voiture.


![](Aspose.Words.5ea7dd9a-2e8c-4dda-9a21-72bfc151e25a.008.png)

![](Aspose.Words.5ea7dd9a-2e8c-4dda-9a21-72bfc151e25a.009.jpeg)

<a name="_bookmark5"></a>**Fig. 2 : Code du structure Voiture**

1. ### <a name="_bookmark6"></a>**Structure Location**
La structure Location est composée par 4 champs : code qui est de type **int** qui est l’identifiant de la location (nombre aléatoire composé par 9 chiffres), voitureLouee qui est de type **VOITURE \*** (un pointeur sur voiture), dateDebut de type **DATE** et dateFin de type **DATE**. Cette structure permet de stocker les détails d’une location d’une voiture donnée.

![](Aspose.Words.5ea7dd9a-2e8c-4dda-9a21-72bfc151e25a.010.jpeg)La figure [3](#_bookmark7) ci-après représente une capture d’écran du code de définition du structure Location.

<a name="_bookmark7"></a>**Fig. 3 : Code du structure Location**




1. ### <a name="_bookmark8"></a>**Structure Client**
La structure Client est composée par 6 champs : prenom qui est de type **char[50]**, nom de type **char[50]**, téléphone de type **int**,le nombreLocations de type **int** et locations qui est de type **LOCATION \*** qui renseigne les locations d’un client donné. Cette structure permet de stocker les détails d’un client donné.

La figure [4](#_bookmark9) ci-aprés représente une capture d’écran du code de définition du structure Client.

![](Aspose.Words.5ea7dd9a-2e8c-4dda-9a21-72bfc151e25a.011.jpeg)

<a name="_bookmark9"></a>**Fig. 4 : Code du structure Client**

1. ### <a name="_bookmark10"></a>**Structure Resultat**
La structure Resultat est composée par 3 champs : nomClient qui est de type **char[50]**, prenomClient de type **char[50]** et nbLocations de type **int**. Cette structure permet de stocker le nombre de locations pour chaque client.

![](Aspose.Words.5ea7dd9a-2e8c-4dda-9a21-72bfc151e25a.012.jpeg)La figure [5](#_bookmark11) ci-jointe désigne une capture d’écran du code de définition du structure  Resultat.

<a name="_bookmark11"></a>**Fig. 5 : Code du structure Resultat**


1. ## <a name="_bookmark12"></a>**Menu de l’application**
Notre application est composée par un menu principal constitué par : La gestion des voitures et la gestion des clients.

La figure [6](#_bookmark13) ci-jointe représente le menu principal de notre application.

![](Aspose.Words.5ea7dd9a-2e8c-4dda-9a21-72bfc151e25a.013.png)

<a name="_bookmark13"></a>**Fig. 6 : Menu principal**

En choisissant une option, un sous menu apparait au chef d’agence pour manipuler soit les voitures soit les clients. Ci-après, la figure [7](#_bookmark14) renseigne le menu de la gestion des clients.

![](Aspose.Words.5ea7dd9a-2e8c-4dda-9a21-72bfc151e25a.014.png)

<a name="_bookmark14"></a>**Fig. 7 : Menu de la gestion des clients**

Et la figure [8](#_bookmark15) illustre le menu de la gestion des voitures.

![](Aspose.Words.5ea7dd9a-2e8c-4dda-9a21-72bfc151e25a.015.png)

<a name="_bookmark15"></a>**Fig. 8 : Menu de la gestion des voitures**

**Notez bien** : Il y’a une navigation entre les menus ; si le chef d’agence est dans le menu de la gestion des clients il peut revenir au menu principal comme le montre la figure [9](#_bookmark16).

![](Aspose.Words.5ea7dd9a-2e8c-4dda-9a21-72bfc151e25a.016.png)

<a name="_bookmark16"></a>**Fig. 9 : La navigation entre les menus.**


1. ## <a name="_bookmark17"></a>**Les prototypes**
La figure [10](#_bookmark19) ci-après illustre les prototypes des fonctions de notre application.

![](Aspose.Words.5ea7dd9a-2e8c-4dda-9a21-72bfc151e25a.017.jpeg)



1. ## <a name="_bookmark18"></a><a name="_bookmark19"></a>**Realloc**
**Fig. 10 : Prototypes des fonctions**

La fonction **realloc** en langage C est utilisée pour modifier la taille de la mémoire allouée dynamiquement précédemment par malloc, calloc, ou realloc lui-même. Elle permet de réallouer de la mémoire pour un bloc de mémoire déjà alloué, en modifiant sa taille.

Dans notre cas, nous avons utilisé **realloc** pour redimentionner le tableau des voitures. Si le chef d’agence veut ajouter des voitures supplémentaires en plus de sa base de données, il peut le faire grace à la fonction realloc.

Ci-dessous, nous avons présenter dans la figure [11](#_bookmark20) la capture d’écran de la fonction
##### ![](Aspose.Words.5ea7dd9a-2e8c-4dda-9a21-72bfc151e25a.018.png)**reallocVoiture**.

<a name="_bookmark20"></a>**Fig. 11 : Fonction realloc**

1. ## <a name="_bookmark21"></a>**Tableau dynamique d’adresses**
Lors du développement du mon application, j’ai recours à utiliser un tableau    dynamique d’adresses de structure RESULTAT.

![](Aspose.Words.5ea7dd9a-2e8c-4dda-9a21-72bfc151e25a.019.png)J’ai déclaré le tableau et allouer de l’espace mémoire de cette façon comme le montre la figure [14](#_bookmark24).

<a name="_bookmark22"></a>**Fig. 12 : Déclaration et allocation du tableau dynamique d’adresses**

La figure ci-après illustre le remplissage du tableau dynamique **tableauResultats**.

![](Aspose.Words.5ea7dd9a-2e8c-4dda-9a21-72bfc151e25a.020.png)









<a name="_bookmark23"></a>**Fig. 13 : Remplissage du tableau résultat**

![](Aspose.Words.5ea7dd9a-2e8c-4dda-9a21-72bfc151e25a.021.png)

<a name="_bookmark24"></a>**Fig. 14 : Prototype de fonction du remplissage du tableau résultat**
1. ## <a name="_bookmark25"></a>**Les fichiers**
J’ai utilisé deux fichiers binaires ; fichier Clients et fichier ClientsIndex. Le fichier Clients stocke les données des clients de l’agence alors que ClientsIndex stocke la position du curseur dans le fichier Clients. Les figures ci-après représente les fonctions de gestion des fichiers.

![](Aspose.Words.5ea7dd9a-2e8c-4dda-9a21-72bfc151e25a.022.jpeg)

![](Aspose.Words.5ea7dd9a-2e8c-4dda-9a21-72bfc151e25a.023.jpeg)<a name="_bookmark26"></a>**Fig. 15 : Création du fichier**

<a name="_bookmark27"></a>**Fig. 16 : Remplissage du fichier**

![](Aspose.Words.5ea7dd9a-2e8c-4dda-9a21-72bfc151e25a.024.jpeg)

<a name="_bookmark28"></a>**Fig. 17 : Affichage du fichier**

![](Aspose.Words.5ea7dd9a-2e8c-4dda-9a21-72bfc151e25a.025.jpeg)

<a name="_bookmark29"></a>**Fig. 18 : Lecture d’un client du fichier**

![](Aspose.Words.5ea7dd9a-2e8c-4dda-9a21-72bfc151e25a.026.jpeg)

<a name="_bookmark30"></a>**Fig. 19 : Ecriture d’un client dans un fichier** 










La figure [20](#_bookmark31) représente l’affichage du contenu du fichier Clients. 

![](Aspose.Words.5ea7dd9a-2e8c-4dda-9a21-72bfc151e25a.027.png)

**Fig. 20 : Affichage du fichier clients**








<a name="_bookmark31"></a>Ci-jointe, la figure [21](#_bookmark32) représente l’affichage du fichier ClientsIndex.

![](Aspose.Words.5ea7dd9a-2e8c-4dda-9a21-72bfc151e25a.028.png)


**Fig. 21 : Affichage du fichier ClientsIndex**



<a name="_bookmark32"></a>Grace à cette application, le chef d’agence a la main de modifier les données d’un client à partir de sa position dans le fichier comme illustre la figure [22 .](#_bookmark34)

![](Aspose.Words.5ea7dd9a-2e8c-4dda-9a21-72bfc151e25a.029.png)
























**Fig. 22 : Modification d’un client à partir de sa position dans le fichier**



![](Aspose.Words.5ea7dd9a-2e8c-4dda-9a21-72bfc151e25a.030.png)



<a name="_bookmark33"></a>**Fig. 23 : Affichage du fichier après modification**



1. ## <a name="_bookmark34"></a><a name="_bookmark35"></a>**Les traitements**
   1. ### <a name="_bookmark36"></a>**La gestion des voitures**
      0. ##### **Remplissage**
Ci-joint la figure [29](#_bookmark42) montre le code de remplissage du tableau voitures.

![](Aspose.Words.5ea7dd9a-2e8c-4dda-9a21-72bfc151e25a.031.png)

<a name="_bookmark37"></a>**Fig. 24 : Code du tableau remplissage des voitures**

![](Aspose.Words.5ea7dd9a-2e8c-4dda-9a21-72bfc151e25a.032.png)

<a name="_bookmark38"></a>**Fig. 25 : Exécution du remplissage du tableau voitures**
















0. ##### **Modification**
Ci-joint le code de modification d’une voiture


![](Aspose.Words.5ea7dd9a-2e8c-4dda-9a21-72bfc151e25a.033.jpeg)



![](Aspose.Words.5ea7dd9a-2e8c-4dda-9a21-72bfc151e25a.034.jpeg)


















**Fig. 26 : Modification d’une voiture**




![](Aspose.Words.5ea7dd9a-2e8c-4dda-9a21-72bfc151e25a.035.png)




































<a name="_bookmark39"></a>**Fig. 27 : Exécution de modification d’une voiture**




0. ##### <a name="_bookmark40"></a>**Suppression**
Ci-joint la figure [29](#_bookmark42) montre le code de suppression d’une voiture.

![](Aspose.Words.5ea7dd9a-2e8c-4dda-9a21-72bfc151e25a.036.jpeg)![](Aspose.Words.5ea7dd9a-2e8c-4dda-9a21-72bfc151e25a.037.jpeg)































**Fig. 28 : Suppression d’une voiture**



![](Aspose.Words.5ea7dd9a-2e8c-4dda-9a21-72bfc151e25a.038.png)

<a name="_bookmark43"></a><a name="_bookmark41"></a><a name="_bookmark42"></a>**Fig. 29 : Exécution de la suppression d’une voiture**

1. ### **La gestion des clients**
   0. ##### **Remplissage**
Ci-joint la figure [33](#_bookmark47) montre le code de remplissage du tableau des clients.

![](Aspose.Words.5ea7dd9a-2e8c-4dda-9a21-72bfc151e25a.039.jpeg)




<a name="_bookmark44"></a>**Fig. 30 : Code de remplissage du tableau clients**


![](Aspose.Words.5ea7dd9a-2e8c-4dda-9a21-72bfc151e25a.040.png)

<a name="_bookmark45"></a>**Fig. 31 : Exécution du remplissage du tableau clients**

0. ##### **Affichage**
Ci-joint la figure [33](#_bookmark47) montre le code d’affichage du tableau des clients.

![](Aspose.Words.5ea7dd9a-2e8c-4dda-9a21-72bfc151e25a.041.jpeg)


<a name="_bookmark46"></a>**Fig. 32 : Code d’affichage du tableau clients**

![](Aspose.Words.5ea7dd9a-2e8c-4dda-9a21-72bfc151e25a.042.png)










<a name="_bookmark47"></a>**Fig. 33 : Exécution de l’affichage du tableau clients**













0. ##### **Le client qui a le nombre de locations le plus élevé**
![](Aspose.Words.5ea7dd9a-2e8c-4dda-9a21-72bfc151e25a.043.jpeg)![](Aspose.Words.5ea7dd9a-2e8c-4dda-9a21-72bfc151e25a.044.jpeg)Ci-joint la figure [35](#_bookmark49) montre le code d’affichage du tableau des clients.
























`	`**Fig. 34 : Code d’affichage du client qui a le plus grand nombre de locations**






![](Aspose.Words.5ea7dd9a-2e8c-4dda-9a21-72bfc151e25a.045.png)

<a name="_bookmark48"></a><a name="_bookmark49"></a>**Fig. 35 : Exécution d’affichage du client qui a le plus grand nombre de locations**



# <a name="conclusion_générale"></a><a name="_bookmark50"></a>**Conclusion générale**

**Conclusion générale**

En conclusion, la création d’une application de gestion pour une agence de location de voitures en langage C a été une expérience enrichissante. Ce projet m’a offert l’opportunité d’approfondir mes connaissances en programmation et de développer des compétences précieuses dans plusieurs domaines.

Travailler en langage C m’a permis de maîtriser les aspects fondamentaux de la programmation, notamment la gestion de la mémoire, la manipulation des pointeurs et la modularité du code. La conception modulaire du système, avec ses différents modules pour la gestion des véhicules, des clients, et des locations, a renforcé ma compréhension de l’organisation logicielle.








# <a name="annexes"></a><a name="_bookmark51"></a>**Annexes**

[ref1]: Aspose.Words.5ea7dd9a-2e8c-4dda-9a21-72bfc151e25a.001.png
[ref2]: Aspose.Words.5ea7dd9a-2e8c-4dda-9a21-72bfc151e25a.003.png
