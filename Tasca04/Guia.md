# INSTAL·LACIÓ WINDOWS SERVER 2025

| Procediment |
|----------------------------------------|

- Crea una màquina virtual amb 8 GB de RAM i dos processadors. La VM disposarà de dos discos, un de 32 GB com a disc principal (on instal·lareu el SO) i un de secundari de 10 GB. La màquina haurà de tenir dues interfícies de xarxa: una en xarxa NAT (no NAT) i la segona en host-only.

Comencem creant la màquina, posant, nom, la ISO, Folder i posem l’opció del Skip Unattended Installation (Omet la instal·lació desatès).

![Comencem creant la màquina, posant, nom, la ISO, Folder i posem l’opció del Skip Unattended Installation (Omet la instal·lació desatès).](Img/Imatge01.png)

Després de RAM posem 8 GB (8192 MB) i dos processadors.

![Després de RAM posem 8 GB (8192 MB) i dos processadors.](Img/Imatge02.png)

La VM disposarà de dos discos, un de 32 GB com a disc principal (on instal·larem el SO) i un de secundari de 10 GB. 

![La VM disposarà de dos discos, un de 32 GB com a disc principal (on instal·larem el SO) i un de secundari de 10 GB. ](Img/Imatge03.png)

![La VM disposarà de dos discos, un de 32 GB com a disc principal (on instal·larem el SO) i un de secundari de 10 GB. ](Img/Imatge04.png)

La màquina tindrà dues interfícies de xarxa: una en xarxa NAT (no NAT) i la segona en host-only.

![La màquina tindrà dues interfícies de xarxa: una en xarxa NAT (no NAT) i la segona en host-only.](Img/Imatge05.png)

![La màquina tindrà dues interfícies de xarxa: una en xarxa NAT (no NAT) i la segona en host-only.](Img/Imatge06.png)

- Instal·la Windows Server 2025 en mode GUI, idioma US però configuració i teclat en espanyol.

Comencem la instal·lació, posarem d’idioma l’anglès (ja que és com es solen configurar els servers) i el teclat i configuracions regionals en espanyol. 

![Comencem la instal·lació, posarem d’idioma l’anglès (ja que és com es solen configurar els servers) i el teclat i configuracions regionals en espanyol. ](Img/Imatge07.png)

El teclat i mètode d'entrada en espanyol.

![El teclat i mètode d'entrada en espanyol.](Img/Imatge08.png)

Instal·lem Windows Server.

![Instal·lem Windows Server.](Img/Imatge09.png)

Instal·lem Windows Server 2025 en mode GUI.

![Instal·lem Windows Server 2025 en mode GUI.](Img/Imatge10.png)

Acceptem els termes (EULA).

![Acceptem els termes (EULA).](Img/Imatge11.png)

Escollim el disc principal.

![Escollim el disc principal.](Img/Imatge12.png)

Instal·lem.

![Instal·lem.](Img/Imatge13.png)

Configurem el compte d’Administrator, el qual l’user name (nom d'usuari) és Administrador i de contrasenya posem: P@ssw0rd.

![Configurem el compte d’Administrator, el qual l’user name (nom d'usuari) és Administrador i de contrasenya posem: P@ssw0rd.](Img/Imatge14.png)

- Canvia el nom de l’equip a DCxx (xx és el vostre número de llista).

Canviem el nom de l’equip a DCxx (DC21), per això desde Server Manager anem a Computer name (nom de l'ordinador), Change (canviar) i posem el nou nom.

![Canviem el nom de l’equip a DCxx (DC21), per això desde Server Manager anem a Computer name (nom de l'ordinador), Change (canviar) i posem el nou nom.](Img/Imatge15.png)

Reiniciem.

![Reiniciem.](Img/Imatge16.png)

I veiem com s’ha canviat el nom.

![I veiem com s’ha canviat el nom.](Img/Imatge17.png)

- Actualitza la màquina virtual (un cop fet, pausa les actualitzacions tot el temps que sigui possible).

Ara anem a configuració, Windows Update i fem les actualitzacions.

![Ara anem a configuració, Windows Update i fem les actualitzacions.](Img/Imatge18.png)

Actualitzacions fetes.

![Actualitzacions fetes.](Img/Imatge19.png)

Pausem les actualitzacions tot el temps que sigui possible (5 setmanes).

![Pausem les actualitzacions tot el temps que sigui possible (5 setmanes).](Img/Imatge20.png)

| Contingut de la guia |
|----------------------------------------|

**Compara la configuració de la màquina virtual definits a l’apartat anterior amb els requisits indicats per Microsoft. Són coherents?**

La configuració de la màquina virtual utilitzada és coherent amb els requisits oficials de Microsoft per a Windows Server 2025. El servidor virtual té 2 processadors, tot i que Microsoft només en demana 1, i té 8 GB de memòria RAM, que és molt més del mínim necessari perquè Windows Server amb pantalla gràfica funcioni bé.                 L’emmagatzematge, el disc principal de 32 GB compleix exactament el mínim requerit pel sistema operatiu, i el disc secundari de 10 GB aporta espai addicional (útil per a rols o dades). Finalment, les dues interfícies de xarxa configurades (NAT i Host‑Only) també s’ajusten als requisits, ja que Microsoft només demana un adaptador compatible.

**Documenta els diversos procediments de la instal·lació amb captures de pantalla i observacions. Recorda que el format a utilitzar és MarkDown.**

[Anar a l'enunciat](../Tasca04/README.md)  
[Anar a la pàgina inicial](../README.md)
