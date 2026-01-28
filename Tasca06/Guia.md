# CONFIGURACIÓ DEL DOMINI

| Introducció |
|----------------------------------------|

Un cop tenim ja el nostre domini creat, el següent pas, és desplegar el domini, és a dir, crear els diferents objectes que el formaran: grups, usuaris, màquines. Aquí veurem la utilitat d’organitzar els objectes amb unitats organitzatives (OU).

| Procediment pràctic |
|----------------------------------------|

- Crear la següent estructura d’unitats organitzatives: 
- Definir la següent estructura de grups:

-gestio

-magatzem

-gerencia

-personal (tots els grups anteriors han de ser membres d’aquest grup)



- Crear una plantilla d’usuari per cadascun dels grups:

-Gestio

-Magatzem

-Gerencia

Cada plantilla ha de tenir definida la pertinença al grup i la creació de la carpeta personal.



- Definir un usuari de prova per cadascuna de les plantilles.



- Aprovisionar un equip que anomenarem PC1 dins la OU equips.



- Crear una VM amb Windows 11 amb 4 GB de RAM i disc suficient. La xarxa estarà en xarxa NAT. Un cop creat l’equip, agregeu-lo al domini.



- Comprovar el correcte funcionament, iniciant sessió a l’equip client amb els tres usuaris de prova.





[Anar a l'enunciat](../Tasca06/README.md)  
[Anar a la pàgina inicial](../README.md)
