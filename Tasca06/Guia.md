# CONFIGURACIÓ DEL DOMINI

| Introducció |
|----------------------------------------|

## Un cop tenim ja el nostre domini creat, el següent pas, és desplegar el domini, és a dir, crear els diferents objectes que el formaran: grups, usuaris, màquines. Aquí veurem la utilitat d’organitzar els objectes amb unitats organitzatives (OU).

Tenim l’opció de tenir una paperera de reciclatge pels objectes del directori, així si esborrem per error un objecte de l’AD el podrem recuperar.

![Tenim l’opció de tenir una paperera de reciclatge pels objectes del directori, així si esborrem per error un objecte de l’AD el podrem recuperar.](img/Imatge01.png)

![Tenim l’opció de tenir una paperera de reciclatge pels objectes del directori, així si esborrem per error un objecte de l’AD el podrem recuperar.](img/Imatge02.png)

Després de seleccionar, d’haver confirmat i refrescat el Manager ens surt.

![Després de seleccionar, d’haver confirmat i refrescat el Manager ens surt.](img/Imatge03.png)

| Procediment pràctic |
|----------------------------------------|

- ## Crear la següent estructura d’unitats organitzatives: Grups i Usuaris.

Anem a AD DS, fem click dret i anem a Active Directory Users and Computers (Usuaris i ordinadors d'Active Directory).

![Anem a AD DS, fem click dret i anem a Active Directory Users and Computers (Usuaris i ordinadors d'Active Directory).](img/Imatge04.png)

Ara creem la següent estructura d’unitats organitzatives: Grups i Usuaris. Creem aquestes 2 ja que així s’entén millor amb la pràctica, és més ordenat, clar i té més sentit.

![Ara creem la següent estructura d’unitats organitzatives: Grups i Usuaris. Creem aquestes 2 ja que així s’entén millor amb la pràctica, és més ordenat, clar i té més sentit.](img/Imatge05.png)

![Ara creem la següent estructura d’unitats organitzatives: Grups i Usuaris. Creem aquestes 2 ja que així s’entén millor amb la pràctica, és més ordenat, clar i té més sentit.](img/Imatge06.png)

![Ara creem la següent estructura d’unitats organitzatives: Grups i Usuaris. Creem aquestes 2 ja que així s’entén millor amb la pràctica, és més ordenat, clar i té més sentit.](img/Imatge07.png)

Resultat:

![Resultat](img/Imatge08.png)

- **Definir la següent estructura de grups:**

-**gestio**

-**magatzem**

-**gerencia**

-**personal (tots els grups anteriors han de ser membres d’aquest grup)**

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

- **Crear una plantilla d’usuari per cadascun dels grups:**

-**Gestio**

-**Magatzem**

-**Gerencia**

**Cada plantilla ha de tenir definida la pertinença al grup i la creació de la carpeta personal.**

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

*Aquest, per configurar la carpeta compartida, si no funciona per això, hem d’anar a domain users, edit, a Domain Users en els permisos marquem l’opció de Read/Write (Llegir/Escriure) i a la carpeta que hem creat (personal) com abans hem fet amb Everyone, en Domain Users, marquem les caselles de Full Control, Change i Read (Control total, canvi i lectura). 

Comprovació, Carpeta compartida, Permissions.

![*Aquest, per configurar la carpeta compartida, si no funciona per això, hem d’anar a domain users, edit, a Domain Users en els permisos marquem l’opció de Read/Write (Llegir/Escriure) i a la carpeta que hem creat (personal) com abans hem fet amb Everyone, en Domain Users, marquem les caselles de Full Control, Change i Read (Control total, canvi i lectura). 
Comprovació, Carpeta compartida, Permissions.](img/Imatge31.png)

Comprovació, Share.

![Comprovació, Share.](img/Imatge32.png)

Effective Access comprovació, per això anem a Select user, escollim (Domain Users) i View effective access (Veure l'accés efectiu).

![Effective Access comprovació, per això anem a Select user, escollim (Domain Users) i View effective access (Veure l'accés efectiu).](img/Imatge33.png)

Ara creem les plantilles d’usuari, fem click dret, New i User.

![Ara creem les plantilles d’usuari, fem click dret, New i User.](img/Imatge34.png)

Afegim.

![Afegim.](img/Imatge35.png)

No posem contrasenya, marquem la casellla de: Account is disabled (El compte està desactivat).

![No posem contrasenya, marquem la casellla de: Account is disabled (El compte està desactivat).](img/Imatge36.png)

Seguidament fem click dret a la plantilla d’usuari, Add to a group i afegim grup.

![Seguidament fem click dret a la plantilla d’usuari, Add to a group i afegim grup.](img/Imatge37.png)

Ara anem a Properties, Profile i creem la carpeta personal (usem la variable %username% que és el nom d’usuari, així a cada usuari se li crea la seva carpeta). Apply i OK. 

![Ara anem a Properties, Profile i creem la carpeta personal (usem la variable %username% que és el nom d’usuari, així a cada usuari se li crea la seva carpeta). Apply i OK. ](img/Imatge38.png)

![Ara anem a Properties, Profile i creem la carpeta personal (usem la variable %username% que és el nom d’usuari, així a cada usuari se li crea la seva carpeta). Apply i OK. ](img/Imatge39.png)

Fem aquest procediment amb tots 3 i hauria de quedar aixís:

![Fem aquest procediment amb tots 3 i hauria de quedar aixís:](img/Imatge40.png)

![Fem aquest procediment amb tots 3 i hauria de quedar aixís:](img/Imatge41.png)

- **Definir un usuari de prova per cadascuna de les plantilles.**

Fem click dret a una plantilla d’usuari i Copy.

![Fem click dret a una plantilla d’usuari i Copy.](img/Imatge42.png)

Definim usuari de prova.

![Definim usuari de prova.](img/Imatge43.png)

Password i posem: User must change password at next logon (User must change password at next logon).

![Password i posem: User must change password at next logon (User must change password at next logon).](img/Imatge44.png)

Fem aquest procediment de definir un usuari de prova per cadascuna de les plantilles.

![Fem aquest procediment de definir un usuari de prova per cadascuna de les plantilles.](img/Imatge45.png)

![Fem aquest procediment de definir un usuari de prova per cadascuna de les plantilles.](img/Imatge46.png)

![Fem aquest procediment de definir un usuari de prova per cadascuna de les plantilles.](img/Imatge47.png)

![Fem aquest procediment de definir un usuari de prova per cadascuna de les plantilles.](img/Imatge48.png)

Carpeta personal (usem la variable %username% que és el nom d’usuari, així a cada usuari se li crea la seva carpeta). Apply i OK. En Z ja que en D no es munta la unitat corresponent a la carpeta personal de l’usuari.

![Carpeta personal (usem la variable %username% que és el nom d’usuari, així a cada usuari se li crea la seva carpeta). Apply i OK. En Z ja que en D no es munta la unitat corresponent a la carpeta personal de l’usuari.](img/Imatge48_.png)

![Carpeta personal (usem la variable %username% que és el nom d’usuari, així a cada usuari se li crea la seva carpeta). Apply i OK. En Z ja que en D no es munta la unitat corresponent a la carpeta personal de l’usuari.](img/Imatge48_1.png)

![Carpeta personal (usem la variable %username% que és el nom d’usuari, així a cada usuari se li crea la seva carpeta). Apply i OK. En Z ja que en D no es munta la unitat corresponent a la carpeta personal de l’usuari.](img/Imatge48_2.png)

Resultats:

![Resultats:](img/Imatge49.png)

![Resultats:](img/Imatge50.png)

- **Aprovisionar un equip que anomenarem PC1 dins la OU equips.**

Creem una nou OU anomenada: equips.

![Creem una nou OU anomenada: equips.](img/Imatge51.png)

![Creem una nou OU anomenada: equips.](img/Imatge52.png)

![Creem una nou OU anomenada: equips.](img/Imatge53.png)

Ara fem click dret, New i Computer.

![Ara fem click dret, New i Computer.](img/Imatge54.png)

Aquest nou equip l’anomenem PC1.

![Aquest nou equip l’anomenem PC1.](img/Imatge55.png)

Resultat.

![Resultat.](img/Imatge56.png)

- Crear una VM amb Windows 11 amb 4 GB de RAM i disc suficient. La xarxa estarà en xarxa NAT. Un cop creat l’equip, agregeu-lo al domini.

Una vegada creat l’equip corresponentment, primer canviem el nom del PC a PC-1, per això anem a Sistema, Informació i canviar el nom d’aquest equip.

![Una vegada creat l’equip corresponentment, primer canviem el nom del PC a PC-1, per això anem a Sistema, Informació i canviar el nom d’aquest equip.](img/Imatge57.png)

Ara anem a Xarxa i Internet, Ethernet i editem la configuració DNS, posem l’IP del DC de l’altre màquina i guardem.

![Ara anem a Xarxa i Internet, Ethernet i editem la configuració DNS, posem l’IP del DC de l’altre màquina i guardem.](img/Imatge58.png)

Ara anem a Sistema, Informació, Domini o grup de treball i en Nom d’equip anem a Canviar.

![Ara anem a Sistema, Informació, Domini o grup de treball i en Nom d’equip anem a Canviar.](img/Imatge59.png)

I li posem el domini corresponent com podem veure:

![I li posem el domini corresponent com podem veure:](img/Imatge60.png)

Ara hem de posar el nom d’usuari i contrasenya: Administrator i P@ssw0rd

![Ara hem de posar el nom d’usuari i contrasenya: Administrator i P@ssw0rd](img/Imatge61.png)

I ara ja ens diu que s’ha unit correctament al domini translogic21.test i l’ordinador es reiniciarà.

![I ara ja ens diu que s’ha unit correctament al domini translogic21.test i l’ordinador es reiniciarà.](img/Imatge62.png)

- Comprovar el correcte funcionament, iniciant sessió a l’equip client amb els tres usuaris de prova.

Ara fem la comprovació amb els tres usuaris de prova (ens assegurem que iniciem sessió al domini i no a l’equip local).

![Ara fem la comprovació amb els tres usuaris de prova (ens assegurem que iniciem sessió al domini i no a l’equip local).](img/Imatge63.png)

Fem el canvi de contrasenya, ja que havíem marcat aquesta opció anteriorment per quan entressim.

![Fem el canvi de contrasenya, ja que havíem marcat aquesta opció anteriorment per quan entressim.](img/Imatge64.png)

Entra correctament.

![Entra correctament.](img/Imatge65.png)

Ara veiem com s’ha muntat unitat corresponent a la carpeta personal de l’usuari.

![Ara veiem com s’ha muntat unitat corresponent a la carpeta personal de l’usuari.](img/Imatge66.png)

Següent comprovació:

![Següent comprovació:](img/Imatge67.png)

![Següent comprovació:](img/Imatge68.png)

![Següent comprovació:](img/Imatge69.png)

Següent i última comprovació: 

![Següent i última comprovació:](img/Imatge70.png)

![Següent i última comprovació:](img/Imatge71.png)

![Següent i última comprovació:](img/Imatge72.png)

Aquí faig la comprovació de com entrant amb el compte de N.Lozano no puc entrar a una altra carpeta que no sigui la seva, per exemple intento entrar a la del B.Batalla i no deixa obtenir l'accés.

![Aquí faig la comprovació de com entrant amb el compte de N.Lozano no puc entrar a una altra carpeta que no sigui la seva, per exemple intento entrar a la del B.Batalla i no deixa obtenir l'accés.](img/Imatge73.png)

I aquí es veu com a la del N.Lozano sí que deixa (he creat un arxiu temporalment perquè es vegi que està sincronitzat).

![I aquí es veu com a la del N.Lozano sí que deixa (he creat un arxiu temporalment perquè es vegi que està sincronitzat).](img/Imatge74.png)

[Anar a l'enunciat](../Tasca06/README.md)  
[Anar a la pàgina inicial](../README.md)
