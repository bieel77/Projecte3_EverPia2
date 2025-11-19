# 🌐 P04: Documentació del servidor DNS

Com a membres de l'equip de sistemes d'EverPia, el vostre repte és configurar un servidor DNS com a prova de concepte per al client Digicore. Actualment, la configuració està implementada en una màquina virtual, però l'objectiu és publicar aquesta configuració a GitHub per tal de facilitar la seva replicació en futurs entorns.

## 🎯 Objectiu

Permetre que la configuració es pugui replicar fàcilment sense començar des de zero: només caldrà descarregar els fitxers al servidor Linux desitjat i reiniciar el servei perquè el servidor estigui completament operatiu.

## 🧩 Fase 1: Preparació de la connectivitat i còpia dels fitxers

### ⚙️ Pas 1.1: Configuració de la interfície Host-Only

Afegiu una segona interfície de xarxa a la vostra màquina virtual Ubuntu Server i configureu-la en mode **Host-Only**.  
Assegureu-vos que la interfície estigui activa i que tingueu connectivitat amb la màquina física (host).

### 🔐 Pas 1.2: Còpia segura dels fitxers amb SCP

Un cop establerta la connexió **Host-Only**, utilitzarem **SCP** (Secure Copy Protocol), que ve inclòs en el servei SSH, per transferir els fitxers de configuració a la màquina física.

#### 📂 Fitxers a copiar:
- `/etc/bind/named.conf.options`
- `/etc/bind/named.conf.local` (verifiqueu que no hi hagi errors tipogràfics, com "cof" en lloc de "conf")
- Arxius de zones dins la carpeta `/etc/bind/zones`

#### 💻 Exemple de comanda SCP:

```bash
scp usuari@IP_VM:/etc/bind/named.conf.options .

