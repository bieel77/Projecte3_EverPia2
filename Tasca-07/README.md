# T07: Instal·lant un servidor de noms

Després de l’exitosa experiència a nivell de formació, els nostres clients de **Digicore** estan tan satisfets amb la nostra feina que ens encarreguen la implantació des de zero dels seus serveis de **DNS interns**.

Actualment, l'agència fa servir **adreces IP** per accedir als seus servidors de desenvolupament, bases de dades i eines de gestió interna. Aquest mètode és ineficient i propens a errors:

- **Usabilitat deficient:** Els empleats han de memoritzar o buscar constantment adreces IP complexes (p. ex., `192.168.10.25`).
- **Manteniment feixuc:** Si un servidor canvia la seva IP, cal notificar i actualitzar manualment la configuració a tots els equips i aplicacions que s'hi connecten.
- **Manca de professionalitat:** En un entorn professional, tots els serveis haurien de ser accessibles mitjançant noms fàcils de recordar.

Per tant, la nostra missió és implementar un **Sistema de Noms de Domini (DNS)** intern robust.  
L'objectiu és que els servidors i aplicacions de l'agència es puguin accedir utilitzant **noms de domini amigables** (p. ex., `bbdd.digicore.lan` o `wiki.digicore.lan`).

![imagen](img/ftto2.png)

---

## El vostre repte

La recomanació com a consultora és utilitzar **BIND9**, l'estàndard de facto de servidor de noms a Linux, per la seva fiabilitat i flexibilitat.

La vostra missió serà **instal·lar i configurar un servidor DNS primari (màster)** amb BIND9 en un sistema Linux.  
Haureu de crear una **Zona Directa (Forward Zone)** i una **Zona Inversa (Reverse Zone)** per al domini privat de DigiCore, garantint que tant els noms es resolguin a IPs com les IPs es resolguin a noms.

Per fer una prova de concepte, usareu el domini `digicore-XX.test`, on **XX** serà el vostre número de llista.

---

### Pas previ

Configurar un **Ubuntu Server** amb **4 GB de RAM** i **20 GB de disc**.  
Aquesta màquina virtual haurà de tenir:
- Una interfície en **adaptador pont** (la configuració que s’indicarà a l’inici del repte)
- Una segona en **host-only**

Un cop configurat:
1. Caldrà instal·lar el paquet `bind9`.
2. Instal·leu el servei `ssh` al servidor, perquè després caldrà **exportar els arxius de configuració al vostre repositori de GitHub**.

---

## Accions a realitzar

1. **Configurar** l’arxiu `named.conf.options` perquè accepti consultes recursives de la seva xarxa local.  
   - Haurà d’usar com a reenviador la IP `8.8.8.8`.
   - Mostra la captura.  
   - Un cop fet, reinicia el servei i comprova que funciona (mostra l’estat).

2. **Utilitzar un client** (pot ser la màquina Zorin usada anteriorment).  
   - Canvia l’adaptador a **adaptador pont**.  
   - Configura que el **servidor de noms (DNS)** sigui la IP del vostre servidor.  
   - Comprova que el client té resolució a Internet (obrint una pàgina al navegador o fent un `dig google.com`).

3. **Editar** l’arxiu `named.conf.local` per definir dues zones:
   - Zona directa del domini `digicore-XX.test`
   - Zona inversa de la xarxa local (adreça de xarxa utilitzada a la prova de concepte)

4. **Crear l’arxiu corresponent a la zona directa**
   - Dins una carpeta anomenada `zones` a `/etc/bind` (cal crear-la prèviament).
   - Per comoditat, es pot crear copiant l’arxiu `db.local`.

   **Configura aquest arxiu amb els següents registres:**
   - **SOA** (amb les dades correctament configurades)
   - **NS** que sigui el vostre servidor
   - Un registre **A** anomenat `server` amb la IP del servidor
   - Un registre **A** anomenat `dbserver` amb la IP del client
   - Un registre àlies (**CNAME**) amb nom `data` que apunti a `dbserver`

5. **Crear l’arxiu corresponent a la zona inversa**
   - També dins la carpeta `zones` (podeu copiar `db.127` com a base).

   **Configura aquest arxiu:**
   - **SOA** i **NS** adients
   - **Registres PTR** corresponents al `server` i al `dbserver`

6. **Reiniciar** el servei i fer les comprovacions des del client fent consultes directes i inverses.

7. **Editar** `named.conf.local` per permetre la **transferència de la zona directa** als companys de l’equip.

8. **Configurar una zona secundària** del domini d’un dels companys.  
   - Força la transferència i comprova el funcionament des del client.

---

## Activitat d’avaluació del repte

Per demostrar que sou uns tècnics competents haureu de passar una **avaluació pràctica** al final del repte.  
Durant aquesta avaluació només podreu usar com a material de suport **un full manuscrit amb les vostres anotacions**, que lliurareu en finalitzar la prova.

