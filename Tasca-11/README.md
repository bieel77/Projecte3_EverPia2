# T11: Instal·lació de WordPress en local amb WP Local – Aplicacions Web

En aquesta tasca, cada alumne crearà la seva primera instal·lació de **WordPress en local** utilitzant el programari **WP Local**, que ja està instal·lat als PC de l’aula.

![imagen](img/img1.png)

Aquest WordPress serà el vostre **entorn de proves**, on treballarem durant les classes magistrals per entendre els fonaments de WordPress i preparar-nos per desenvolupar una réplica d’una **web completa** en el següent projecte.

Aquesta web serà per a fer proves i aprendre a fer servir el WordPress, per ara, els continguts no seràn molt importants. Per tant, el text i les imatges seran dummies

Per crear **text dummy**: [https://www.lipsum.com/](https://www.lipsum.com/) per a crear paràgrafs de text sense sentit per omplir.  
Per a crear **imatges dummies**: recomanem visitar la web [https://picsum.photos](https://picsum.photos)   
  - Si vols fotos quadrades, visita la web posant una dimensió en pixels, com per exemple: [https://picsum.photos/200](https://picsum.photos/200)  
  - Si vols fotos amb una dimensió en particular, afegeix les dues dimensions separades per barres com en aquest exemple: [https://picsum.photos/200/300](https://picsum.photos/200/300) 

Els professors us explicarem com fer-ho, la idea és fer una petita classe magistral i després que pogueu crear la vostra pàgina de proves. 

📌 **Recorda: la web de proves creada en aquesta tasca s’utilitzarà en futures explicacions i classes magistrals, per tant és molt important deixar-la configurada i coherent des del principi.**

Objectius de la tasca

Aprendre a utilitzar WP Local per gestionar instal·lacions de WordPress en local.  
Crear i configurar un lloc web de proves individual.  
Practicar amb les funcionalitats bàsiques de WordPress (pàgines, entrades, ajustaments generals).  
Mantenir una instal·lació activa al llarg del curs que servirà com a base de totes les pràctiques.

**Passos a realitzar**

1. **Obrir WP Local**  
   * Inicia el programari **WP Local** al PC de classe.  
   * Comprova que el panell principal estigui buit o que només hi hagi les webs ja creades.  
2. **Crear un nou lloc de WordPress**  
   * Afegeix una nova instal·lació des del botó **“Create a new site”**. Escriu el nom de la teva web seguint aquest patró:  web_proves_[Nom]. Ha de ser de l’estil web_proves_Cristian) Pero no posis Cristian si no et dius Cristian…  
3. **Configuració inicial**  
   * Configura l’usuari i contrasenya d’administrador (apunteu-vos-ho per no oblidar-ho).  
     * Feu servir el correu de l’escola, per exemple: cristian.gonzalez@mataro.epiaedu.cat  
     * Feu servir el usuari igual que el vostre correu, pero sense la part del correu, per exemple: cristian.gonzalez  
     * ⚠️La contrasenya, que sigui fàcil de recordar. No tenim cap sistema de recuperació.  
   * Mantingueu la configuració per defecte de PHP, MySQL i servidor web que proposa WP Local.  
   * Finalment, fes clic a **Add Site** i espera que acabi la instal·lació.  
4. **Accedir al tauler d’administració**

   Un cop el teu lloc ja està creat a WP Local, arriba el moment d’accedir al tauler d’administració, el lloc des d’on podràs gestionar tot el teu lloc web: pàgines, entrades, menús, disseny i configuracions.

   🔑 Què és el wp-admin?

   El **wp-admin** és l’adreça (URL) que porta al **panell de control intern** de WordPress.  
   És com la **porta d’entrada privada** a la part tècnica del teu web.

   Per exemple, si la teva web es diu web_proves_cristian.local, el panell d’administració estarà a:

   `http://web_proves_cristian.local/wp-admin`

   Des d’aquest espai podràs:

Crear i editar pàgines i entrades.  
Canviar l’aspecte del web (temes, menús, ginys...).  
Configurar opcions generals (nom del lloc, idioma, comentaris, etc.).  
Gestionar usuaris i rols.

  💡 **Pensa-hi així:**  
  La part wp-admin és com la **cuina d’un restaurant**: no la veu el públic, però és on es prepara tot el que després surt “a la sala” (la web pública).

  🌍 Distingir entre la vista d’administrador i la vista pública

  Quan treballes amb WordPress, és essencial saber **on ets en tot moment**:

  Quan treballes amb WordPress, és essencial saber **on ets en tot moment**:

| Vista | URL aproximada | Descripció |
| :---- | :---- | :---- |
| 🧑‍💻 **Vista d’administrador (wp-admin)** | `http://web_proves_nom.local/wp-admin` | És la zona privada. Només hi entres amb usuari i contrasenya. Serveix per **gestionar i configurar** el web. |
| 👀 **Vista pública (visitant)** | http://web_proves_nom.local | És el que veurien els **visitants** del teu lloc. Aquí només es mostra el contingut publicat (pàgines, entrades...). |

💡 Pots passar fàcilment d’una vista a l’altra:

Des del tauler, fes clic a dalt a l’esquerra on diu el **nom del teu web** i tria “Visita el lloc”.  
I des del lloc públic, si estàs identificat com a administrador, veuràs una **barra negra superior** amb l’opció “Tauler” per tornar a l’administració.

Accions:

Entreu a l’URL que us proporciona WP Local (sol ser http://web_proves_nom.local).  
  * Accediu al tauler de WordPress amb el vostre usuari i contrasenya.

Abans de continuar \- Canviarem tots al tema recomanat per a formació bàsica  **“Twenty Seventeen”**

**Motiu:**  És un tema oficial de WordPress, clàssic i sense dependències d’editors de blocs complexos.  
 Ofereix una estructura senzilla amb:

Una pàgina d’inici amb imatge de capçalera.  
Suport per a menú principal i menú de peu.  
Personalització des del Personalitzador clàssic (Aparença → Personalitza).  
Compatibilitat total amb l’editor clàssic (o Gutenberg sense maquetació avançada).  
Disseny responsive i net, perfecte per treballar conceptes essencials: **pàgines, entrades, menús i ginys**.

**5\.      Primers passos amb WordPress**

Creeu una primera **pàgina** de prova.  
  * Escriu com a **títol: Benvinguts al meu web personal**  
    * A l’espai del contingut, escriu una breu presentació sobre tu mateix:  
    * explica qui ets, què t’agrada o què esperes aprendre aquest curs. 💡 Si no saps què escriure, pots fer servir el Lorem Ipsum Generator per afegir text provisional.  
    * Publica la pàgina fent clic al botó “Publica” (a la part superior dreta).  
    * Desa el treball i revisa com queda fent clic a “Veure pàgina”.  
  * Afegeix una segona **pàgina** sobre mascotes 🐾  
    * Torna a **Pàgines → Afegir nova**.  
    * Títol: Les meves mascotes  
    * Afegeix contingut explicant si tens alguna mascota o, si no en tens, inventa’n una (pot ser un pokemon…).  
    * També pots afegir una imatge (fes servir el botó Afegeix un bloc → Imatge).  
  * Crea una **pàgina que es dirà Blog**. No tindrà cap contingut, perque serà a on aniran les entrades que anirem publicant.  
  * Crea **tres entrades** per al teu blog (seran per explicar els tres primers capitols d’una sèrie, si vols, pots descriure els **tres primers capítols de One Piece)**  
    * Ves a **Entrades → Afegir nova**.  
    * Escriu una **primera entrada** amb el títol:  
    * Opinió sobre una sèrie \- Capítol 1  
      1. Explica breument què t’agrada d’una sèrie que segueixis (pot ser One Piece, Stranger Things, The Boys, etc.).  
      2. Posa imatges, imatge destacada, categories, etiquetes  
      3. Genera-ho amb chatGPT i crea un contingut prou complet i llarg  
    * Repeteix el procés per crear **dues entrades més** sobre els dos capitols següents  
  * Compareu la diferència entre **pàgines** i **entrades**.  
  * Crea una **pàgina de contacte**  
    * Ves a **Pàgines → Afegir nova**.  
    * Escriu com a **títol: Contacte**  
    * **E**scriu un petit text que convidi els visitants a contactar amb tu.  
      1. Si vols contactar amb mi per parlar de sèries, tecnologia o gats, pots escriu-me  
      2. 💡 Més endavant, aprendrem a afegir **formularis de contacte reals**, però de moment n’hi ha prou amb el text.

     **6\.         Configuració bàsica.** Ara que ja tens creades les teves pàgines i entrades, configurarem el         comportament        principal del     teu web: decidirem què es mostra quan algú entra a la teva web i on s’agrupen les         entrades del     blog.

Per defecte, WordPress mostra **les entrades recents** a la pàgina principal.

Això pot anar bé per a un blog, però com que estem creant **un web personal**, ens interessa que la **pàgina d’inici** sigui una pàgina fixa (per exemple, “Benvinguts al meu web personal”), i que les **entrades** es mostrin a una altra pàgina (per exemple, “Blog”).

🧭 Passos per configurar-ho

    Entra al tauler de WordPress (wp-admin).

Ves al menú lateral esquerre i fes clic a:  Configuració → Lectura

A l’apartat **“La pàgina d’inici mostra”**, marca l’opció:  
🔘 **Una pàgina estàtica (selecciona a sota)**  
A continuació, escull:  
**Pàgina d’inici:** selecciona Benvinguts al meu web personal  
**Pàgina de les entrades:** selecciona Blog

Fes clic a **Desa els canvis** (a la part inferior de la pàgina).

  **7\.    Documentació de la tasca**

Creeu un document T11_wordpress_local.md dins la carpeta T11/ del vostre repositori GitHub amb:  
  * Nom de la web creada.  
    * Captures de pantalla del procés (creació amb WP Local, tauler de WordPress, pàgina i entrada creades).  
    * Explicació de la diferència entre pàgines i entrades.  
    * Descripció dels ajustaments configurats.

A l'arxiu [solucio.md](solucio.md) hi ha la solució descrita

[Torna a la pàgina principal](../README.md)
