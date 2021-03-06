# Adatvizualizációs műhely beadandó
*Molnár Adrián (Neptun kód: LWPJBS)*

### Beadandó célja:
#### Adatvizualizációs eszköz önálló használatának elsajátítátsa

### Választott eszközök:
  - **Python 3.7** 
    - *pandas könyvtár:* Nagy méretű fájlok kezelésére alkalmas
    - *matplotlib könyvtár:* Adatvizualizációs eszközökkel rendelkezik
  - **VisualStudio fejlesztői környezet**
    - VisualStudioval egyszerűen inportálhatóak a beadandóhoz szükséges könyvtárak. Az elkészült kód futtatására is alkalmas
 
### Adathalmaz:
  - KSH weboldaláról letöltött, magyarországi turizmussal kapcsolatos adatok
  - Az adathalmaz elemzése során felmerült érdekességek:
      - Ugrásszerű férőhelynövekedés: 1992 és 2010 körül ( 1_graf)
      - A vendgéjszakák és a vendégek száma közötti távolság egyre nagyobb (2_graf). Ebből azt gondolhatnánk, hogy átlagosan egy vendég         egyre több éjszakát foglal le. Erre azonban rácáfol az évszeinti foglalt éjszakák darabszáma (7_graf), ami csökkenő tendenciát           mutat. Ez a jelenség azért állhat elő, mert bár a foglalt éjszakák száma nő, a vendégek száma arányosan ennél gyorsabban nő,             ezért mutat csökkenést a 7_graf grafikon.
      - Legalcsonyabb szálloda kihasználtság a 2000-es évek körül volt. Legmagasabb kihasználtság 1978-79 krűörül, de még ez sem érte el         a 10%-ot.
      - A 8_graf alapján jol látszik, hogy évtizedenként a vendégek száma folyamatos növekvő tendenciát mutat.

### Megvalósítás:

  Első lépésben az adathalmazt python szabványoknak megfelőlre alakítottam (ékezetek eltávolítás). A beolvasás, azonosítás, új adatok     képzése a "pandas" könyvtár segítségével történt.
  
  A diagramok létrehozásához a matplotlib könyvtár pyplot és numpy gyűjteményeit használtam. A diagramok külalakjának testreszabása a     pyplot beépített funkcióival történt, úgy mint: vonalstílus, vonalszín, háttérstílus, alapstílus, oszlopdiagramok színe, szélessége,     több diagramtípus egy koordinátarendszeren való megjelenítése. A program futtatásakor a diagramok png formátumú fényképeit               automatikusan   a gyökérkönyvtárba generálja a "plt.savefig('1_graf.png')" sor.
  
  Az alap adathalmazhoz hozzáfűzött oszlopokat is készít a program a pandas könyvát segítségével, amit a memóriban tárol. A program       lefutása után az alap adathalmaz nem változik meg. Ezekből az általunk készített adatokból olyan vizualizációkat készíthetünk,           amelyekből egyszerűbben vonhatóak le a következtetések.
      
### Könyvtárstruktúra:
  - **PythonApplication1.py:** python forráskódot tartalmazó futtatható forrsáfájl. A külömböző diagramok megjelenítéséhez a "#" komment      jelek eltávolítása szükséges.
  - **.png fotók:** kapott diagramok png képformátumban.
  - **turizmus.xls:** adathalmaz

### Fejlesztési lehetőségek:
  - **Menüredszer kialakítása**
  - **Diagramok külalkjának megformázása a felhasználástól függően**
  - **Különböző kimutatásokank megfelelő adatok készítése az alap adathalmazból (pandas könyvtár)**
  - **Az eredmények összevetése az évenkénti gazdasági növekedés/csökkenés adataival**
