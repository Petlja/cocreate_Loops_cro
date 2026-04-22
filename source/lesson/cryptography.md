# Vrlo kratki uvod u kriptografiju

Od davnine, od kada su ljudi počeli pisati, postojala je potreba da se neki
pisani tekst čuva u tajnosti. Osmišljavanjem tehnika za skrivanje zapisanih
informacija, nastalo je novo znanstveno područje – kriptografija.

> **Kriptografija** je znanstvena disciplina koja se bavi razvojem sustava za
> šifriranje informacija. Riječ kriptografija dolazi od grčkih riječi kryptós
> (*skriveno, tajno*) i graphein (*pisati*).

U Indiji, spisi stari 2000 godina govore o dvije vrste šifriranja – prva vrsta
temeljila se na zamjeni slova prema njihovim fonetskim odnosima, a druga na
kodiranoj abecedi uparivanjem slova i korištenjem uzajamnih slova. U Perziji,
današnjem Iranu, također su postojale dvije vrste šifriranja – prvo kraljevsko
pismo koristilo se za službenu prepisku unutar kraljevstva, a drugo za
komunikaciju s drugim državama.

Prva knjiga o kriptografiji, naslovljena "Knjiga kriptografskih poruka" prema
povijesnim izvorima, napisana je od strane arapskog filozofa Al-Khalila
(717.–786.), u kojoj se permutacije i kombinacije prvi put koriste za nabrajanje
svih arapskih riječi sa samoglasnicima i bez njih. Međutim, klasične metode
šifriranja često otkrivaju statističke uzorke o originalnoj poruci, koji se
mogu iskoristiti za razbijanje šifre.

![Al-Kindijev rukopis o dešifriranju kriptografskih poruka](./images/kindi.jpg)

Nakon otkrića frekventne analize slova u poruci, arapski matematičar Al-Kindi
napisao je u devetom stoljeću knjigu "Rukopis za dešifriranje kriptografskih
poruka", u kojoj je prvi put opisana upotreba tehnika frekventne analize.

> **Kriptoanaliza** je znanstvena disciplina koja proučava metode "razbijanja"
> kriptografskih sustava. Riječ kriptoanaliza dolazi od grčkih riječi kryptós
> (*skriveno, tajno*) i analýein (*analiza*).

Prvi poznati traktat o kriptografiji napisao je na 25 stranica talijanski
arhitekt Leone Battista Alberti 1467. godine. On je također tvorac šifarskog
kruga i drugih rješenja za dvostruko skrivanje teksta. Pola stoljeća kasnije,
objavljeno je djelo Johannesa Tritheimusa o kriptografiji u pet svezaka. U
16. stoljeću značajne doprinose dali su milanski liječnik Girolamo Cardano,
matematičar Battista Porta i francuski diplomat Blaise de Vigenere.

![Francuska šifarska naprava u obliku knjige iz 16. stoljeća](./images/cyphermachine.jpg)

U 19. stoljeću zaključeno je da kriptografija ne bi smjela ovisiti o tajnosti
algoritama šifriranja, već o tajnosti ključa. Tajnost samog ključa mora biti
dovoljna da spriječi razbijanje šifrirane poruke. To je postalo jedno od
temeljnih načela kriptografije, zapisano 1883. godine od strane Augustea
Kerckhoffsa (Kerckhoffsovo načelo). Eksplicitnije, ponovio ga je Claude Shannon,
osnivač teorije informacija i ključna figura u teorijskoj kriptografiji, kao
Shannonovu maksimu: "neprijatelj poznaje sustav".

Tijekom Drugog svjetskog rata, Nijemci su izgradili stroj pod nazivom Enigma koji
je šifrirao poruke na do tada neviđen način. Međutim, koliko god je bio
revolucionaran u to vrijeme, saveznici, predvođeni Alanom Turingom, uspjeli su
razbiti kriptografski sustav Enigme putem kriptoanalize.

![Enigma](./images/enigma.jpg)

Kriptografija i kriptoanaliza dvije su glavne discipline kriptologije.

> **Kriptologija** je znanost koja se bavi različitim aspektima sigurnosti
> informacija. Riječ kriptologija dolazi od grčkih riječi kryptós (*skriveno,
> tajno*) i logos (*znanost*).

## Sadašnjost

Nakon Drugog svjetskog rata, razvojem informacijske tehnologije, kriptologija
i njezine znanstvene discipline postale su sve važnije. Moderna računala mogu
razbiti jednostavne šifre nevjerojatnom brzinom, pa su kriptografski algoritmi
postali mnogo napredniji. Danas se kriptografija općenito dijeli na
**simetričnu** enkripciju, gdje se isti ključ koristi za šifriranje i
dešifriranje...

![Simetrična enkripcija](./images/symmetric.png)

...i **asimetričnu** enkripciju, gdje se koristi par javnog i privatnog ključa:

![Asimetrična enkripcija](./images/asymmetric.png)

Još jedan esencijalni alat je kriptografska hash funkcija, koja stvara jedinstveni
digitalni otisak podataka i široko se koristi u zaštiti lozinki, digitalnim
potpisima i blockchain tehnologiji.

## Budućnost

Gledajući unaprijed, očekuje se da će kvantna kriptografija postati temelj
sigurne komunikacije. Temelji se na Heisenbergovom načelu neodređenosti kvantne
fizike. Međutim, kvantno računarstvo također predstavlja prijetnju mnogim
kriptografskim algoritmima koji se danas koriste, što je dovelo do razvoja
postkvanme kriptografije.

![Google Quantum AI](./images/google.jpg)

Važnost kriptologije u modernom društvu ne može se dovoljno naglasiti.
Kriptografski sustavi osiguravaju privatnost elektroničke komunikacije,
omogućuju sigurnu e-trgovinu, štite kriptovalute, a u nekim zemljama čak
štite elektroničko glasovanje i brojanje glasova.
