# Decentralizált cinkelt kocka algoritmus

A választás során egy ellenzéki többségű körzet nagyjából kétféleképp nyerhető: ha a  pártok megegyeznek egy közös indulóban, vagy ha a szavazók megegyeznek egy közös indulóban. Utóbbit segítheti ez az itt bemutatott algoritmus, amely figyelembe veszi az ellenzéki pártok országos támogatottságát is, és annak arányában javasol körzetről körzetre más és más, de országos szinten a népszerűségekkel arányos számú jelöltet az ellenzékieknek, választásra.

## A maszlag

Ahogy a "kocogtatok" szó is erősen szöveg környezet érzékeny - "én" vagy "ti" - úgy a "visszacsatolás párti", is csak egyes embereknek juttatja a trianoni békeszerződést eszébe. Mások, főleg műszakiak, tudják, hogy a "jó tett helyébe jót várj" mondás igazságára utal ez a sajnálatosan inkább műszó kategóriába eső kifejezés, aminek a hétköznapi elterjedtsége nagyon hiányzik a magyar nyelvből: talán még a demokráciához és a kapitalizmushoz való viszonyunkat is aláássa, hogy nem gondolkodunk nyelvi szinten abban, az emberre a cselekedeteinek vissza kell hatnia. A modern társadalmak mind erre épülnek, ettől fejlődtek fel. Ahol a visszacsatolás sérül, ott csak a neveltetésen, elveken, eszméken, vagy épp hiten múlik, ki hogyan cselekszik, de az pár évszadnyi középkoron át nem vitt sehova.

Ma Magyarországon ez a visszacsatolás sérül a politikában az új, 2010 utáni választási rendszer és az ellenzéki pártok számosságának nem is olyan szövevényes együttállása miatt: a relatív többség alapú, egy fordulós választásban az ellenzék rendre alul marad a körzetekben, lásd 2018-ban, ahol "országosan" (határon túli szavazatokkal együtt) 49,5%-nyi szavazó voksolt a kormányra listán. Éppcsak az ellenzék 50,5%-nyi szavazója szanaszét szavazott a versengő ellenzéki pártokra, így az országos többség végül a körzetek miatt is a jelenlegi kormányé lett. Erre a jelenségre több megoldás is elképzelhető, például összefogás előválasztás alapján a relevánsabb körzetekben. De mi lesz azon területeken, ahol nincs meg az emberi és-vagy anyagi erőforrás az ellenzék egységesítésére, és a verseny miatt továbbra is eloszlanának az ellenzéki szavazatok?

## Műszakibb leírás

Legkézenfekvőbb, ha a szavazók maguk egyeznek meg, kire szavazzanak. De hogyan lehet azt megszervezni egy előválasztás nélkül?

Ha a szavazók minden körzetben a valóban ellenzéki pártok jelöltjei közül szimplán a névsorban legelsőt választanák, akkor országos szinten a nevek véletlenszerűsége miatt kb. azonos számú körzeti képviselő juthatna be az országgyűlésbe az egyes ellenzéki pártokból. Későbbiekben ez a módszer egy offline is működőképes számítógépes programmal vagy okostelefon applikációval tovább finomítható úgy, hogy az egyes körzetekben a szoftver által tett véletlenszerű javaslatok országos szintű végeredménye közelítse a pártok valódi országos támogatottságát.

Ez technikailag megoldható... Valahogy így:

Induljunk ki abból, hogy a pártvezetők kidobhatnák egy sima dobókockával, melyik körzetben melyikük jelöltje induljon. Ennek a decentralizált megfelelője, ha ABC sorrendben, praktikusan az első - releváns - ellenzéki jelöltre szavaz mindenki a saját helyi listájáról. Ez azonban még nem tükrözi a pártok országos népszerűségét. Ahhoz egy cinkelt kockán keresztül vezethetne az út, amit a pártvezetők a pártjaik népszerűsége szerint súlyozhatnának. Ez azonban nem decentralizált, vagyis nem hajtható végre állampolgárként, egyemberként.

A "decentralizált cinkelt kocka" technikai megoldása jobban hasonlítható egy olyan kártya játékhoz ahol a legerősebb kártya birtokosa nyer, és a pártjaik országos népszerűségével arányos számú lapot kapnak az egyes körzetek helyi jelöltjei párt hovatartozásaik alapján. A leosztáshoz egy ún. ál-véletlen generátorra van szükség, ami egy olyan matematikai számítás amely azonos bemenetre mindig ugyanazzal, a bemeneti adat függvényében egyébként rendkívül megjósolhatatlanul változó eredménnyel reagál. Ez ott jön be a képbe, hogy nem a pártok vezetői vagy jelöltjei játsszák le a  képzeletbeli kártya játékot, hanem minden szavazónak egyenként, "passziánsz jelleggel" a saját szoftvere számolja ki, hogy kire érdemes szavaznia egymástól függetlenül, offline, központi koordinációtól mentesen. Ahhoz azonban, hogy körzetenként minden szavazó mégis ugyanazt a tanácsot kapja, a kiindulási lapjaiknak egyezniük kell! Eközben ahhoz, hogy orszagos szinten körzetről körzetre valtozó legyen a végeredmény, így tükrözve az országos népszerűségi szinteket, az egyes körzetekben azonos, de az eltérő körzetekben már más és más leosztásra van szükség az egyes "passziánszozó" applikációkban. Ezt a két feltételt egyszerre teljesíti, ha a lapjárást a körzetenként változó, de egy adott körzetben azonos névlistakat bemenetként használó ál-véletlen generátor segítségével osztjuk ki. Mintegy a körzeti név listákat használva egységes igazodási pontként.

A lapjárást még célszerű a választás előtti, utolsó előtti - kb. 1 hetes - Joker sorsolás eredményétől is függővé tenni, több okból is:
1) szinte az utolsó napig nem derül ki, kiket fog javasolni a szoftver, így lejáratni, politikailag támadni sem tudni, melyik körzetben kiket kell pontosan
2) a pártok körzetenkénti reprezentációja, bár közelíteni fogja azok korábban mért országos népszerűségét, de a statisztikai folyamat szórása és a körzetek véges száma miatt ez matematikailag nem lehet tökéletes, lesz amelyik párt a pontos népszerűségéhez képest kicsit felül reprezentáltabb lesz, lesz amelyik alul, és a Joker sorsoláson múlik gyakorlatilag, hogy ez végül az adott választáson éppen pontosan hogyan alakul
3) a 2) pont szerinti eltérések véletlenszerűen alakulnak választásról választásra, amíg a választáshoz ezt az algoritmust használjuk és a mostani törvény hatályos
4) a különböző későbbi választásokon akkor is más és más eredmény születik majd, ha történetesen egy-két helyen ugyanazok a nevek indulnának

Az algoritmus működéséhez kritikus, hogy
 - mindenki precízen és pontosan ugyanazt az algoritmust használja
 - az egy körzetben szavazók ugynazokat a neveket adják meg (ékezet, kis és nagy betű, de még a szóközök száma (1) is befolyásol)
 - országosan pedig azonos esélyeket adjanak meg az egyes pártok helyi indulóinak (utóbbihoz per pillanat jó kiindulási alap lehet az önkormányzati választás, máskor a legutolsó hasonlóan hiteles országos népszerűségi felmérés)
 - a Joker szám ismert legyen mindenki számára (ezért érdemes az egy héttel korábbit használni, ha a sorsolás "véletlenül" elmaradna, akkor "ééééhhnn" formátumban a választás napja adandó meg)

Ha a kormányt leváltani akaró szavazó polgárok mind, önként ezen eljárás szerint választanak, akkor gyakorlatilag csak az egyszerű, abszolút többségükön múlik egy-egy körzet megnyerése, még akkor is, ha több, egymás közt nem koordináló ellenzéki párt száll versenybe!

A vázolt eljárás offline, önállóan számolja ki a javasolt jelölteket, használata semmilyen központi adatgyűjtést nem igényel, és központosított koordinációt is csak annyiban tesz szükségessé, hogy ha a lakosság több különféle alkalmazást használna, vagy több különféle véletlen szám forrást adna meg (egy hetes Joker helyett), azzal újfent megosztaná saját magát a helyi ellenzéki jelöltek között, és valószínűleg elveszítené az helyi választási körzeteket.

Arra az esetre ha több applikáció létrehozása miatt komprimittálódna a szavazatok egységesítése, és nem sikkerülne időben megszervezni, hogy melyiket használjuk egységesen, marad _vészforgatókönyvnek az ABC sorrendben 1. (első) releváns ellenzéki körzeti jelölt választása!_
