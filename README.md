### _[[ MAGYAR VÁLTOZATÉRT GÖRGESS LEJJEBB ]]_

## ✍️ It's going to be a long post (TL;DR), but I think it's worth reading, and I hope you will.

In a Facebook group of my home town, Szentendre, an investor (or his representative) posted about a new shopping center to be built opposite the Interspar in Szentendre, and asked locals what kind of shop they would like to see—because they are now negotiating with all kinds of shops and franchises.

🤔 I honestly wasn't too happy about this because the new shopping center is being built on green space, and I don't believe we need a shopping center on the outskirts of town, accessible only by car. But we live in capitalism, and the green space on which it is being built was zoned to "GKSz" decades ago. (GKSz means an economic-commercial zone.) And if a private developer takes a risk, that's his choice.


I didn't comment on the post, but I did notice that there are overwhelmingly positive comments, very much welcoming the news, and of course there are replies about what kind of shops preferred.

![Kép a Dera-parkról](https://github.com/agatity/dera_park_analysis/blob/main/dera_latvanyterv.jpg)

🗣️ Then I looked back a couple of days later, there were hundreds of comments, and I saw that some people were writing that it was not the right direction, that these investments were at the expense of green space, but I saw that this was a minority. I am part of that minority.


✊ Never mind, I thought, I'm used to my opinions often being a minority opinion. I am aware that the majority think there is nothing wrong with climate change, it has nothing to do with our way of life (which includes the peri-urban shopping centers) and we have no control over it anyway. And let's not mention the fact that many people think it's just a 'Climate-Change Hysteria'. OK, I thought, I'm used to being a minority.
Then a few days later I saw that there were 500 comments on it, and there were many threads arguing, and many people commenting that it was not really good news, that they were not happy about it. And not just people who I know care about the environment or about the fact climate change has been kicked on the door. Even later the number of comments reached 700.

### ❗ And that's when I had the idea that it would be nice to know, am I really in such a minority in my opinion that this is not the right direction? That a big shopping center in the form of greenfield project is not necessarily good news?

**So I've had a bit of a run at the data.**

🗃️ I downloaded all the comments, cleaned the data, anonymized the names in it (no matter it's a public post, if I make a database out of it, I have to anonymize the data), and did a sentiment analysis on it using the Llama 3.1 large language model via API. Let me explain the latter: I asked the language model (Llama 3.1 knows some Hungarian) to score the comments from 1 to 10. A score of 1 is very much against it, the comment is very negative, and a 10 means very much go for it, very positively toned.

Then I ran a simple data analysis on the data.

The method involves the fact that, since the large language models are not deterministic (i.e. the same comment is not always answered the same way each time it's been asked), I used two different models and ran the sentiment analysis five times on each and averaged the resulting total of 10 results.

☝️ And before I describe the results, let me note it's a pretty simple data analysis process: obviously I could look at the time course of comments, try to put each comment in a deeper context of content, or look at whether there were any people whose opinions changed over time. But my original question has been answered by this simple analysis. **That is, how much of a minority are those who don't like this new mall?**

**Figure 1️⃣**: a total of 711 comments were received on the post, showing that there are more comments in favor of the investment, with a nice distribution of sentiment scores.

![Első ábra](https://github.com/agatity/dera_park_analysis/blob/main/charts/Distribution_of_Sentiment_Scores_total_replies.png)

**Figure 2️⃣**: We can better understand the distribution if we divide the comments into 5 groups: very opposed (1-1.99), rather opposed (2-4.99), neutral (5-7), rather in favor (7.01-9), very in favor (9.01-10). This is the first time I was surprised: although overall more people support the project, there are also a lot of opponents. And they're not a tiny minority—not a few percent! There are 135 (1+134) comments against, 247 (203+44) in favour.

![Második ábra](https://github.com/agatity/dera_park_analysis/blob/main/charts/Distribution_of_Sentiment_Scores_total_replies_in_Five_Segments.png)

**Figure 3️⃣:** But let's take out the factor that obviously there are very active users among both supporters and opponents. They comment a lot, perhaps trying to convince others of their rightness. So I thought that instead of all comments, we should consider only one comment from each user. And for the sake of simplicity, let's take only the sentiment score of the first comment posted by each user–assuming that in most cases, the first time a user posts a comment, he/she has written his/her opinion.

293 different users (i.e. people) have commented. The picture of the scale from 1 to 10 is not particularly different from the picture when I looked at all comments.

![Harmadik ábra](https://github.com/agatity/dera_park_analysis/blob/main/charts/Distribution_of_Sentiment_Scores_first_comments.png)

**Figure 4️⃣:** Again, for the grouping of 5, you can see that the distribution has shifted more towards those in favour, but those who are against it are still not a minority. The implication is that there were many supporters who expressed their pleasure—write a single comment—and did not bother to get into debates. In any case, there were 57 people who preferred to oppose and 120 who preferred to support.

![Negyedik ábra](https://github.com/agatity/dera_park_analysis/blob/main/charts/Distribution_of_Sentiment_Scores_in_Five_Segments_first_comments.png)

**Figure 5️⃣-8️⃣.**: A pie chart with percentages gives a better view of the proportions:

* analyzing all comments: 19% are against, 35% are in favor.

* considering only the first comment: 19% against, 41% in favor.

![Ötödik ábra](https://github.com/agatity/dera_park_analysis/blob/main/charts/Community_Sentiment_Segmentation.png)
![Hatodik ábra](https://github.com/agatity/dera_park_analysis/blob/main/charts/Community_Sentiment_Segmentation_piechart.png)

![Hetedik ábra](https://github.com/agatity/dera_park_analysis/blob/main/charts/Community_Sentiment_Segmentation_first_comments.png)
![Nyolcadik ábra](https://github.com/agatity/dera_park_analysis/blob/main/charts/Community_Sentiment_Segmentation_first_comments_piechart.png)

**9️⃣ Figure:** And I also looked at how much the group of commenters with different levels of activity are for or against it. Here it comes out well that there are significantly more supportive comments among those who commented once than in the other groups, and it is interesting that among those who commented a lot (min 4) there is a majority of neutral commenters and those who commented against. Opponents are only here more numerous than supporters. They probably commented more because of their higher engagement.

![Kilencedik ábra](https://github.com/agatity/dera_park_analysis/blob/main/charts/User_Engagement_Segmentation.png)

👉 It's important to note at this point that the investor's representative is, obviously, among the most active users, but he had a very restrained and neutral style, i.e. his comments are probably more neutral. But this is not reflected in the data; data is not everything!

### ℹ️ What I have deduced ℹ️
For me, it became clear that there are a majority of those in Szentendre who are happy about such an investment—I had guessed that—but a not inconsiderable minority position is that a shopping center is not the right direction as a green field investment. This was the biggest surprise for me. In terms of magnitude, the two groups can certainly be compared: i.e. the proportion of opponents and supporters. Because of the proportions, perhaps I'm speaking well when I write that our city of nearly 30,000 people is divided on this issue.

From my point of view—I am not happy about such a shopping center either—this is indeed good news.

 ## 🟩Let me write a few more things to think about! 🟩
*"Okay, okay, you're not happy about a project like this, so what would you do, you punk?"*
* I think it would be great to get to the point where only brown field investments can be made at home, i.e. only vital investments can be built at the expense of green space. I know, in the country of battery factories, this may seem like a utopia, but I will leave this thought here. I think every decision-maker should think in this direction, should go in this direction!
* There are a lot of areas in Szentendre that have long since been regulated as industrial and economic areas, and the owner can build something there at any time: a hall, a factory, a logistics base, a shopping center, whatever. I'm afraid that the people of Szentendre have no idea about this, and the municipality doesn't put it out in a comprehensible way, let's say like a cadaster. In this way the municipality could say, "Well, look, guys, so much area is regulated but still undeveloped." That's why many people are surprised at each construction: "What is being built here?" they often say. Maybe if the municipality doesn't present this, it would be worthwhile to make a public map of Szentendre by volunteering with a series of data requests and using a geodatabase.
* This post is not about the owner/entrepreneur in the least! He does something and takes risks in an area where the opportunity has been there for a long time.
* The post is ultimately about us! Because our many past and present decisions—our decisions, the decisions of previous generations, planners, decision-makers, our parents', grandparents', ultimately the decisions of the people of Szentendre, the Hungarians—still created a situation where green areas are constantly decreasing, and our small towns lose their character.

______

## If you've made it this far:
- the complete Python code with the anonymized database is over here on [Githubon](https://github.com/agatity/dera_park_analysis/)
- and the original post can be read here on the 'Szentendre Blogol' [Facebook group](https://www.facebook.com/groups/szteblogol/posts/7220377584650331/)
- my Facebook post can be [read here](https://www.facebook.com/aron.kubatovics/posts/pfbid02QGJe1zQU6dF4p4KyLxhaizJmPQEfWB7C94VFKGGjBdhzqybEpnoNqznskLesBKRjl)
- and I put it on [LinkedIn](https://www.linkedin.com/posts/kubatovics_a-data36com-nak-aj%C3%A1nlom-ezt-a-posztomat-activity-7257468509595586560-b1R0?utm_source=share&utm_medium=member_desktop) is

📷 Visual design: "Dera-park" (Facebook)

### _[[ MAGYAR SZÖVEG ]]_

## ✍️ Hosszú poszt lesz (TL;DR), de azt hiszem, hogy érdemes elolvasnod – és bízok is ebben.

Egy szentendrei FB-csoportban egy beruházó (vagy képviselője) arról posztolt, hogy új bevásárlóközpont fog épülni a szentendrei Interspar-ral szemben, és megkérdezte a helyieket, hogy ki milyen üzletnek örülne – merthogy most tárgyalnak mindenféle boltokkal és üzletláncokkal.

🤔 Én őszintén szólva nem igazán örültem a hírnek, mert zöldterületre épül az új bevásárlóközpont, és én nem hiszek abban, hogy egy, a város szélén elhelyezkedő és csak autóval megközelíthető bevásárlóközpontra van szükségünk. De hát kapitalizmus van, a zöldterület, amin épül, az pedig már nagyon rég (évtizedek óta) ki volt szabályozva GKSz besorolásúvá, azaz gazdasági-kereskedelmi övezetté. És ha egy magánberuházó kockáztat, az az ő szíve joga.


Nem is szóltam a bejegyzéshez hozzá, de azt azért érzékeltem, hogy túlnyomó többségében pozitív, a hírt nagyon is üdvözlő kommentek érkeznek, és persze jönnek válaszok is, hogy ki milyen üzletnek örülne.

![Kép a Dera-parkról](https://github.com/agatity/dera_park_analysis/blob/main/dera_latvanyterv.jpg)

🗣️ Aztán pár nappal később visszanéztem oda, már többszáz komment volt, és láttam, hogy páran azért írják, hogy nem az a jó irány, hogy a zöldterület rovására mennek ezek a beruházások, de láttam, hogy ez egy kisebbség. Amihez én is tartozom.

✊ Sebaj, gondoltam, szokva vagyok ahhoz, hogy a véleményem sokszor kisebbségi vélemény. Tisztában vagyok vele, hogy a többség szerint nincs semmi gond a klímaváltozással, nincs összefüggésben az életformánkkal (amihez a városszéli bevásárlóközpontok is tartoznak), meg úgysincs ráhatásunk. Hogy sokak szerint csak "klímahiszti" van, arról itt már szó se essék. Oké – gondoltam – már megszoktam a kisebbségi létet.
Aztán pár nap múlva már láttam, hogy 500 komment van rajta, és bizony sok szálon vitatkoznak, és sokan kommentelnek olyat, hogy ez igazából nem jó hír, ők nem örülnek neki. És nem csak olyanok, akikről tudom, hogy fontos számukra a környezetvédelem vagy az ajtót ránk rugó klímaváltozás. Még később már elérte a 700-at a kommentek száma.

### ❗ És ekkor jött az ötlet, hogy de jó lenne tudni, hogy vajon tényleg ennyire kisebbségben vagyok azzal a véleményemmel, hogy nem ez a jó irány? Hogy egy zöldmezős beruházásban készülő nagy bevásárlóközpont nem feltétlenül örömhír?

**Úgyhogy kicsit nekiestem az adatoknak.**

🗃️ Letöltöttem az összes kommentet, tisztítottam az adatokat, anonimizáltam a neveket benne (mert ugyan a poszt nyilvános, de ha adatbázist készítek belőle, akkor már anonimizálni kell az adatokat), és a Llama 3.1 nagy nyelvi modell segítségével, API-n keresztül, szentiment elemzést végeztem rajta. Ez utóbbit hadd magyarázzam el: arra kértem a nyelvi modellt (a Llama 3.1 valamennyire tud magyarul), hogy 1-től 10-ig pontozza a kommenteket: 1-es nagyon ellene van, a komment nagyon negatív, a 10-es pedig azt jelenti, hogy nagyon mellette van, nagyon pozitív töltetű.

A készen kapott adatokon aztán egyszerű adatelemzést végeztem.

A módszerhez hozzá tartozik, hogy mivel a nagy nyelvi modellek nem determinisztikusak (azaz minden egyes megkérdezéskor ugyanarra a kommentere nem mindig ugyanazt válaszolják), ezért kétféle modellt használtam, mindkettőn ötször lefuttattam a szentiment elemzést, és az így kapott összesen 10-féle eredményt átlagoltam.

☝️ És még mielőtt az eredményt leírnám, annyit még, hogy ez egy elég egyszerű adatelemzés: nyilván lehetne vizsgálni a kommentek időbeli lefolyását, meg lehetett volna próbálni mélyebb tartalmi kontextusba helyezni az egyes kommenteket, vagy kutatni, hogy volt-e olyan, akinek a véleménye változott az időben előre haladva. De az eredeti kérdésemre ez az egyszerű elemzés is választ ad. **Azaz arra, hogy mennyire vannak kisebbségben azok, akiknek nem tetszik ez az új bevásárlóközpont?**

**1️⃣. ábra**: összesen 711 komment érkezett a posztra, ránézésre látszódik, hogy több a beruházást támogató komment, szépen eloszlanak a szentiment pontszámok.

![Első ábra](https://github.com/agatity/dera_park_analysis/blob/main/charts/Distribution_of_Sentiment_Scores_total_replies.png)

**2️⃣. ábra**: Jobban megérthetjük az eloszlást, ha 5 csoportra osztjuk a kommenteket: nagyon ellenzők (1-1.99), inkább ellenzők (2-4.99), semlegesek (5-7), inkább támogatók (7.01-9), nagyon támogatók (9.01-10). Itt jött az első meglepetésem: ugyan összességében többen támogatják a projektet, de az ellenzők is bizony sokan vannak, és egyáltalán nem egy törpe kisebbség, nem néhány százalék! Inkább ellenzi 135 (1+134) komment, inkább támogatja 247 (203+44).

![Második ábra](https://github.com/agatity/dera_park_analysis/blob/main/charts/Distribution_of_Sentiment_Scores_total_replies_in_Five_Segments.png)

**3️⃣. ábra:** De vegyük ki azt a tényezőt, hogy nyilván a támogatók és az ellenzők között is vannak nagyon aktív felhasználók, akik sokat kommentelnek, esetleg meg akarnak másokat győzni az igazukról. Ezért arra gondoltam, hogy az összes komment helyett vegyünk csak minden felhasználótól egy kommentet. Az egyszerűség kedvéért mindenkitől csak az általa elsőnek írt komment hangulati (szentiment) pontértékét vegyük számításba – feltétezve, hogy többségében, amikor az ember először hozzászól, akkor le is írta a véleményét.
293 különböző felhasználó (azaz ember) szólt hozzá. Az 1-től 10-ig tartó skála képe nem tér el különösebben attól az ábrától, amikor az összes kommentet vizsgáltam.

![Harmadik ábra](https://github.com/agatity/dera_park_analysis/blob/main/charts/Distribution_of_Sentiment_Scores_first_comments.png)

**4️⃣. ábra:** Az 5-ös csoportosítás esetén itt is látszik, hogy jobban eltolódott a támogatók felé az eloszlás, de még mindig nem váltak törpe kisebbséggé az ellenzők. Az következik ebből, hogy sok olyan támogató volt, aki kifejezte örömét – egyet kommentelt –, és nem foglalkozott azzal, hogy belemenjen vitákba. Mindenesetre 57 ember az, aki inkább ellenzi, és 120 ember volt, aki inkább támogatja.

![Negyedik ábra](https://github.com/agatity/dera_park_analysis/blob/main/charts/Distribution_of_Sentiment_Scores_in_Five_Segments_first_comments.png)

**5️⃣-8️⃣. ábra:** Kördiagramon, százalékokkal együtt mutatva jobban lehet látni az arányokat:
* az összes kommentet elemezve: 19% ellenzi, 35% van mellette.
* csak az első kommentet figyelembe véve: 19% ellenzi, 41% van mellette.

![Ötödik ábra](https://github.com/agatity/dera_park_analysis/blob/main/charts/Community_Sentiment_Segmentation.png)
![Hatodik ábra](https://github.com/agatity/dera_park_analysis/blob/main/charts/Community_Sentiment_Segmentation_piechart.png)

![Hetedik ábra](https://github.com/agatity/dera_park_analysis/blob/main/charts/Community_Sentiment_Segmentation_first_comments.png)
![Nyolcadik ábra](https://github.com/agatity/dera_park_analysis/blob/main/charts/Community_Sentiment_Segmentation_first_comments_piechart.png)

**9️⃣. ábra:** És vizsgáltam azt is, hogy a különféle aktivitású kommentelők csoportja mennyire van mellette vagy ellene. Itt jön ki jól, hogy az egyszer kommentelők között szignifikánsan több a támogató komment, mint a többi csoportban, és érdekes, hogy a sokat (min 4.) kommentelők között többségben vannak a semleges állásponton lévők, illetve az ellenzők. Az ellenzők csak itt vannak többen, mint a támoagtók. Valószínűleg a nagyobb elkötelezettségük miatt kommenteltek többet.

![Kilencedik ábra](https://github.com/agatity/dera_park_analysis/blob/main/charts/User_Engagement_Segmentation.png)

👉 Itt fontos megjegyeznem, hogy a beruházó képviselője – nyilvánvalóan – a legtöbbet kommentelők között van, de nagyon visszafogott stílussal nyilvánult meg, azaz az ő kommentjei valószínűleg a semlegesek között vannak inkább. De ez az adatokon nem látszik, az adat nem minden!

### ℹ️ Amit én leszűrtem ℹ️
Számomra egyértelműen kiderült, hogy többségben vannak Szentendrén azok, akik örülnek egy ilyen beruházásnak – ezt sejtettem is –, de egyáltalán nem elhanyagolható kisebbségi álláspont az, hogy egy bevásárlóközpont zöldmezős beruházásként nem a jó irány. Ez volt nekem a legfőbb meglepetés. Nagyságrendileg bizony összehasonlítható a két sokaság: azaz az ellenzők és a támogatók aránya. Az arányok miatt talán akkor fogalmazok jól, ha azt írom, hogy a közel 30 ezres városunk megosztott ebben a kérdésben. 
Az én nézőpontomból – én sem örülök egy ilyen bevásárlóközpontnak – ez bizony örömhír.

 ## 🟩Hadd írjak még pár továbbgondolni valót! 🟩
*"Oké, oké, nem örülsz egy ilyen projektnek, akkor mit kéne csinálni, te pupák?"*
* Szerintem tök jó lenne eljutni odáig, hogy már csak barnamezős beruházásokat lehessen itthon csinálni, azaz a zöldfelület kárára maximum csak létfontosságú beruházásokat lehessen építeni. Tudom, az akkugyárak országában ez utópiának tűnhet, de én azért itt hagyom ezt a gondolatot. Szerintem minden döntéshozónak ilyen irányba kéne gondolkodnia, e felé kéne mennie!
* Szentendrén nagyon sok olyan terület van, ami baromi rég ki van már szabályozva ipari, gazdasági területnek, és a tulajdonosa oda bármikor felhúzhat valamit: egy csarnokot, egy üzemet, logisztikai bázist, bevásárlóközpontot, akármit. Attól tartok, hogy a szentendreiek ezekről mit sem sejtenek, az önkormányzat pedig nem rakja ki köuérthetően, mondjuk kataszter-szerűen, hogy "no, nézzétek, ennyi és ennyi terület van kiszabályozva, de még beépítetlenül". Ezért minden egyes építkezéskor sokan meglepődnek, hogy "már megint mi épül itt?" Lehet, hogy ha már az önkormányzat nem mutatja ezt be, érdemes lenne adatigénylések sorával és geoadatbázis segítségével önkéntes munkával csinálni egy nyilvános szentendrei térképet.
* Ez a poszt a legkevésbé sem a (tulajdonos)-vállalkozóról szól! Ő csinál valamit, vállalkozik, kockáztat egy olyan területen, amin a lehetőség már régóta adott.
* A poszt végső soron rólunk szól! Ugyanis a sok-sok régi és mostani döntésünk – a mi döntéseink, a korábbi generációké, tervezők, döntéshozók, szüleink, nagyszüleink döntései, végső soron a mi, emberek, szentendreiek, magyarok döntései – mégiscsak előállított egy olyan helyzetet, ahol folyamatosan csökkennek a zöldterületek, és a kisvárosaink elvesztik a jellegüket.

______

## Ha idáig eljutottál:
- a teljes Python kódsor az anonimizált adatbázissal itt van a [Githubon](https://github.com/agatity/dera_park_analysis/)
- az eredeti poszt pedig itt olvasható a Szentendre Blogol [FB-csoportban](https://www.facebook.com/groups/szteblogol/posts/7220377584650331/)
- az én Facebook-posztom [itt olvasható](https://www.facebook.com/aron.kubatovics/posts/pfbid02QGJe1zQU6dF4p4KyLxhaizJmPQEfWB7C94VFKGGjBdhzqybEpnoNqznskLesBKRjl)
- és felraktam [LinkedIn-re](https://www.linkedin.com/posts/kubatovics_a-data36com-nak-aj%C3%A1nlom-ezt-a-posztomat-activity-7257468509595586560-b1R0?utm_source=share&utm_medium=member_desktop) is

📷 Látványterv: Dera-park (Facebook)
