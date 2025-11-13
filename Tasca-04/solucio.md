# **T04: Serveis de directori. LDAP (Guia)**

![imagen](img/imagen1.png)

Al obrir els paràmetres de la màquina assegurat que l’adaptador de xarxa estigui en NAT, just després de fer això obre la màquina.

![imagen](img/imagen2.png)  
Per canviar el nom del servidor escrivim **sudo nano /etc/hosts** i premem ENTER.

![imagen](img/imagen3.png)

Després aquí on el nom d’usuari (en el meu cas és *server*) l’has de canviar per **server.innovatechXX.test** 

![imagen](img/imagen4.png)

En l’adaptador 2, posem només anfitrió.

![imagen](img/imagen5.png)

![imagen](img/imagen6.png)

![imagen](img/imagen7.png)

![imagen](img/imagen8.png)

Escrivim `ip a` per veure les IPs.

---

## **Instal·lació del servei OpenLDAP** apt install slapd ldap-utils -y

![imagen](img/imagen9.png)

Per fer la instal·lació del OpenLDAP, escrivim:
apt install slapd ldap-utils -y

![imagen](img/imagen10.png)

I després aquí fiquem la contrasenya d’usuari.

![imagen](img/imagen11.png)

I comprovem que està funcionant.

![imagen](img/imagen12.png)

I comprovem també que el directori s’ha creat amb el nom que hem canviat abans (**innovatechXX**).

![imagen](img/imagen13.png)

Fiquem aquesta comanda si volem fer la reconfiguració (es fa només si vols canviar el nom del directori).

![imagen](img/imagen14.png)

Premem a que “No”.

![imagen](img/imagen15.png)

Li donem a “Ok”.

![imagen](img/imagen16.png)

Premem també “Ok” aquí.

![imagen](img/imagen17.png)

I en la contrasenya fiquem **p@ssw0rd** i posteriorment premem “Ok”.

![imagen](img/imagen18.png)

Premem a “Yes”.

![imagen](img/imagen19.png)

I per últim aquí premem a “Yes” també.

![imagen](img/imagen20.png)

I després introduïm `sudo slapcat` (s’ha d’escriure en root) per comprovar que la modificació ha estat ben feta.

---

## **Creació d’Unitats Organitzatives (OU)**

![imagen](img/imagen21.png)

Primer de tot creem la carpeta.

![imagen](img/imagen22.png)

Escrivim aquesta comanda per crear les OU **usuaris** i **grups**.

![imagen](img/imagen23.png)

![imagen](img/imagen24.png)

Introduïm aquesta comanda per afegir l’arxiu en el directori.

![imagen](img/imagen25.png)

I per últim introduïm la següent comanda per veure totes les OU creades en el directori.

---

### **3.2. Gestió i Administració (LAM)**

![imagen](img/imagen26.png)

Escrivim això per instal·lar el **LDAP Account Manager**.

![imagen](img/imagen27.png)

![imagen](img/imagen28.png)

Escrivim la IP de **host-only** amb `/lam` al cercador. Un cop dintre de la web, ens ubiquem a dalt a la dreta on posa “LAM configuration”.

![imagen](img/imagen29.png)

Després fem clic a **“Edit server profiles”**.

![imagen](img/imagen30.png)

Introduïm la contrasenya **lam** i premem “Ok”.

![imagen](img/imagen31.png)

Un cop dintre, anem a **“General settings”** i configurem l’admin, l’idioma i el compte.

![imagen](img/imagen32.png)

![imagen](img/imagen33.png)

Després anem a **“Tipos de cuentas”**, introduïm els **usuaris** i **grups**, i premem **“Guardar”**.

![imagen](img/imagen34.png)

Després, un cop iniciem sessió, se’ns obrirà això: premem a **“Cuentas”**.

![imagen](img/imagen35.png)

Després anem a **“Grupos”**.

![imagen](img/imagen36.png)

I per últim, premem a **“Nuevo Grupo”**.

![imagen](img/imagen37.png)

Creem el primer grup **tech**.

![imagen](img/imagen38.png)

I el segon **“manager”**.

![imagen](img/imagen39.png)

Ara creem els usuaris pels grups **tech01** i **manager01**. De moment, creem el de **tech**.

![imagen](img/imagen40.png)

![imagen](img/imagen41.png)

I ara el de **manager**.

![imagen](img/imagen42.png)

I ja estan els **usuaris** i els **grups** creats.

---

### **4. Integració de Client (Client Ubuntu Desktop)**

Per començar la part 4, hem de crear una altra màquina virtual amb la ISO de **Zorin** per tenir interfície gràfica.

![imagen](img/imagen43.png)

![imagen](img/imagen44.png)

Un cop creada, anem a **“Paràmetres”**, i configurem els adaptadors de xarxa: la primera en **NAT** i la segona en **“Adaptador de només l’amfitrió”**.

![imagen](img/imagen45.png)

Per últim, creem la instantània: anem a les tres ratlles de la màquina, posteriorment a **“Fes”**, li fiquem un nom i a **“D’acord”**, obrim la màquina i configurem la instal·lació.

![imagen](img/imagen46.png)

Primer de tot, fem `ip a` per veure la IP.

![imagen](img/imagen47.png)

Després fiquem la següent comanda per començar les actualitzacions.

![imagen](img/imagen48.png)

Escrivim aquesta comanda per entrar a `/etc/hosts`.

![imagen](img/imagen49.png)

Un cop aquí, fiquem la següent informació, de IP i **innovatechXX.test**, i guardem.

![imagen](img/imagen50.png)

Després fiquem la següent comanda per modificar el **hostname**.

![imagen](img/imagen51.png)

I introduïm el següent, i guardem.

![imagen](img/imagen52.png)

I escrivim aquesta comanda per fer la comprovació.

![imagen](img/imagen53.png)

![imagen](img/imagen54.png)

Ara fiquem la següent comanda per instal·lar els mòduls per l'autenticació de LDAP.

![imagen](img/imagen55.png)

Posteriorment fiquem el domini de **innovatech** i continuem.

![imagen](img/imagen56.png)

Ara introduïm el **nom distingit de la base de cerca** i acceptem.
![imagen](img/imagen57.png)

Seleccionem **“3”**.

![imagen](img/imagen58.png)

Premem a **“Si”**.

![imagen](img/imagen59.png)

Ara premem a **“No”**.

![imagen](img/imagen60.png)

Ara posem el compte de **LDAP**.

![imagen](img/imagen61.png)

I per últim, introduïm la contrasenya.

![imagen](img/imagen62.png)

I ja tenim la instal·lació feta.

![imagen](img/imagen63.png)

Després, amb la següent comanda, comprovem la connectivitat des de la mateixa màquina.

![imagen](img/imagen64.png)

Ara, amb aquesta comanda, modificarem l’arxiu **nsswitch.conf**, perquè LDAP sigui utilitzat per usuaris i grups.

![imagen](img/imagen65.png)

![imagen](img/imagen66.png)

I ara canviem aquesta configuració.

![imagen](img/imagen67.png)

I ara, amb aquesta comanda, anirem a l’arxiu **pam.d/common-password**.

![imagen](img/imagen68.png)

Un cop aquí, busquem `use_authtok` i ho borrem; ha de quedar així:  

![imagen](img/imagen69.png)

![imagen](img/imagen70.png)

Després, amb la següent comanda, entrem a l’arxiu **pam.d/common-session**.

![imagen](img/imagen71.png)

I un cop aquí, ens ubiquem a la part de baix de tot i afegim el següent **session optional**:  

![imagen](img/imagen72.png)

I guardem.

![imagen](img/imagen73.png)

Ara introduïm la següent comanda per **reiniciar**.

![imagen](img/imagen74.png)

I fiquem la contrasenya.

![imagen](img/imagen75.png)

Amb la següent comanda, mirem que els **usuaris estiguin visibles**.

![imagen](img/imagen76.png)

Després, amb aquesta comanda, entrem a l’arxiu **pam.d/gdm-launch-environment**.

![imagen](img/imagen77.png)

I introduïm la següent informació:  

![imagen](img/imagen78.png)

I per últim apliquem una contrasenya a cada usuari i iniciem sessió desde la màquina client.


