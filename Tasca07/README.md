# Enunciat

# Acadèmia feta amb Moodle

# Part 1: Instal·lar un sistema de gestió d’aprenentatge a distància, personalitzar-lo i configurar-lo segons les necessitats d’una organització

Una escola d'ensenyament secundari, anomenada Escola Júlia, ens ha demanat el desenvolupament d'un portal web d'aprenentatge amb l'objectiu d'oferir, tan als professors com als alumnes, una plataforma online que faciliti la comunicació i l'aprenentatge. Per tal de crear aquest portal, s'ha decidit utilitzar l'aplicació web Moodle.

Segueix les indicacions que es mostren a continuació per tal d'adaptar el Moodle a les necessitats del client.

## 1. Instal·lació inicial

El primer que haurem de fer es descomprimir el Moodle al nostre servidor web. Un cop disposem de l'aplicació allotjada al servidor, accedirem a través del navegador per començar la instal·lació.

Com podràs observar, serà necessari crear una base de dades. Indica que utilitzarem una base de dades de **MySQL Improved (MySQL Mejorado)**, que anomenarem **moodle**. Recorda que l'usuari de la base de dades és **root** (amb contrasenya **root**).

Al finalitzar la instal·lació hauràs de crear una compta d'usuari per l'administrador (que seràs tu mateix). El nom d'aquest usuari serà **admin**, amb la contrasenya **Administrador_1**. A part del nom d'usuari i la contrasenya, també s'ha d'indicar l'email, la població i el país.

## 2. Idioma predefinit

Aconsegueix que l'idioma predefinit del Moodle sigui el **català**.

## 3. Configuració de la primera pàgina del lloc

- Nom complet: **Escola d'Ensenyament Secundari Júlia**
- Nom curt: **Escola Júlia**
- Afegeix una descripció detallada dels valors i el compromís d'aquesta escola (copia aquesta informació de la web d'alguna altra escola).

A la primera pàgina del lloc no es mostrarà res fins que l'usuari no hagi entrat. Un cop hagi entrat, es mostrarà:

- la llista de categories de cursos  
- la caixa de text per buscar cursos

## 4. Aparença del Moodle

- Afegeix i aplica un **nou tema** (diferent dels que incorpora per defecte).
- Modifica el **favicon** per un personalitzat.
- Si el tema ho permet, mostra el **logo** de l'escola.

---

# Part 2: Crear comptes d’usuari definint els privilegis d’accés sobre els recursos d’un sistema de gestió d’aprenentatge a distància

El nostre lloc web ja està totalment configurat i llest per ser utilitzar. El que ara necessitem és crear les comptes d'usuari dels professors i assignar-los als cursos que hauran de gestionar.

## 1. Categories de cursos

Afegeix 4 noves categories:

- 1er ESO  
- 2on ESO  
- 3er ESO  
- 4rt ESO  

## 2. Comptes d’usuari dels professors

Els professors són:

- Pedro Ruiz Gomez  
- Benito Wolff Ruiz  
- Angel Lobo Mateo  
- Claudia Blazquez Tomas  
- Vicente Puñal Pineda  

La configuració d’aquestes comptes es mostra a l’[arxiu adjunt número 1.](https://drive.google.com/file/d/1knqUOnsEa3VWLk51jIVAF-vIZ3vEPJvm/view?usp=sharing)

## 3. Assignació de rols

Assigna a **Pedro Ruiz Gomez** el rol de **creador de cursos**.

## 4. Modificació del rol de creador de cursos

Modifica el rol perquè tingui permís per gestionar les categories de cursos.

Ruta:  
**Administració del lloc > Usuaris > Definició de rols > Creador de cursos > Editar**

**IMPORTANT:** Accedeix com si fossis **Pedro Ruiz Gomez** i segueix les indicacions següents.

## 5. Crear el curs *Matemàtiques 1*

Categoria: **1er ESO**  
Nom curt: **MAT_1ESO**

Característiques:

- Data d'inici: **12 de setembre de 2025**
- Curs visible
- Resum del curs: [arxiu adjunt número 2](https://drive.google.com/file/d/11Y7WW7zuAFoOFEzsdbEpo1sShYsb_4-8/view?usp=sharing) (donar format)
- Format: **5 temes**, **1 per pàgina**
- Temes ocults: **no visibles**
- Idioma: **català**
- Fins a **5 notícies**
- Qualificacions i informes visibles
- Mida màxima fitxers: **2 MB**
- Sense treball en grups
- Rol de professor: **Senyor Ruiz**

## 6. Crear el curs *Taulell d'anuncis 1*

Categoria: **1er ESO**  
Nom curt: **TAU_1ESO**

Característiques:

- Data d'inici: **12 de setembre de 2025**
- Curs visible
- Resum: *Taulell d'anuncis de 1er de la ESO*
- Format: **social**
- Idioma: **català**
- No notícies, no qualificacions, no informes
- Fitxers màxim 2 MB
- Sense grups

## 7. Crear el curs *Informàtica 1*

Categoria: **1er ESO**  
Nom curt: **INF_1ESO**

Característiques:

- Data d'inici: **12 de setembre de 2025**
- Curs visible
- Resum: [arxiu adjunt número 3](https://drive.google.com/file/d/1EiezMWOKSC37mD2sxKBdraJ_mGhM7YGK/view?usp=sharing) (donar format)
- Format: **12 setmanes**, tot en una pàgina
- Temes ocults: **visibles**
- Idioma: **català**
- Fins a **5 notícies**
- Qualificacions i informes visibles
- Fitxers màxim 2 MB
- **Treball en grups**  
  - Els alumnes només veuen els del seu grup  
  - Obligatori a totes les activitats
- Rol professor: **Senyor Ruiz**
- Rol professor no-editor: **Senyoreta Blazquez**

## 8. Ordenar cursos

El curs **Taulell d'anuncis 1** ha d’aparèixer **a dalt de tot**.

## 9. Assignació de professors als cursos

- Pedro Ruiz Gomez → **Matemàtiques 1** i **Informàtica 1** (rol professor)
- Claudia Blazquez Tomas → **Informàtica 1** (rol professor no-editor)

Accedeix com a Claudia i comprova les limitacions del rol.

## 10. Automatriculació i accés de visitants

- Automatriculació:
  - Matemàtiques 1 → contrasenya **mates1**
  - Informàtica 1 → contrasenya **info1**
- Accés visitants:
  - Taulell d'anuncis 1 → contrasenya **guest**

## 11. Activar autenticació basada en correu electrònic

Ruta:  
**Configuracions > Administració del lloc > Connectors > Autenticació > Gestió de l'autenticació**

A *Paràmetres comuns*:  
**Autoregistre → activar Autenticació basada en el correu electrònic**

## 12. Registrar un nou alumne

Registra’t com alumne i automatricula’t.

Com que el servidor no té correu, cal confirmar manualment el registre des del compte administrador.

---

# Part 3: Manipular el sistema afegint continguts i configurant components

Accedeix com **Pedro Ruiz Gomez** al curs **Matemàtiques 1**.

## 1. Afegir títols i resums als 5 temes

Temes:

- Nombres  
- Equacions de primer grau  
- Equacions de segon grau  
- Polinomis  
- Trigonometria  

Afegeix resum i format adequat.

## 2. Afegir etiqueta superior amb imatge

A la secció inicial:

- Afegeix una etiqueta amb:
  - Nom del curs
  - Imatge relacionada amb matemàtiques (dimensions reduïdes)
- Dona format integrat amb el tema

## 3. Afegir fòrum

Nom: **Fòrum de Matemàtiques 1**  
Text: *Si tens dubtes amb l'assignatura, pregunta al fòrum.*  
Format integrat  
Tipus: **estàndard (com blog)**  
Subscripció: **automàtica**

## 4. Afegir glossari

Nom: **Glossari de Matemàtiques 1**  
Text: *Glossari de terminologia matemàtica*  
Format integrat  
Visualització: **enciclopèdia**, 5 entrades per pàgina

Entrades:

- Nombres Enters  
- Teorema de Pitàgores  
- Regla de Ruffini  

Inclou una imatge en almenys una entrada.

## 5. Afegir xat

Nom: **El xat del professor**  
Text: *Xateja amb el teu professor*  
Format integrat

Configuració:

- Proper dissabte a les 10:00  
- Sessions setmanals  
- Comprovar funcionament com professor i participant

## 6. Afegir enquesta

Tipus: **COLLES (preferit)**  
Nom: **Enquesta de satisfacció**

Comprovar funcionament com participant.

## 7. Afegir enllaç URL

URL: http://www.xtec.cat/web/recursos/matematiques  
Nom: **XTEC - Matemàtiques**  
Descripció: no visible  
Obertura: **finestra emergent**

## 8. Afegir pàgina

Nom: **Criteris d'avaluació de Matemàtiques 1**  
Text d’introducció: *Criteris d'avaluació*  
Visible a la pàgina principal

Contingut: taula amb:

| Tema                         | Pes |
|------------------------------|-----|
| Nombres                      | 10% |
| Equacions de primer grau     | 20% |
| Equacions de segon grau      | 25% |
| Polinomis                    | 15% |
| Trigonometria                | 30% |

Format integrat amb el tema.

## 9. Reordenar elements

Ordre final:

1. Etiqueta  
2. Enllaç  
3. Pàgina  
4. Fòrum  
5. Xat  
6. Glossari  
7. Enquesta  

---

# Part 4: Afegir més continguts i activitats

## 1. Dividir el tema *Nombres* en 3 etiquetes

Etiquetes:

- Apunts  
- Exercicis pràctics  
- Exercicis d'avaluació  

Cada etiqueta ha d’incloure una imatge (petita) i format integrat.

## 2. Afegir consulta

Nom: **Exercici pràctic 1**  
Descripció: *Quin és el resultat d'aquesta operació: 10 : 2 + 5 · 3 + 4 - 5 · 2 - 8 + 4 · 2 - 20 : 4?*  
Format integrat

Respostes (vertical):

- 5  
- 9  
- 18  

Sense canviar resposta, sense límit, resultats anònims.

## 3. Afegir lliçó

Nom: **Els nombres racionals**

Configuració:

- Barra de progrés  
- Puntuació acumulada  
- Menú esquerra (després del 75%)  
- Format diapositives  
- Màxim 2 respostes per pàgina  
- 1 intent per pregunta  
- Revisió sempre disponible  
- Qualificació sobre 10  
- Es pot repetir, conserva millor nota  

Contingut:

- 4 pàgines de contingut  
- 4 preguntes V/F  
- Punts: 2, 2, 3, 3

[Enllaç](http://www.vitutor.com/di/r/fracciones.html)

Format integrat.

## 4. Afegir qüestionari

Nom: **Exercici d'avaluació 1**

Configuració:

- Disponible: **25 de febrer, 9–10 h**
- Temps màxim: **20 min**
- 1 intent
- 1 pregunta per pàgina
- Preguntes i respostes barrejades
- Feedback immediat
- Segona oportunitat amb penalització
- Revisió completa un cop tancat
- Retroacció global:
  - 100% → *Perfecte!*
  - 45% → *Ui! Casi*

Afegir 5 preguntes (tema: nombres racionals), 2 punts cadascuna, penalització 25%. [Enllaç](http://www.vitutor.com/di/r/fracciones.html)

## 5. Afegir tasca (text en línia)

Nom: **Exercici pràctic 2**  
Descripció: *Què són els nombres primers?*  
Format integrat  
Nota sobre 10  
Es pot repetir

## 6. Afegir tasca (penjar fitxer)

Nom: **Exercici d'avaluació 2**  
Descripció: *Elabora un resum d'aquest tema.*  
Format integrat  
Data límit: **25 de febrer, 10 h**  
Nota sobre 10  
Enviaments il·limitats

---

# Part 5: Afegir i configurar nous components i plugins

Accedeix com **Pedro Ruiz Gomez**, però **cal fer-ho com administrador**.

## 1. Afegir blocs

Blocs:

- Calendario  
- Eventos próximos  
- Usuarios en línea  
- Mis cursos  
- Comentarios  
- Entrada aleatoria del glosario (glossari activitat 3)  
- Canal RSS remoto (RSS El Periódico i La Vanguardia)  
- Text (amb 3 enllaços):
  - http://www.xtec.cat  
  - http://educalab.es/recursos  
  - http://www.vitutor.com  

Visibilitat:

- **Calendario** i **Eventos próximos** → visibles a totes les pàgines  
- Resta → només pàgina principal del curs  

## 2. Afegir gadgets (blocs Text)

- Rellotge en javascript  
- Gadget web lliure  

## 3. Crear insígnies

Crear 3 insígnies amb [Canva](https://www.canva.com/es_es/):

- Activitat 1  
- Activitat 2  
- Activitat 3  

Configurar:

- Activar seguiment de compleció  
- Assignar condicions per guanyar insígnia  

## 4. Còpia de seguretat

- Crear backup del curs **Matemàtiques 1**
- Restaurar-lo com a **Matemàtiques 1 backup**  
  - Nom curt: **MAT_BCKP**

[Anar a la pàgina inicial](../README.md)
