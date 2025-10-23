**T01: Gestor de contrasenyes**

Alerta\!\! EverPia ha estat atacada per ciberdelinqüents. La consultora on esteu de becaris ha patit una fuita d’informació (data breach) i informació confidencial sobre un projecte que està en fase de desenvolupament està ara en mans de delinqüents que amenacen amb publicar-la si no es paga un rescat.

Òbviament, això ha causat una gran alarma dins la companyia i s’ha creat un comitè de crisi per gestionar la situació. 

La investigació interna ha revelat que un dels comptes tècnics va ser compromès a causa de l'ús d'una contrasenya feble o reutilitzada.

![imagen](img/image1.png)

Com a resposta a aquesta crisi, la Direcció Tècnica ha emès una directriu: tot el personal tècnic ha de començar a utilitzar un gestor de contrasenyes validat per garantir l'ús de credencials úniques i robustes. Se us encarrega la tasca d'avaluar les opcions i crear la documentació necessària per a la formació del personal.

**Fase 1: Anàlisi i Justificació (Document d'Informe)**

Les contrasenyes febles o repetides representen un risc crític per a l’empresa, ja que poden ser explotades mitjançant:

* **Atacs de diccionari**, on es proven combinacions habituals de paraules o contrasenyes comunes.

* **Credential stuffing**, que consisteix a provar credencials robades en altres serveis on els usuaris poden haver reutilitzat la mateixa contrasenya.

* **Enginyeria social o phishing**, que busca enganyar els usuaris perquè revelin la seva informació d’accés.

Els efectes d’un atac d’aquest tipus poden ser molt greus, incloent-hi accés no autoritzat a dades, pèrdua d’informació confidencial i afectació de la reputació de l’empresa.

Un gestor de contrasenyes és una eina que permet:

* Generar contrasenyes úniques i robustes per a cada servei.  
    
* Emmagatzemar-les de forma xifrada i segura, accessible només amb una contrasenya mestra.  
    
* Facilitar l’autocompletat de contrasenyes i, en alguns casos, la sincronització entre dispositius.

Per tot això, la Direcció Tècnica ha decidit implantar un gestor de contrasenyes corporatiu. L’objectiu és millorar la seguretat, centralitzar la gestió de credencials i reduir el risc de futurs incidents relacionats amb contrasenyes febles o reutilitzades.

**2\. Comparativa tècnica**

A continuació es compara **Bitwarden (solució online/núvol)** amb **KeePassXC (solució offline/escriptori)** segons diversos criteris:

| Característica | Bitwarden (Online / Núvol) | KeePassXC (Offline / Escriptori) |
| :---- | :---- | :---- |
| Tipus | Núvol, sincronització automàtica entre dispositius | Local, arxiu `.kdbx` que es pot portar en USB o emmagatzemar localment |
| Xifratge i seguretat | Xifratge end-to-end AES-256; les dades només es desen xifrades al núvol | Xifratge AES-256 local; només l’usuari pot accedir a la base de dades |
| Accés multiplataforma | Web, Windows, macOS, Linux, Android, iOS | Windows, macOS, Linux; portabilitat via arxiu `.kdbx` |
| Sincronització | Automàtica via núvol | Manual: cal copiar el fitxer `.kdbx` entre dispositius |
| Cost / model freemium | Freemium: funcionalitat bàsica gratuïta, opcions premium opcionals | Totalment gratuït, codi obert |
| Open Source | Sí | Sí |
| Facilitat d’ús | Molt amigable, integració amb navegadors, fàcil configuració | Requereix més coneixement tècnic, menys integració automàtica amb navegadors |

**3\. Avantatges i inconvenients**

**Bitwarden (núvol / online)**

**Avantatges**: sincronització automàtica, fàcil d’utilitzar, còpies de seguretat al núvol, integració amb navegadors i mòbils.

**Inconvenients**: depèn del proveïdor de núvol, possible risc si el servei online és compromès.

**KeePassXC (offline / escriptori)**

* **Avantatges**: control total de les dades, sense dependència del núvol, codi obert, molt segur si es gestiona correctament.

* **Inconvenients**: sincronització manual, menys còmode per a equips distribuïts, requereix coneixements tècnics.

**4\. Recomanació**

Després de l’anàlisi, recomanem Bitwarden per al personal tècnic de l’empresa, per les següents raons:

1. Permet **sincronitzar automàticament** les credencials entre diversos dispositius, la qual cosa facilita el treball de l’equip tècnic.  
     
2. La **facilitat d’ús** i la integració amb navegadors i aplicacions fa que sigui més probable que els usuaris adoptin l’eina correctament.  
     
3. Ofereix **xifratge end-to-end** i opcions de còpia de seguretat automàtica, assegurant un equilibri entre seguretat i comoditat.  

