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

Ara creem la següent estructura d’unitats organitzatives: Grups i Usuaris. Creem aquestes 2 ja que així s’entén millor amb la pràctica, és més ordenat, clar i té més sentit.

![Ara creem la següent estructura d’unitats organitzatives: Grups i Usuaris. Creem aquestes 2 ja que així s’entén millor amb la pràctica, és més ordenat, clar i té més sentit.](img/Imatge05.png)

![Ara creem la següent estructura d’unitats organitzatives: Grups i Usuaris. Creem aquestes 2 ja que així s’entén millor amb la pràctica, és més ordenat, clar i té més sentit.](img/Imatge06.png)

![Ara creem la següent estructura d’unitats organitzatives: Grups i Usuaris. Creem aquestes 2 ja que així s’entén millor amb la pràctica, és més ordenat, clar i té més sentit.](img/Imatge07.png)

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

Primerament, amb la màquina aturada, anem a Paràmetres, Emmagatzematge i afegim un nou disc de 5 GB que serà on tindrem tota la informació en xarxa: carpetes personals, dels grups, etc.

![Primerament, amb la màquina aturada, anem a Paràmetres, Emmagatzematge i afegim un nou disc de 5 GB que serà on tindrem tota la informació en xarxa: carpetes personals, dels grups, etc.](img/Imatge15.png)

Ara dins, al Disk Management (Gestió de discs) anem al nou disc, l’inicialitzem, el formatem i l’anomenem DATA:

![Ara dins, al Disk Management (Gestió de discs) anem al nou disc, l’inicialitzem, el formatem i l’anomenem DATA:](img/Imatge16.png)

![Ara dins, al Disk Management (Gestió de discs) anem al nou disc, l’inicialitzem, el formatem i l’anomenem DATA:](img/Imatge17.png)

![Ara dins, al Disk Management (Gestió de discs) anem al nou disc, l’inicialitzem, el formatem i l’anomenem DATA:](img/Imatge18.png)

Comprovació:

![Comprovació:](img/Imatge19.png)

Ara a DATA, creem una carpeta personal. Es crearan unes carpetes pròpies per cada usuari del directori.

![Ara a DATA, creem una carpeta personal. Es crearan unes carpetes pròpies per cada usuari del directori.](img/Imatge20.png)

Ara per això fem click dret a la carpeta i Properties (Propietats).

![Ara per això fem click dret a la carpeta i Properties (Propietats).](img/Imatge21.png)

Seguidament en Sharing (Compartint), anem a Advanced Sharing (Compartició avançada).

![Seguidament en Sharing (Compartint), anem a Advanced Sharing (Compartició avançada).](img/Imatge22.png)

Ara anem a permissions (permisos).

![Ara anem a permissions (permisos).](img/Imatge23.png)

I marquem les caselles de Full Control, Change i Read (Control total, canvi i lectura), guardem i ja tindriem els permisos compartits activats.

![I marquem les caselles de Full Control, Change i Read (Control total, canvi i lectura), guardem i ja tindriem els permisos compartits activats.](img/Imatge24.png)

Ara passem als permisos locals, aquesta vegada anem a Security i Advanced (perquè és on tenim un control molt més afinat dels permisos de la carpeta).

![Ara passem als permisos locals, aquesta vegada anem a Security i Advanced (perquè és on tenim un control molt més afinat dels permisos de la carpeta).](img/Imatge25.png)

Seguidament anem a Disable inheritance (Disable inheritance).

![Seguidament anem a Disable inheritance (Disable inheritance).](img/Imatge26.png)

I ara escollim l’opció de: Convert inherited permissions into explicit permissions on this object (Converteix els permisos heretats en permisos explícits sobre aquest objecte).

![I ara escollim l’opció de: Convert inherited permissions into explicit permissions on this object (Converteix els permisos heretats en permisos explícits sobre aquest objecte).](img/Imatge27.png)

Ara canviem els permisos dels usuaris del grup “Domain Users” perquè només puguin llegir i escriure dins la seva carpeta personal. Per això anem a Add i Select a principal.

![Canviem els permisos dels usuaris del grup “Domain Users” perquè només puguin llegir i escriure dins la seva carpeta personal.](img/Imatge28.png)

Ara posem a Domain Users els permisos: Execute file, List folder/read data, Read attributes, Read extended attributes, Create folders i Read permissions (Executar fitxer, Llistar carpeta/llegir dades, Llegir atributs, Llegir atributs estesos, Crear carpetas i Permisos de lectura).

![Ara posem a Domain Users els permisos: Execute file, List folder/read data, Read attributes, Read extended attributes, Create folders i Read permissions (Executar fitxer, Llistar carpeta/llegir dades, Llegir atributs, Llegir atributs estesos, Crear carpetas i Permisos de lectura).](img/Imatge28_.png)

Després al CREATOR OWNER habilitem totes les opcions.

![Després al CREATOR OWNER habilitem totes les opcions.](img/Imatge29.png)

Resum carpeta personal.

![Resum carpeta personal.](img/Imatge30.png)

Comprovació, Carpeta compartida, Permissions.

![Comprovació, Carpeta compartida, Permissions.](img/Imatge31.png)

Comprovació, Share.

![Comprovació, Share.](img/Imatge32.png)

Effective Access comprovació, per això anem a Select user, escollim i View effective access (Veure l'accés efectiu).

![Effective Access comprovació, per això anem a Select user, escollim i View effective access (Veure l'accés efectiu).](img/Imatge33.png)

![Resultats:](img/Imatge34.png)

![Resultats:](img/Imatge35.png)

![Resultats:](img/Imatge36.png)

![Resultats:](img/Imatge37.png)

![Resultats:](img/Imatge38.png)

![Resultats:](img/Imatge39.png)

![Resultats:](img/Imatge40.png)

![Resultats:](img/Imatge41.png)

![Resultats:](img/Imatge42.png)

![Resultats:](img/Imatge43.png)

![Resultats:](img/Imatge44.png)

![Resultats:](img/Imatge45.png)

- Definir un usuari de prova per cadascuna de les plantilles.



- Aprovisionar un equip que anomenarem PC1 dins la OU equips.



- Crear una VM amb Windows 11 amb 4 GB de RAM i disc suficient. La xarxa estarà en xarxa NAT. Un cop creat l’equip, agregeu-lo al domini.



- Comprovar el correcte funcionament, iniciant sessió a l’equip client amb els tres usuaris de prova.





[Anar a l'enunciat](../Tasca06/README.md)  
[Anar a la pàgina inicial](../README.md)
