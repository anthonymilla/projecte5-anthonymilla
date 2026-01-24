# INSTAL·LACIÓ DEL DOMINI

| Procediment a documentar |
|----------------------------------------|

- Instal·lar els rols necessaris al servidor.

Primerament anem a configuració, Network & internet (Xarxa i Internet), després a Ethernet i Edit (editar) en DNS server assignment (Assignació del servidor DNS).

![Primerament anem a configuració, Network & internet (Xarxa i Internet), després a Ethernet i Edit (editar) en DNS server assignment (Assignació del servidor DNS).](Img/Imatge01.png)

En Manual, ara en IPv4 (On) posem com a IP 127.0.0.1 i save (guardar).

![En Manual, ara en IPv4 (On) posem com a IP 127.0.0.1 i save (guardar).](Img/Imatge02.png)

Després a Server Manager, en Manage (Gestionar), cliquem l’opció de Add Roles and Features (Afegir rols i funcions).

![Després a Server Manager, en Manage (Gestionar), cliquem l’opció de Add Roles and Features (Afegir rols i funcions).](Img/Imatge03.png)

Ara anem a Installation Type i marquem l’opció de Role-based or feature-based installation (Instal·lació basada en rols o funcions) i Next.

![Ara anem a Installation Type i marquem l’opció de Role-based or feature-based installation (Instal·lació basada en rols o funcions) i Next.](Img/Imatge04.png)

En Server Selection hem de tenir marcat l’opció de Select a server from the server pool, permet instal·lar rols de forma centralizada al diferents servidors del domini.

![En Server Selection hem de tenir marcat l’opció de Select a server from the server pool, permet instal·lar rols de forma centralizada al diferents servidors del domini.](Img/Imatge05.png)

Activem l’opció de Active Directory Domain Services i seguidament Add Roles and Features Wizard.

![Activem l’opció de Active Directory Domain Services i seguidament Add Roles and Features Wizard.](Img/Imatge06.png)

AD DS, Next.

![AD DS, Next.](Img/Imatge07.png)

I el sistema marca per defecte els features associats al rol que es vol instal·lar.

![I el sistema marca per defecte els features associats al rol que es vol instal·lar.](Img/Imatge08.png)

![I el sistema marca per defecte els features associats al rol que es vol instal·lar.](Img/Imatge09.png)

Ara la confirmació, marquem l’opció Restart i Install.

![Ara la confirmació, marquem l’opció Restart i Install.](Img/Imatge10.png)

- Crear un domini nou en bosc nou anomenat translogicXX.test on XX és el vostre nº de llista.

Després de la instal·lació ens surt aquest missatge Post-deployment Configuration (Configuració posterior al desplegament) i cliquem en Promote this server to a domain controller (Promoure aquest servidor a controlador de domini).

![Després de la instal·lació ens surt aquest missatge Post-deployment Configuration (Configuració posterior al desplegament) i cliquem en Promote this server to a domain controller (Promoure aquest servidor a controlador de domini).](Img/Imatge11.png)

Creem un domini nou en bosc nou anomenat translogic21.test.

![Creem un domini nou en bosc nou anomenat translogic21.test.](Img/Imatge12.png)

- Establir el nivell funcional a 2025.

 Establim el nivell funcional a 2025 i posem de Password pel Restore Mode: P@ssw0rd.

![Establim el nivell funcional a 2025 i posem de Password pel Restore Mode: P@ssw0rd.](Img/Imatge13.png)

- Promocionar el servidor com a controlador de domini:

-Important documentar la pantalla resum.

-Grava a un arxiu l’script PowerShell que permet automatitzar el procés.

Anem a DNS Options i Next. Com que fa servir DNS i no troba cap equip amb el domini indicat, ens informa i instal·la el rol al DC (controlador de domini).

![Anem a DNS Options i Next. Com que fa servir DNS i no troba cap equip amb el domini indicat, ens informa i instal·la el rol al DC (controlador de domini).](Img/Imatge14.png)

Després en NetBIOS domain name (Nom de domini NetBIOS), assigna automàticament un nom: TRANSLOGIC21, Next.

![Després en NetBIOS domain name (Nom de domini NetBIOS), assigna automàticament un nom: TRANSLOGIC21, Next.](Img/Imatge15.png)

Paths, continuem.

![Paths, continuem.](Img/Imatge16.png)

- Important documentar la pantalla resum.

Review Options. Bàsicament ens mostra un resum de les opcions escollides i permet generar un script PowerShell amb elles, està molt bé per replicar configuracions. Ara cliquem View script.

![Review Options. Bàsicament ens mostra un resum de les opcions escollides i permet generar un script PowerShell amb elles, està molt bé per replicar configuracions. Ara cliquem View script.](Img/Imatge17.png)

- Grava a un arxiu l’script PowerShell que permet automatitzar el procés.

Script PowerShell. El guardem i continuem (en downloads en aquest cas).

![Grava a un arxiu l’script PowerShell que permet automatitzar el procés. Script PowerShell. El guardem i continuem (en downloads en aquest cas).](Img/Imatge18.png)

![Grava a un arxiu l’script PowerShell que permet automatitzar el procés. Script PowerShell. El guardem i continuem (en downloads en aquest cas).](Img/Imatge19.png)

Ara en Prerequisites Check (Comprovació de requisits previs) cliquem en Instal·lar (Install).

![Ara en Prerequisites Check (Comprovació de requisits previs) cliquem en Instal·lar (Install).](Img/Imatge20.png)

![Ara en Prerequisites Check (Comprovació de requisits previs) cliquem en Instal·lar (Install).](Img/Imatge21.png)

I ja estaria, el Domain Controller operatiu.

![I ja estaria, el Domain Controller operatiu.](Img/Imatge22.png)

![I ja estaria, el Domain Controller operatiu.](Img/Imatge23.png)

Posem la zona horària corresponent, Madrid, UTC+01:00, ajustem l’hora correcta (Time & language -> Date & time/Hora i idioma -> Data i hora).

![Posem la zona horària corresponent, Madrid, UTC+01:00, ajustem l’hora correcta (Time & language -> Date & time/Hora i idioma -> Data i hora).](Img/Imatge24.png)

Ara anem a Server Manager, DNS, clic dret i DNS Manager (El servidor DNS pot consultar Internet directament. Afegim un reenviador per fer-ho més ràpid i amb menys càrrega).

![Ara anem a Server Manager, DNS, clic dret i DNS Manager (El servidor DNS pot consultar Internet directament. Afegim un reenviador per fer-ho més ràpid i amb menys càrrega).](Img/Imatge25.png)

Forwarders.

![Forwarders.](Img/Imatge26.png)

I posem 8.8.8.8 com a reenviador i en Number of seconds before forward queries time out (Nombre de segons abans que s'esgoti el temps d'espera de les consultes de reenviament) posem 5.

![I posem 8.8.8.8 com a reenviador i en Number of seconds before forward queries time out (Nombre de segons abans que esgoti el temps d'espera de les consultes de reenviament) posem 5.](Img/Imatge27.png)

![I posem 8.8.8.8 com a reenviador i en Number of seconds before forward queries time out (Nombre de segons abans que esgoti el temps d'espera de les consultes de reenviament) posem 5.](Img/Imatge28.png)

Apply.

![Apply.](Img/Imatge29.png)

Un cop teniu tot els procediment finalitzat, copieu l’script PowerShell a la carpeta del repositori que esteu utilitzant. Per fer-ho teniu diversos mecanismes:

- Copiar usant USB.

- Enviant-lo mitjançant Internet (correu, Drive o serveis com filetransfer)

- Copiant-lo usant scp (cal que instal·leu el SSH a Windows Server)

En aquest cas mitjançant correu.

![Un cop teniu tot els procediment finalitzat, copieu l’script PowerShell a la carpeta del repositori que esteu utilitzant. Per fer-ho teniu diversos mecanismes: Copiar usant USB. Enviant-lo mitjançant Internet (correu, Drive o serveis com filetransfer). Copiant-lo usant scp (cal que instal·leu el SSH a Windows Server). En aquest cas mitjançant correu.](Img/Imatge30.png)

![Un cop teniu tot els procediment finalitzat, copieu l’script PowerShell a la carpeta del repositori que esteu utilitzant. Per fer-ho teniu diversos mecanismes: Copiar usant USB. Enviant-lo mitjançant Internet (correu, Drive o serveis com filetransfer). Copiant-lo usant scp (cal que instal·leu el SSH a Windows Server). En aquest cas mitjançant correu.](Img/Imatge31.png)

```
#
# Windows PowerShell script for AD DS Deployment
#

Import-Module ADDSDeployment
Install-ADDSForest `
-CreateDnsDelegation:$false `
-DatabasePath "C:\WINDOWS\NTDS" `
-DomainMode "Win2025" `
-DomainName "translogic21.test" `
-DomainNetbiosName "TRANSLOGIC21" `
-ForestMode "Win2025" `
-InstallDns:$true `
-LogPath "C:\WINDOWS\NTDS" `
-NoRebootOnCompletion:$false `
-SysvolPath "C:\WINDOWS\SYSVOL" `
-Force:$true
```

[Anar a l'enunciat](../Tasca05/README.md)  
[Anar a la pàgina inicial](../README.md)
