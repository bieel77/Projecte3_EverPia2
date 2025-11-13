# **T04: Serveis de directori. LDAP (Guia)**

![imagen](img/imagenn1.png)

Al obrir els paràmetres de la màquina assegurat que l’adaptador de xarxa estigui en NAT, just després de fer això obre la màquina.

![imagen](img/imagenn2.png)  
Per canviar el nom del servidor escrivim **sudo nano /etc/hosts** i premem ENTER.

![imagen](img/imagenn3.png)

Després aquí on el nom d’usuari (en el meu cas és *server*) l’has de canviar per **server.innovatechXX.test** 

![imagen](img/imagenn4.png)

En l’adaptador 2, posem només anfitrió.

![imagen](img/imagenn5.png)

![imagen](img/imagenn6.png)

![imagen](img/imagenn7.png)

![imagen](img/imagenn8.png)

Escrivim `ip a` per veure les IPs.

---

## **Instal·lació del servei OpenLDAP** apt install slapd ldap-utils -y

![imagen](img/imagenn9.png)

Per fer la instal·lació del OpenLDAP, escrivim:
apt install slapd ldap-utils -y

![imagen](img/imagenn10.png)

I després aquí fiquem la contrasenya d’usuari.

![imagen](img/imagenn11.png)

I comprovem que està funcionant.

![imagen](img/imagenn12.png)

I comprovem també que el directori s’ha creat amb el nom que hem canviat abans (**innovatechXX**).

![imagen](img/imagenn13.png)

Fiquem aquesta comanda si volem fer la reconfiguració (es fa només si vols canviar el nom del directori).

![imagen](img/imagenn14.png)

Premem a que “No”.

![imagen](img/imagenn15.png)

Li donem a “Ok”.

![imagen](img/imagenn16.png)

Premem també “Ok” aquí.

![imagen](img/imagenn17.png)

I en la contrasenya fiquem **p@ssw0rd** i posteriorment premem “Ok”.

![imagen](img/imagenn18.png)

Premem a “Yes”.

![imagen](img/imagenn19.png)

I per últim aquí premem a “Yes” també.

![imagen](img/imagenn20.png)

I després introduïm `sudo slapcat` (s’ha d’escriure en root) per comprovar que la modificació ha estat ben feta.

---

## **Creació d’Unitats Organitzatives (OU)**

![imagen](img/imagenn21.png)

Primer de tot creem la carpeta.

![imagen](img/imagenn22.png)

Escrivim aquesta comanda per crear les OU **usuaris** i **grups**.

![imagen](img/imagenn23.png)

![imagen](img/imagenn24.png)

Introduïm aquesta comanda per afegir l’arxiu en el directori.

![imagen](img/imagenn25.png)

I per últim introduïm la següent comanda per veure totes les OU creades en el directori.

---

### **3.2. Gestió i Administració (LAM)**

![imagen](img/imagenn26.png)

Escrivim això per instal·lar el **LDAP Account Manager**.

![imagen](img/imagenn27.png)

![imagen](img/imagenn28.png)

Escrivim la IP de **host-only** amb `/lam` al cercador. Un cop dintre de la web, ens ubiquem a dalt a la dreta on posa “LAM configuration”.

![imagen](img/imagenn29.png)

Després fem clic a **“Edit server profiles”**.

![imagen](img/imagenn30.png)

Introduïm la contrasenya **lam** i premem “Ok”.

![imagen](img/imagenn31.png)

Un cop dintre, anem a **“General settings”** i configurem l’admin, l’idioma i el compte.

![imagen](img/imagenn32.png)

![imagen](img/imagenn33.png)

Després anem a **“Tipos de cuentas”**, introduïm els **usuaris** i **grups**, i premem **“Guardar”**.

![imagen](img/imagenn34.png)

Després, un cop iniciem sessió, se’ns obrirà això: premem a **“Cuentas”**.

![imagen](img/imagenn35.png)

Després anem a **“Grupos”**.

![imagen](img/imagenn36.png)

I per últim, premem a **“Nuevo Grupo”**.

![imagen](img/imagenn37.png)

Creem el primer grup **tech**.

![imagen](img/imagenn38.png)

I el segon **“manager”**.

![imagen](img/imagenn39.png)

Ara creem els usuaris pels grups **tech01** i **manager01**. De moment, creem el de **tech**.

![imagen](img/imagenn40.png)

![imagen](img/imagenn41.png)

I ara el de **manager**.

![imagen](img/imagenn42.png)

I ja estan els **usuaris** i els **grups** creats.

---

### **4. Integració de Client (Client Ubuntu Desktop)**

Per començar la part 4, hem de crear una altra màquina virtual amb la ISO de **Zorin** per tenir interfície gràfica.

![imagen](img/imagenn43.png)

![imagen](img/imagenn44.png)

Un cop creada, anem a **“Paràmetres”**, i configurem els adaptadors de xarxa: la primera en **NAT** i la segona en **“Adaptador de només l’amfitrió”**.

![imagen](img/imagenn45.png)

Per últim, creem la instantània: anem a les tres ratlles de la màquina, posteriorment a **“Fes”**, li fiquem un nom i a **“D’acord”**, obrim la màquina i configurem la instal·lació.

![imagen](img/imagenn46.png)

Primer de tot, fem `ip a` per veure la IP.

![imagen](img/imagenn47.png)

Després fiquem la següent comanda per començar les actualitzacions.

![imagen](img/imagenn48.png)

Escrivim aquesta comanda per entrar a `/etc/hosts`.

![imagen](img/imagenn49.png)

Un cop aquí, fiquem la següent informació, de IP i **innovatechXX.test**, i guardem.

![imagen](img/imagenn50.png)

Després fiquem la següent comanda per modificar el **hostname**.

![imagen](img/imagenn51.png)

I introduïm el següent, i guardem.

![imagen](img/imagenn52.png)

I escrivim aquesta comanda per fer la comprovació.

![imagen](img/imagenn53.png)

![imagen](img/imagenn54.png)

Ara fiquem la següent comanda per instal·lar els mòduls per l'autenticació de LDAP.

![imagen](img/imagenn55.png)

Posteriorment fiquem el domini de **innovatech** i continuem.

![imagen](img/imagenn56.png)

Ara introduïm el **nom distingit de la base de cerca** i acceptem.
![imagen](img/imagenn57.png)

Seleccionem **“3”**.

![imagen](img/imagenn58.png)

Premem a **“Si”**.

![imagen](img/imagenn59.png)

Ara premem a **“No”**.

![imagen](img/imagenn60.png)

Ara posem el compte de **LDAP**.

![imagen](img/imagenn61.png)

I per últim, introduïm la contrasenya.

![imagen](img/imagenn62.png)

I ja tenim la instal·lació feta.

![imagen](img/imagenn63.png)

Després, amb la següent comanda, comprovem la connectivitat des de la mateixa màquina.

![imagen](img/imagenn64.png)

Ara, amb aquesta comanda, modificarem l’arxiu **nsswitch.conf**, perquè LDAP sigui utilitzat per usuaris i grups.

![imagen](img/imagenn65.png)

![imagen](img/imagenn66.png)

I ara canviem aquesta configuració.

![imagen](img/imagenn67.png)

I ara, amb aquesta comanda, anirem a l’arxiu **pam.d/common-password**.

![imagen](img/imagenn68.png)

Un cop aquí, busquem `use_authtok` i ho borrem; ha de quedar així:  

![imagen](img/imagenn69.png)

![imagen](img/imagenn70.png)

Després, amb la següent comanda, entrem a l’arxiu **pam.d/common-session**.

![imagen](img/imagenn71.png)

I un cop aquí, ens ubiquem a la part de baix de tot i afegim el següent **session optional**:  

![imagen](img/imagenn72.png)

I guardem.

![imagen](img/imagenn73.png)

Ara introduïm la següent comanda per **reiniciar**.

![imagen](img/imagenn74.png)

I fiquem la contrasenya.

![imagen](img/imagenn75.png)

Amb la següent comanda, mirem que els **usuaris estiguin visibles**.

![imagen](img/imagenn76.png)

Després, amb aquesta comanda, entrem a l’arxiu **pam.d/gdm-launch-environment**.

![imagen](img/imagenn77.png)

I introduïm la següent informació:  

![imagen](img/imagenn78.png)

I per últim apliquem una contrasenya a cada usuari i iniciem sessió desde la màquina client.


