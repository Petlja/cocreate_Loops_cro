# Uvod u povijest kriptografije i važnost kriptografije u suvremenom svijetu

Još od davnina, kada su ljudi počeli pisati, postojala je potreba da se neki
pisani tekst sačuva u tajnosti. Razvijanjem tehnika za skrivanje zabilježenih
informacija, pojavilo se novo znanstveno područje – kriptografija.

> **Kriptografija** je znanstvena disciplina koja se bavi razvojem sustava za
> šifriranje informacija. Riječ kriptografija dolazi od grčkih riječi κρυπτός
> (*skriveno, tajno*) i γράφειν (*pisati*).

Prvu knjigu o kriptografiji, pod naslovom "Knjiga kriptografskih poruka", prema
povijesnim izvorima, napisao je arapski filozof Al-Khalil (717.–786.), u kojoj
se permutacije i kombinacije prvi put koriste za nabrajanje svih arapskih
riječi sa samoglasnicima i bez njih. Međutim, klasične metode šifriranja često
otkrivaju statističke uzorke o originalnoj poruci, koji se mogu iskoristiti
za razbijanje šifre.

Nakon otkrića frekventne analize slova u poruci, arapski matematičar Al-Kindi
napisao je u devetom stoljeću knjigu „Rukopis za dešifriranje šifriranih poruka",
u kojoj je po prvi put opisana upotreba tehnika frekventne analize.

> **Kriptoanaliza** je znanstvena disciplina koja proučava metode „razbijanja"
> kriptografskih sustava. Riječ kriptoanaliza dolazi od grčkih riječi κρυπτός
> (*skriveno, tajno*) i αναλύειν (*analizirati*).

> **Kriptoanaliza** je znanstvena disciplina koja proučava metode "razbijanja"
> kriptografskih sustava. Riječ kriptoanaliza dolazi od grčkih riječi κρυπτός
> (*skriveno, tajno*) i αναλύειν (*analiza*).

Prvi poznati traktat o kriptografiji napisao je na 25 stranica talijanski
arhitekt Leone Battista Alberti 1467. godine. On je također tvorac šifarskog
kruga i drugih rješenja za dvostruko skrivanje teksta. U 16. stoljeću značajne
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

Tijekom Drugog svjetskog rata, Nijemci su izgradili stroj pod nazivom **Enigma** koji
je šifrirao poruke na do tada neviđen način. Međutim, koliko god je bio
revolucionaran u to vrijeme, saveznici, predvođeni Alanom Turingom, uspjeli su
razbiti kriptografski sustav Enigme putem kriptoanalize.

Tijekom Drugog svjetskog rata, Nijemci su izgradili stroj pod nazivom **Enigma**
koji je šifrirao poruke na do tada neviđen način. Međutim, koliko god je bio
revolucionaran u to vrijeme, saveznici predvođeni Alanom Turingom uspjeli su
razbiti kriptografski sustav Enigme kriptoanalizom.

## Sadašnjost

Nakon Drugog svjetskog rata, razvojem informacijske tehnologije, kriptologija
i njezine znanstvene discipline postale su sve važnije. Moderna računala mogu
razbiti jednostavne šifre nevjerojatnom brzinom, pa su kriptografski algoritmi
postali mnogo napredniji.

Danas se u kriptografiji govori o **simetričnoj** enkripciji, gdje se isti ključ
koristi i za šifriranje i za dešifriranje. Simetrična enkripcija brža je i
prikladnija za velike količine podataka. Koristi se kada treba brzo zaštititi
podatke — npr. šifriranje datoteka na računalu, šifriranje komunikacije tijekom
videopoziva ili zaštita podataka na disku ili USB uređaju.

S druge strane, kada je važno sigurno razmijeniti ključeve, dokazati tko je
poslao poruku ili potpisati dokument digitalnim potpisom, koristimo **asimetrično**
šifriranje, gdje se koristi par javnog i privatnog ključa:

S druge strane, kada je važno sigurno razmijeniti ključeve, dokazati tko je
poslao poruku ili potpisati dokument digitalnim potpisom, koristimo
**asimetričnu** enkripciju, gdje se koristi par javnog i privatnog ključa:


Još jedan važan alat je kriptografska hash funkcija, koja stvara jedinstveni
digitalni otisak podataka i široko se koristi u zaštiti lozinki, digitalnim
potpisima i blockchain tehnologiji.


## Budućnost

Gledajući unaprijed, očekuje se da će kvantna kriptografija postati temelj
sigurne komunikacije. Temelji se na Heisenbergovom načelu neodređenosti u
kvantnoj fizici. Međutim, kvantno računarstvo predstavlja i prijetnju mnogim
kriptografskim algoritmima koji se danas koriste, što je dovelo do razvoja
postkvantne kriptografije.

![Google Quantum AI](./images/google.jpg)

Važnost kriptologije u modernom društvu ne može se dovoljno naglasiti.
Kriptografski sustavi osiguravaju privatnost elektroničke komunikacije,
omogućuju sigurnu e-trgovinu, štite kriptovalute, a u nekim zemljama čak
štite elektroničko glasovanje i brojanje glasova. Ipak, otvaraju se i brojna
etička pitanja. Kako bismo odgovorili na njih, pripremite se za debatu!

## Debata

**Tema debate: Treba li pravo na privatnost biti važnije od sigurnosti društva?**

Podjela uloga

Tim A – Za snažnu zaštitu privatnosti

Svaka osoba ima pravo na privatnu komunikaciju.
Šifriranje štiti građane od zlouporabe, krađe identiteta i nadzora.
Nitko, pa ni država, ne bi trebao imati pristup privatnim porukama.

Tim B – Za veću kontrolu radi sigurnosti

Potpuno šifriranje može pomoći kriminalcima i teroristima da sakriju svoje aktivnosti.
Sigurnosne službe ponekad moraju imati pristup komunikaciji radi zaštite građana.
Društvo mora pronaći ravnotežu između privatnosti i sigurnosti.

Razmatranje argumenata možete obaviti u skupinama između dva sata ili na samom satu. Potom slijedi razmjena stajališta — svaka skupina ima 5 minuta za obrazlaganje svog stajališta. Ostali učenici — porota — potom postavljaju pitanja, a obje skupine imaju 10-ak minuta za odgovaranje.

Ocjenjivanje i određivanje pobjedničke skupine nije nužno, ali jest poželjna zajednička diskusija o svim iznesenim argumentima. Neka dodatna pitanja za diskusiju mogu biti:

- Treba li policija imati pravo pristupa šifriranim porukama osumnjičenih osoba?
- Biste li pristali da se vaše poruke analiziraju ako bi to spriječilo teroristički napad?
- Koji su rizici ako netko ima pristup svim našim podacima?
- Jesu li društvene mreže dovoljno transparentne u pogledu podataka koje prikupljaju?
- Jesu li mladi svjesni koliko osobnih podataka ostavljaju na internetu?
- Je li lozinka dovoljna za zaštitu računa ili su potrebne dodatne mjere sigurnosti?
