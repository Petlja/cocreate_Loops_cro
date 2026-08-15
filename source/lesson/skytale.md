# Skital

Skital (engl. skytale) jedan je od najstarijih poznatih alata za šifriranje,
koji potječe iz antičke Grčke oko 400. godine prije nove ere. Bio je to
jednostavan cilindrični uređaj koji su Spartanci koristili za slanje tajnih
poruka tijekom vojnih pohoda.

Traka pergamenta ili kože omotavala se oko drvenog štapa (*skital*) određenog
promjera. Poruka se zatim pisala duž štapa. Kada se traka odmotala, slova su
izgledala razbacano i besmisleno. Primatelj je trebao štap **istog promjera**
kako bi omotao traku i pročitao originalnu poruku.

Ako želite šifrirati poruku:

```text
attackatdawn
```


i odaberete štap koji omogućuje **4 slova po okretaju**, najprije pišete
poruku vertikalno u stupcima, formirajući retke duljine 4:

```text
a t t a
c k a t
d a w n
```


Šifrirani tekst se zatim dobiva čitanjem po recima:

```text
acdtkatawatn
```


Za dešifriranje, primatelj ponovo omota traku oko štapa istog promjera i čita
vertikalno kako bi rekonstruirao originalnu poruku.


## Prvi zadatak

Napravite konzolnu aplikaciju u bilo kojem programskom jeziku koja će šifrirati
i dešifrirati poruke koristeći Skital šifru. Koristite razvojno okruženje koje
koristite na satovima programiranja.

Dopuštena abeceda za poruke sadrži samo mala slova engleske abecede:

```text
Σ = { a, b, c, d, e, f, g, h, i, j, k, l, m, n, o, p, q, r, s, t, u, v, w, x, y, z }
```


Razmaci, velika slova, brojevi i drugi znakovi nisu dopušteni!


U prvom retku korisničkog unosa nalazit će se poruka `m` duljine do sto znakova.
U drugom retku nalazit će se cijeli broj `k` (broj stupaca – opseg štapa). U
trećem retku nalazit će se cijeli broj `s` koji predstavlja operaciju. Ako je
$s=1$, tada `m` treba biti šifrirano. Ako je $s=2$, tada `m` treba biti dešifrirano.


### Test primjer 1

Ako je unos:

```text
attackatdawn
4
1
```


izlaz bi trebao biti:

```text
acdtkatawatn
```


### Test primjer 2

Ako je unos:

```text
acdtkatawatn
4
2
```


izlaz bi trebao biti:

```text
attackatdawn
```

## Savjeti za rješenje

Za **šifriranje**, zapišite otvoreni tekst vertikalno u tablicu s `k` stupaca.
Čitajte tablicu po recima kako biste formirali šifrirani tekst. Za
**dešifriranje**, zapišite šifrirani tekst po recima u tablicu s `k` stupaca,
a zatim čitajte tablicu vertikalno kako biste rekonstruirali otvoreni tekst.


## Napredni zadaci s Skital šifrom (opcionalno)

### Proširite dopuštenu abecedu

Uključite velika slova, razmake, brojeve i interpunkciju.

### Koristite funkcije

Napravite funkcije `encrypt()` i `decrypt()` kako bi kod bio modularan.

### Napravite klasu

Implementirajte klasu `SkytaleCipher` koja pohranjuje `k` i pruža metode za
šifriranje i dešifriranje.

### Šifrirajte i dešifrirajte datoteke

Izmijenite program tako da čita otvoreni tekst ili šifrirani tekst iz datoteke
i rezultate zapisuje u drugu datoteku.

### Rukujte nepotpunim recima

Izmijenite program tako da, ako je posljednji redak kraći od `k`, ispravno
šifrira i dešifrira rukujući nedostajućim znakovima ili dopunjavanjem.
