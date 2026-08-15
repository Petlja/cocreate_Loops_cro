# Uvod u povijest kriptografije i važnost kriptografije u suvremenom svijetu

Već od davnina, otkada su ljudi počeli pisati, postojala je potreba da se neki
pisani tekst sakrije, odnosno zaštiti. Razvijanjem tehnika za skrivanje zapisanih
informacija, pojavilo se novo znanstveno područje – kriptografija.

> **Kriptografija** je znanstvena disciplina koja se bavi razvojem sustava za
> šifriranje informacija. Riječ kriptografija dolazi od grčkih riječi κρυπτός
> (*skriveno, tajno*) i γράφειν (*pisati*).

Prvu knjigu o kriptografiji, naslovljenu „Knjiga o šifriranim porukama", prema
povijesnim izvorima, napisao je arapski filozof Al-Halil (717.–786.), u kojoj
se po prvi put koriste permutacije i kombinacije za nabrajanje svih arapskih
riječi sa samoglasnicima i bez njih. Međutim, klasične metode šifriranja često
otkrivaju statističke uzorke o originalnoj poruci, koji se mogu iskoristiti za
razbijanje šifre.

Nakon otkrića frekventne analize slova u poruci, arapski matematičar Al-Kindi
napisao je u devetom stoljeću knjigu „Rukopis za dešifriranje šifriranih poruka",
u kojoj je po prvi put opisana upotreba tehnika frekventne analize.

> **Kriptoanaliza** je znanstvena disciplina koja proučava metode „razbijanja"
> kriptografskih sustava. Riječ kriptoanaliza dolazi od grčkih riječi κρυπτός
> (*skriveno, tajno*) i αναλύειν (*analizirati*).


Prvi poznati traktat o kriptografiji napisao je na 25 stranica talijanski
arhitekt Leone Battista Alberti 1467. godine. On je i tvorac šifarskog kruga
i drugih rješenja za dvoslojno skrivanje teksta. U 16. stoljeću značajne
doprinose dali su milanski liječnik Girolamo Cardano, matematičar Battista
Porta i francuski diplomat Blaise de Vigenere.


![Francuska šifarska naprava u obliku knjige iz 16. stoljeća](./images/cyphermachine.jpg)


U 19. stoljeću zaključeno je da kriptografija ne bi smjela ovisiti o tajnosti
algoritama šifriranja, već o tajnosti ključa. Tajnost samog ključa mora biti
dovoljna da spriječi razbijanje šifrirane poruke. To je postalo jedno od
temeljnih načela kriptografije, koje je 1883. zapisao Auguste Kerckhoffs
(Kerckhoffsovo načelo). Eksplicitnije, ponovio ga je Claude Shannon, osnivač
teorije informacija i ključna figura u teorijskoj kriptografiji, kao Shannonovu
maksimu: „neprijatelj poznaje sustav".


Tijekom Drugog svjetskog rata, Nijemci su izgradili stroj pod nazivom **Enigma**
koji je šifrirao poruke na do tada neviđen način. Međutim, koliko god je bio
revolucionaran u to vrijeme, saveznici predvođeni Alanom Turingom uspjeli su
razbiti kriptografski sustav Enigme kriptoanalizom.

![Enigma](./images/enigma.jpg)


## Sadašnjost

Nakon Drugog svjetskog rata, razvojem informacijskih tehnologija, kriptologija
kao znanost o zaštiti informacija, i njezine znanstvene poddiscipline postaju
sve važnije. Moderna računala mogu razbiti jednostavne šifre nevjerojatnom
brzinom, pa su kriptografski algoritmi postali mnogo napredniji.


Danas se u kriptografiji govori o **simetričnom** šifriranju, gdje se isti ključ
koristi i za šifriranje i za dešifriranje. Simetrično šifriranje je brže i
prikladnije za velike količine podataka. Koristi se kada je potrebno brzo
zaštititi podatke — npr. šifriranje datoteka na računalu, šifriranje komunikacije
tijekom videopoziva ili zaštita podataka na disku ili USB uređaju.

![Simetrično šifriranje](./images/symmetric.png)

S druge strane, kada je važno sigurno razmijeniti ključeve, dokazati tko je
poslao poruku ili potpisati dokument digitalnim potpisom, koristimo **asimetrično**
šifriranje, gdje se koristi par javnog i privatnog ključa:

![Asimetrično šifriranje](./images/asymmetric.png)


Još jedan važan alat je kriptografska hash funkcija, koja stvara jedinstveni
digitalni otisak podataka i široko se koristi u zaštiti lozinki, digitalnim
potpisima i blockchain tehnologiji.


## Budućnost

Gledajući unaprijed, očekuje se da će kvantna kriptografija postati temelj
sigurne komunikacije. Temelji se na Heisenbergovom načelu neodređenosti u
kvantnoj fizici. Međutim, kvantno računarstvo predstavlja i prijetnju mnogim
kriptografskim algoritmima koji se danas koriste, što je dovelo do razvoja
postkvanme kriptografije.

![Google Quantum AI](./images/google.jpg)

Važnost kriptologije u suvremenom društvu nemjerljiva je. Kriptografski sustavi
osiguravaju privatnost elektroničke komunikacije, omogućuju sigurnu elektroničku
trgovinu, štite kriptovalute, a u nekim državama čak osiguravaju elektroničko
glasovanje i brojanje glasova. Ipak, otvaraju se i brojna etička pitanja. Da
bismo odgovorili na njih, pripremite se za raspravu!

## Rasprava

**Tema rasprave: Treba li pravo na privatnost biti važnije od sigurnosti društva?**

Podjela uloga

Tim A – Za jaku zaštitu privatnosti

Svaka osoba ima pravo na privatnu komunikaciju.
Šifriranje štiti građane od zlouporabe, krađe identiteta i nadzora.
Nitko, pa ni država, ne bi trebao imati pristup privatnim porukama.

Tim B – Za veću kontrolu radi sigurnosti

Potpuno šifriranje može pomoći kriminalcima i teroristima da sakriju svoje aktivnosti.
Sigurnosne službe ponekad moraju imati pristup komunikaciji radi zaštite građana.
Društvo mora pronaći ravnotežu između privatnosti i sigurnosti.

Razmatranje argumenata možete obaviti u grupama između dva sata ili na samom satu, a
zatim slijedi razmjena stajališta (svaka grupa ima 5 minuta da obrazloži svoje
stajalište). Ostali učenici — porota — potom postavljaju pitanja i obje grupe imaju
oko 10 minuta da odgovore.

Ocjenjivanje i određivanje pobjedničke grupe nije nužno, ali je poželjna zajednička
rasprava o svim iznesenim argumentima. Neka dodatna pitanja za raspravu mogu biti:
Treba li policija imati pravo pristupa šifriranim porukama osumnjičenih osoba?
Biste li pristali da se vaše poruke analiziraju ako bi to spriječilo teroristički napad?
Koji su rizici ako netko ima pristup svim našim podacima?
Jesu li društvene mreže dovoljno transparentne u pogledu podataka koje prikupljaju?
Jesu li mladi svjesni koliko osobnih podataka ostavljaju na internetu?
Je li lozinka dovoljna za zaštitu računa ili su potrebne dodatne mjere sigurnosti?
