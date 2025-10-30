# T06: Fonaments del servei DNS

## Context

Com a membres cada cop més integrats de l'equip tècnic de la consultora **EverPia**, teniu davant un nou repte.  
El vostre client, una empresa de màrqueting digital (**DigiCore**), experimenta de tant en tant errors de connectivitat a certes aplicacions.  
El seu equip tècnic creu que la causa principal podria ser una **resolució de noms (DNS) incorrecta o lenta**.

Se us ha encarregat **realitzar una auditoria teòrica i pràctica del servei DNS** per tal de formar el personal del client i oferir eines de diagnosi ràpides.

![imagen](img/fto2.png)


---

## Fase Teòrica: Sessió Formativa

Com a part d’aquesta formació, caldrà que elaboreu un **material formatiu** pel personal del client.  
Per assegurar la màxima qualitat en els continguts, els vostres directors tècnics han preparat unes sessions prèvies per tal que tingueu un domini dels conceptes que després haureu d’explicar.

### Conceptes a treballar

- **Jerarquia i Estructura:**  
  Explicació de l'estructura en arbre del DNS (Root > TLDs > Segon Nivell).

- **Procés de Resolució:**  
  Com es realitza una consulta iterativa i una recursiva.  
  Què és un servidor d'arrel (*Root Server*) i un servidor autoritatiu.

- **Tipus de zones:**  
  Directa i inversa. Zona primària i zona secundària.

- **Tipus de Registres Clau (Records):**  
  Descripció de la funció dels registres `A`, `CNAME`, `MX`, `NS` i `SRV`.

### Conceptes essencials

- **Resposta Autoritativa:** Què significa i com es pot identificar.  
- **Time To Live (TTL):** La seva funció i impacte en la propagació i el rendiment.  
- **Start of Authority (SOA):** Quina informació essencial conté i per què és crítica.  
- **Reenviadors:** Condicionals i incondicionals.  
- **Resolució local:** Mecanismes de resolució sense servidor entre equips clients. El protocol **mDNS**.

### Activitat de la fase teòrica

Un cop domineu aquests conceptes, caldrà que prepareu la vostra **píndola formativa**, que consistirà en un **vídeo d’entre 10 i 15 minuts**.  
Aquest haurà d’explicar de forma breu però clara tots els conceptes anteriors.

---

## Fase Pràctica: Diagnosi de Noms (Auditoria amb CLI)

Heu de demostrar l'ús de les principals **utilitats de diagnosi DNS** en els diferents sistemes operatius que utilitza el client (**Linux/macOS i Windows**).  
Per a cada eina, executeu les comandes indicades a continuació contra el domini que s’indiqui explícitament i **captureu/analitzeu els resultats**.

Per fer aquesta demostració, caldrà usar un **equip Zorin amb dues interfícies**:
- La primera en **NAT**.
- La segona en **adaptador pont**, amb la IP configurada correctament segons les indicacions dels vostres responsables.

---

### A. Diagnosi Avançada amb `dig` (Linux / macOS)

#### Comanda 1: Consulta Bàsica de Registre A
```bash
dig xtec.cat A

