## ✍️ Hosszú poszt lesz (TL;DR), de azt hiszem, hogy érdemes elolvasnod – és bízok is ebben.

Egy szentendrei FB-csoportban egy beruházó (vagy képviselője) arról posztolt, hogy új bevásárlóközpont fog épülni a szentendrei Interspar-ral szemben, és megkérdezte a helyieket, hogy ki milyen üzletnek örülne – merthogy most tárgyalnak mindenféle boltokkal és üzletláncokkal.
🤔 Én őszintén szólva nem igazán örültem a hírnek, mert zöldterületre épül az új bevásárlóközpont, és én nem hiszek abban, hogy egy, a város szélén elhelyezkedő és csak autóval megközelíthető bevásárlóközpontra van szükségünk. De hát kapitalizmus van, a zöldterület, amin épül, az pedig már nagyon rég (évtizedek óta) ki volt szabályozva GKSz besorolásúvá, azaz gazdasági-kereskedelmi övezetté. És ha egy magánberuházó kockáztat, az az ő szíve joga.

Nem is szóltam a bejegyzéshez hozzá, de azt azért érzékeltem, hogy túlnyomó többségében pozitív, a hírt nagyon is üdvözlő kommentek érkeznek, és persze jönnek válaszok is, hogy ki milyen üzletnek örülne.
🗣️ Aztán pár nappal később visszanéztem oda, már többszáz komment volt, és láttam, hogy páran azért írják, hogy nem az a jó irány, hogy a zöldterület rovására mennek ezek a beruházások, de láttam, hogy ez egy kisebbség. Amihez én is tartozom.

✊ Sebaj, gondoltam, szokva vagyok ahhoz, hogy a véleményem sokszor kisebbségi vélemény. Tisztában vagyok vele, hogy a többség szerint nincs semmi gond a klímaváltozással, nincs összefüggésben az életformánkkal (amihez a városszéli bevásárlóközpontok is tartoznak), meg úgysincs ráhatásunk. Hogy sokak szerint csak "klímahiszti" van, arról itt már szó se essék. Oké – gondoltam – már megszoktam a kisebbségi létet.
Aztán pár nap múlva már láttam, hogy 500 komment van rajta, és bizony sok szálon vitatkoznak, és sokan kommentelnek olyat, hogy ez igazából nem jó hír, ők nem örülnek neki. És nem csak olyanok, akikről tudom, hogy fontos számukra a környezetvédelem vagy az ajtót ránk rugó klímaváltozás. Még később már elérte a 700-at a kommentek száma.

### ❗ És ekkor jött az ötlet, hogy de jó lenne tudni, hogy vajon tényleg ennyire kisebbségben vagyok azzal a véleményemmel, hogy nem ez a jó irány? Hogy egy zöldmezős beruházásban készülő nagy bevásárlóközpont nem feltétlenül örömhír?

**Úgyhogy kicsit nekiestem az adatoknak.**

🗃️ Letöltöttem az összes kommentet, tisztítottam az adatokat, anonimizáltam a neveket benne (mert ugyan a poszt nyilvános, de ha adatbázist készítek belőle, akkor már anonimizálni kell az adatokat), és a Llama 3.1 nagy nyelvi modell segítségével, API-n keresztül, szentiment elemzést végeztem rajta. Ez utóbbit hadd magyarázzam el: arra kértem a nyelvi modellt (a Llama 3.1 valamennyire tud magyarul), hogy 1-től 10-ig pontozza a kommenteket: 1-es nagyon ellene van, a komment nagyon negatív, a 10-es pedig azt jelenti, hogy nagyon mellette van, nagyon pozitív töltetű.
A készen kapott adatokon aztán egyszerű adatelemzést végeztem.
A módszerhez hozzá tartozik, hogy mivel a nagy nyelvi modellek nem determinisztikusak (azaz minden egyes megkérdezéskor ugyanarra a kommentere nem mindig ugyanazt válaszolják), ezért kétféle modellt használtam, mindkettőn ötször lefuttattam a szentiment elemzést, és az így kapott összesen 10-féle eredményt átlagoltam.

☝️ És még mielőtt az eredményt leírnám, annyit még, hogy ez egy elég egyszerű adatelemzés: nyilván lehetne vizsgálni a kommentek időbeli lefolyását, meg lehetett volna próbálni mélyebb tartalmi kontextusba helyezni az egyes kommenteket, vagy kutatni, hogy volt-e olyan, akinek a véleménye változott az időben előre haladva. De az eredeti kérdésemre ez az egyszerű elemzés is választ ad. **Azaz arra, hogy mennyire vannak kisebbségben azok, akiknek nem tetszik ez az új bevásárlóközpont?**

1️⃣. ábra: összesen 711 komment érkezett a posztra, ránézésre látszódik, hogy több a beruházást támogató komment, szépen eloszlanak a szentiment pontszámok.

2️⃣. Jobban megérthetjük az eloszlást, ha 5 csoportra osztjuk a kommenteket: nagyon ellenzők (1-1.99), inkább ellenzők (2-4.99), semlegesek (5-7), inkább támogatók (7.01-9), nagyon támogatók (9.01-10). Itt jött az első meglepetésem: ugyan összességében többen támogatják a projektet, de az ellenzők is bizony sokan vannak, és egyáltalán nem egy törpe kisebbség, nem néhány százalék! Inkább ellenzi 135 (1+134) komment, inkább támogatja 247 (203+44).

3️⃣. De vegyük ki azt a tényezőt, hogy nyilván a támogatók és az ellenzők között is vannak nagyon aktív felhasználók, akik sokat kommentelnek, esetleg meg akarnak másokat győzni az igazukról. Ezért arra gondoltam, hogy az összes komment helyett vegyünk csak minden felhasználótól egy kommentet. Az egyszerűség kedvéért mindenkitől csak az általa elsőnek írt komment hangulati (szentiment) pontértékét vegyük számításba – feltétezve, hogy többségében, amikor az ember először hozzászól, akkor le is írta a véleményét.
293 különböző felhasználó (azaz ember) szólt hozzá. Az 1-től 10-ig tartó skála képe nem tér el különösebben attól az ábrától, amikor az összes kommentet vizsgáltam.

4️⃣. Az 5-ös csoportosítás esetén itt is látszik, hogy jobban eltolódott a támogatók felé az eloszlás, de még mindig nem váltak törpe kisebbséggé az ellenzők. Az következik ebből, hogy sok olyan támogató volt, aki kifejezte örömét – egyet kommentelt –, és nem foglalkozott azzal, hogy belemenjen vitákba. Mindenesetre 57 ember az, aki inkább ellenzi, és 120 ember volt, aki inkább támogatja.

5️⃣. Kördiagramon, százalékokkal együtt mutatva jobban lehet látni az arányokat:
* az összes kommentet elemezve: 19% ellenzi, 35% van mellette.
* csak az első kommentet figyelembe véve: 19% ellenzi, 41% van mellette.

5️⃣. És vizsgáltam azt is, hogy a különféle aktivitású kommentelők csoportja mennyire van mellette vagy ellene. Itt jön ki jól, hogy az egyszer kommentelők között szignifikánsan több a támogató komment, mint a többi csoportban, és érdekes, hogy a sokat (min 4.) kommentelők között többségben vannak a semleges állásponton lévők, illetve az ellenzők. Az ellenzők csak itt vannak többen, mint a támoagtók. Valószínűleg a nagyobb elkötelezettségük miatt kommenteltek többet.

👉 Itt fontos megjegyeznem, hogy a beruházó képviselője – nyilvánvalóan – a legtöbbet kommentelők között van, de nagyon visszafogott stílussal nyilvánult meg, azaz az ő kommentjei valószínűleg a semlegesek között vannak inkább. De ez az adatokon nem látszik, az adat nem minden!

### ℹ️ Amit én leszűrtem ℹ️
Számomra egyértelműen kiderült, hogy többségben vannak Szentendrén azok, akik örülnek egy ilyen beruházásnak – ezt sejtettem is –, de egyáltalán nem elhanyagolható kisebbségi álláspont az, hogy egy bevásárlóközpont zöldmezős beruházásként nem a jó irány. Ez volt nekem a legfőbb meglepetés. Nagyságrendileg bizony összehasonlítható a két sokaság: azaz az ellenzők és a támogatók aránya. Az arányok miatt talán akkor fogalmazok jól, ha azt írom, hogy a közel 30 ezres városunk megosztott ebben a kérdésben. 
Az én nézőpontomból – én sem örülök egy ilyen bevásárlóközpontnak – ez bizony örömhír.

 ## 🟩Hadd írjak még pár továbbgondolni valót! 🟩
"Oké, oké, nem örülsz egy ilyen projektnek, akkor mit kéne csinálni, te pupák?"
• Szerintem tök jó lenne eljutni odáig, hogy már csak barnamezős beruházásokat lehessen itthon csinálni, azaz a zöldfelület kárára maximum csak létfontosságú beruházásokat lehessen építeni. Tudom, az akkugyárak országában ez utópiának tűnhet, de én azért itt hagyom ezt a gondolatot. Szerintem minden döntéshozónak ilyen irányba kéne gondolkodnia, e felé kéne mennie!
• Szentendrén nagyon sok olyan terület van, ami baromi rég ki van már szabályozva ipari, gazdasági területnek, és a tulajdonosa oda bármikor felhúzhat valamit: egy csarnokot, egy üzemet, logisztikai bázist, bevásárlóközpontot, akármit. Attól tartok, hogy a szentendreiek ezekről mit sem sejtenek, az önkormányzat pedig nem rakja ki köuérthetően, mondjuk kataszter-szerűen, hogy "no, nézzétek, ennyi és ennyi terület van kiszabályozva, de még beépítetlenül". Ezért minden egyes építkezéskor sokan meglepődnek, hogy "már megint mi épül itt?" Lehet, hogy ha már az önkormányzat nem mutatja ezt be, érdemes lenne adatigénylések sorával és geoadatbázis segítségével önkéntes munkával csinálni egy nyilvános szentendrei térképet.
• Ez a poszt a legkevésbé sem a (tulajdonos)-vállalkozóról szól! Ő csinál valamit, vállalkozik, kockáztat egy olyan területen, amin a lehetőség már régóta adott.
• A poszt végső soron rólunk szól! Ugyanis a sok-sok régi és mostani döntésünk – a mi döntéseink, a korábbi generációké, tervezők, döntéshozók, szüleink, nagyszüleink döntései, végső soron a mi, emberek, szentendreiek, magyarok döntései – mégiscsak előállított egy olyan helyzetet, ahol folyamatosan csökkennek a zöldterületek, és a kisvárosaink elvesztik a jellegüket.

______

## Ha idáig eljutottál:
- a teljes Python kódsor itt van a [Githubon](https://github.com/agatity/dera_park_analysis/)
- az eredeti poszt pedig itt olvasható a Szentendre Blogol [FB-csoportban](https://www.facebook.com/groups/szteblogol/posts/7220377584650331/)
