# CONFIGURACIÓ DEL DOMINI

| Introducció |
|----------------------------------------|

Un cop tenim ja el nostre domini creat, el següent pas, és desplegar el domini, és a dir, crear els diferents objectes que el formaran: grups, usuaris, màquines. Aquí veurem la utilitat d’organitzar els objectes amb unitats organitzatives (OU).

Tenim l’opció de tenir una paperera de reciclatge pels objectes del directori, així si esborrem per error un objecte de l’AD el podrem recuperar.

![Tenim l’opció de tenir una paperera de reciclatge pels objectes del directori, així si esborrem per error un objecte de l’AD el podrem recuperar.](img/Imatge01.png)

![Tenim l’opció de tenir una paperera de reciclatge pels objectes del directori, així si esborrem per error un objecte de l’AD el podrem recuperar.](img/Imatge02.png)

Després de seleccionar, d’haver confirmat i refrescat el Manager ens surt.

![Després de seleccionar, d’haver confirmat i refrescat el Manager ens surt.](img/Imatge03.png)

| Procediment pràctic |
|----------------------------------------|

- Crear la següent estructura d’unitats organitzatives:

Anem a AD DS, fem click dret i anem a Active Directory Users and Computers (Usuaris i ordinadors d'Active Directory).

![Anem a AD DS, fem click dret i anem a Active Directory Users and Computers (Usuaris i ordinadors d'Active Directory).](img/Imatge04.png)

Ara creem la següent estructura d’unitats organitzatives: Grups i Usuaris. Creem aquestes 2 ja que així s’entén millor amb la pràctica, és més ordenat i clar i té més sentit.

![Ara creem la següent estructura d’unitats organitzatives: Grups i Usuaris. Creem aquestes 2 ja que així s’entén millor amb la pràctica, és més ordenat i clar i té més sentit.](img/Imatge05.png)

![Ara creem la següent estructura d’unitats organitzatives: Grups i Usuaris. Creem aquestes 2 ja que així s’entén millor amb la pràctica, és més ordenat i clar i té més sentit.](img/Imatge06.png)

![Ara creem la següent estructura d’unitats organitzatives: Grups i Usuaris. Creem aquestes 2 ja que així s’entén millor amb la pràctica, és més ordenat i clar i té més sentit.](img/Imatge07.png)

Resultat:

![Resultat](img/Imatge08.png)

- Definir la següent estructura de grups:

-gestio

-magatzem

-gerencia

-personal (tots els grups anteriors han de ser membres d’aquest grup)

Anem a Grups, click dret, New i Group.

![Anem a Grups, click dret, New i Group.](img/Imatge09.png)

I posem el nom del nou grup, gestio (així amb tots).

![I posem el nom del nou grup, gestio (així amb tots).](img/Imatge10.png)

Resultats:

![Resultats:](img/Imatge11.png)

Tots els grups anteriors han de ser membres del grup: personal. Per això escollim el grup personal, anem a Members, Add…

![Tots els grups anteriors han de ser membres del grup: personal. Per això escollim el grup personal, anem a Members, Add…](img/Imatge12.png)

I posem els grups. Acceptem (OK), Apply i OK. Ho fem amb els tres grups: gestio, magatzem i gerencia.

![I posem els grups. Acceptem (OK), Apply i OK. Ho fem amb els tres grups: gestio, magatzem i gerencia.](img/Imatge13.png)

![I posem els grups. Acceptem (OK), Apply i OK. Ho fem amb els tres grups: gestio, magatzem i gerencia.](img/Imatge13_.png)

Resultats:

![Resultats:](img/Imatge14.png)

- Crear una plantilla d’usuari per cadascun dels grups:

-Gestio

-Magatzem

-Gerencia

Cada plantilla ha de tenir definida la pertinença al grup i la creació de la carpeta personal.



![Resultats:](img/Imatge15.png)

![Resultats:](img/Imatge16.png)

![Resultats:](img/Imatge17.png)

![Resultats:](img/Imatge18.png)

![Resultats:](img/Imatge19.png)

![Resultats:](img/Imatge20.png)

![Resultats:](img/Imatge21.png)

![Resultats:](img/Imatge22.png)

![Resultats:](img/Imatge23.png)

![Resultats:](img/Imatge24.png)

![Resultats:](img/Imatge25.png)

![Resultats:](img/Imatge26.png)

![Resultats:](img/Imatge27.png)

![Resultats:](img/Imatge28.png)

![Resultats:](img/Imatge29.png)

![Resultats:](img/Imatge30.png)



- Definir un usuari de prova per cadascuna de les plantilles.



- Aprovisionar un equip que anomenarem PC1 dins la OU equips.



- Crear una VM amb Windows 11 amb 4 GB de RAM i disc suficient. La xarxa estarà en xarxa NAT. Un cop creat l’equip, agregeu-lo al domini.



- Comprovar el correcte funcionament, iniciant sessió a l’equip client amb els tres usuaris de prova.





[Anar a l'enunciat](../Tasca06/README.md)  
[Anar a la pàgina inicial](../README.md)
