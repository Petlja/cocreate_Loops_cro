# Skitala

Skitala je jedan od najstarijih poznatih sredstava za šifriranje. Potječe iz stare Grčke, iz oko 400. godine pr. Kr. Bila je to jednostavna cilindrična naprava koju su Spartanci upotrebljavali za slanje tajnih poruka tijekom vojnih pohoda.

Traka od pergamenta ili kože namotala se oko drvenog štapa (*skitala*) određena promjera. Poruka se zatim pisala uzduž namotane trake. Za dešifriranje je primatelj namotao traku oko štapa istog promjera i čitao poruku uzduž, na isti način na koji je bila napisana.

Ako želite šifrirati poruku:

```text
attackatdawn
```

a odaberete štap na koji stane **3 slova po namotu**, traka se oko njega namotava 4 puta. Poruku pišete uz štap, redak po redak, po 4 slova u svakom retku (jedno na svakom namotu), čime se dobiva tablica:

```text
a t t a
c k a t
d a w n
```

Šifrirani tekst zatim se dobiva čitanjem stupac po stupac (to je redoslijed slova na odmotanoj traci):

```text
acdtkatawatn
```

Za dešifriranje poruke primatelj namotava traku oko štapa istog promjera i ponovno čita redak po redak kako bi obnovio izvornu poruku.

## Prvi zadatak

Napravite konzolnu aplikaciju u bilo kojem programskom jeziku koja šifrira i dešifrira poruke pomoću šifre skitala.

Dopuštena abeceda za poruke sadrži samo mala slova engleske abecede:

```text
Σ = { a, b, c, d, e, f, g, h, i, j, k, l, m, n, o, p, q, r, s, t, u, v, w, x, y, z }
```

Razmaci, velika slova, brojevi i drugi znakovi nisu dopušteni!

U prvom retku ulaza nalazi se poruka `m` koja ima najviše sto znakova. U drugom retku nalazi se cijeli broj `k` (broj stupaca u tablici za šifriranje). U trećem retku nalazi se cijeli broj `s` (1 za šifriranje, 2 za dešifriranje).

### Primjer provjere 1

Ako je ulaz:

```text
attackatdawn
4
1
```

treba biti izlaz:

```text
acdtkatawatn
```

### Primjer provjere 2

Ako je ulaz:

```text
acdtkatawatn
4
2
```

treba biti izlaz:

```text
attackatdawn
```

## Savjeti za rješenje

Za **šifriranje** upišite otvoreni tekst redak po redak u tablicu s `k` stupaca. Pročitajte tablicu stupac po stupac kako biste dobili šifrirani tekst.

Za **dešifriranje** upišite šifrirani tekst stupac po stupac u tablicu s `k` stupaca (svaki stupac sadrži duljinu poruke podijeljenu s `k` slova), a zatim pročitajte tablicu redak po redak kako biste obnovili otvoreni tekst.

## Složeniji zadaci sa skitalom (izborno)

### Proširite dopuštenu abecedu

Uključite velika slova, razmake, brojeve i interpunkcijske znakove.

### Upotrijebite funkcije

Izradite funkcije `encrypt()` i `decrypt()` kako biste kod učinili modularnim.

### Izradite klasu

Izradite klasu `SkytaleCipher` koja sprema `k` i pruža metode za šifriranje i dešifriranje.

### Šifrirajte i dešifrirajte datoteke

Izmijenite program tako da čita otvoreni ili šifrirani tekst iz datoteke i rezultat zapisuje u drugu datoteku.

### Rukujte nepotpunim recima

Izmijenite program tako da, ako je zadnji redak kraći od `k`, ipak ispravno šifrira i dešifrira poruku te na odgovarajući način obrađuje nepotpune retke.
