# T04-Introducció al cas

Després del nostre assessorament, TransLògic S.A. ens encarrega el desplegament dels seus servidors Windows Servers 2025.

Per aquest motiu, haurem de desplegar diverses màquines virtuals i amb l’objectiu de ser eficients i seguir bones pràctiques, realitzarem una instal·lació de prova que servirà tant per aprendre els procediments com per elaborar una guia de instal·lació, que ha de proporcionar una documentació de base a la posterior implantació als sistemes del client.

---

# Procediment

- Crea una màquina virtual amb 8 GB de RAM i dos processadors. La VM disposarà de dos discos, un de 32 GB com a disc principal (on instal·lareu el SO) i un de secundari de 10 GB. La màquina haurà de tenir dues interfícies de xarxa: una en xarxa NAT (no NAT) i la segona en host-only.
- Instal·la Windows Server 2025 en mode GUI, idioma US però configuració i teclat en espanyol.
- Canvia el nom de l’equip a DCxx (xx és el vostre número de llista).
- Actualitza la màquina virtual (un cop fet, pausa les actualitzacions tot el temps que sigui possible).

---

# Contingut de la guia

- Compara la configuració de la màquina virtual definits a l’apartat anterior amb els requisits indicats per Microsoft. Són coherents?
- Documenta els diversos procediments de la instal·lació amb captures de pantalla i observacions. Recorda que el format a utilitzar és MarkDown.

---

# Materials i links de suport

- UD.6. AA2. Instal·lació Window Server 2025 [Moodle 0224 Sist. Operatius en Xarxa]
- Requisitos de hardware para Windows Server. Microsoft Learn [(enllaç)](https://learn.microsoft.com/es-es/windows-server/get-started/hardware-requirements?tabs=cpu&pivots=windows-server-2025)

# T05-Introducció

Com a continuació de la tasca anterior, us toca desplegar el directori actiu sobre la màquina virtual amb l’objectiu de practicar pel posterior desplegament en el client. A més, aquest procediment us ha de servir com a prova de concepte (PoC) per mostrar als responsables de TransLògic i d’aquesta manera, ajustar les configuracions a les necessitats reals del client.

---

# Procediment a documentar

- Instal·lar els rols necessaris al servidor.
- Crear un domini nou en bosc nou anomenat **translogicXX.test** on XX és el vostre nº de llista.
- Establir el nivell funcional a **2025**.
- Promocionar el servidor com a controlador de domini:
  - Important documentar la pantalla resum.
  - Grava a un arxiu l’script PowerShell que permet automatitzar el procés.
- Un cop teniu tot els procediment finalitzat, copieu l’script PowerShell a la carpeta del repositori que esteu utilitzant. Per fer-ho teniu diversos mecanismes:
  - Copiar usant USB.
  - Enviant-lo mitjançant Internet (correu, Drive o serveis com filetransfer)
  - Copiant-lo usant **scp** (cal que instal·leu el SSH a Windows Server)

---

# Materials i links de suport

- Guia **UD6.AA3 Instal·lació DC** [Moodle SOX]

[Anar a la Guia](../Tasca04_05/Guia.md)     
[Anar a la pàgina inicial](../README.md)

