# XOR

XOR *(Ekskluzivni ILI)* je logička operacija koja daje istinito (1) samo kada
se ulazi razlikuju. To je temeljna binarna operacija s važnim primjenama
u računarstvu i kriptografiji.

| A | B | A XOR B |
| - | - | :-----: |
| 0 | 0 | 0       |
| 0 | 1 | 1       |
| 1 | 0 | 1       |
| 1 | 1 | 0       |

Na primjer, za šifriranje riječi "HELLO" koristeći ključ "KEY", najprije
trebate pretvoriti `HELLO` u binarni zapis...

| Znak | ASCII | Binarno  |
| ---- | ----- | -------- |
| H    | 72    | 01001000 |
| E    | 69    | 01000101 |
| L    | 76    | 01001100 |
| L    | 76    | 01001100 |
| O    | 79    | 01001111 |

...zatim pretvoriti `KEY` u binarni zapis...

| Znak | ASCII | Binarno  |
| ---- | ----- | -------- |
| K    | 75    | 01001011 |
| E    | 69    | 01000101 |
| Y    | 89    | 01011001 |

...i konačno provesti šifriranje — XOR svaki znak s ključem, ponavljajući ključ
onoliko puta koliko je potrebno:

```text
H ⊕ K: 01001000 ⊕ 01001011 = 00000011 (ASCII 3)
E ⊕ E: 01000101 ⊕ 01000101 = 00000000 (ASCII 0)
L ⊕ Y: 01001100 ⊕ 01011001 = 00010101 (ASCII 21)
L ⊕ K: 01001100 ⊕ 01001011 = 00000111 (ASCII 7)
O ⊕ E: 01001111 ⊕ 01000101 = 00001010 (ASCII 10)
```

Dobiveni šifrirani tekst sastoji se od ASCII znakova koji se ne mogu ispisati s
decimalnim vrijednostima 3, 0, 21, 7 i 10. Ako bi napadač presreo ovu poruku,
vidio bi samo nečitljive binarne podatke, budući da znakovi nisu ispisivi.

Za dešifriranje šifriranog teksta trebate XOR-irati šifrirani tekst s istim ključem:

```text
3  ⊕ K: 00000011 ⊕ 01001011 = 01001000 (ASCII 72 → H)
0  ⊕ E: 00000000 ⊕ 01000101 = 01000101 (ASCII 69 → E)
21 ⊕ Y: 00010101 ⊕ 01011001 = 01001100 (ASCII 76 → L)
7  ⊕ K: 00000111 ⊕ 01001011 = 01001100 (ASCII 76 → L)
10 ⊕ E: 00001010 ⊕ 01000101 = 01001111 (ASCII 79 → O)
```

XOR operacija je samoinverzna — primjena XOR-a dva puta s istim ključem
vrača originalne podatke.

U stvarnim primjenama, ponovna upotreba istog ključa za više poruka čini
XOR šifriranje ranjivim na frekventnu analizu i napade poznatog otvorenog teksta.
XOR sam po sebi ne pruža jaku sigurnost osim ako se ključem pravilno upravlja
i nije kraći od poruke — kao kod jednokratne bilježnice. Međutim, u obrazovne
svrhe i za osnovna demonstriranja kriptografskih načela, XOR je jednostavan i idealan.

## Prvi zadatak

Napravi konzolnu aplikaciju u bilo kojem programskom jeziku koja će šifrirati i
dešifrirati poruke koristeći XOR operaciju. Koristi razvojno okruženje koje
koristite na satovima programiranja.

Dopuštena abeceda za poruke (otvoreni tekst i ključ) uključuje samo
mala slova engleske abecede:

```text
Σ = { a, b, c, d, e, f, g, h, i, j, k, l, m, n, o, p, q, r, s, t, u, v, w, x, y, z }
```

Razmaci, velika slova, brojevi i drugi znakovi nisu dopušteni.

U prvom retku korisničkog unosa bit će poruka `m` duljine do sto ASCII znakova
za otvoreni tekst ili 800 bita za šifrirani tekst, u drugom retku bit će ključ
`k` duljine do pet znakova, a u trećem retku bit će cijeli broj `s`, koji
predstavlja operaciju. Ako je $s=1$, tada je `m` otvoreni tekst i treba biti
šifriran, a ako je $s=2$, tada je `m` šifrirani tekst u binarnom obliku i treba
biti dešifriran.

### Test primjer 1

Ako je unos:

```text
nikolatesla
ser
1
```

izlaz bi trebao biti:

```text
0001110100001100000110010001110000001001000100110000011100000000000000010001111100000100
```

### Test primjer 2

Ako je unos:

```text
0001110100001100000110010001110000001001000100110000011100000000000000010001111100000100
ser
2
```

izlaz bi trebao biti:

```text
nikolatesla
```

## Uradi zadatak

[Implementirajte šifru ovdje](https://arena.petlja.org/sr-Latn-RS/competition/123-co-create#tab_142947)

## Savjeti za rješenje

Svaki znak pohranjen je u memoriji kao 8-bitna ASCII vrijednost (za mala slova
a–z, kodovi se kreću od 97 do 122). Za šifriranje znaka uzmite njegovu ASCII
vrijednost i ASCII vrijednost odgovarajućeg znaka ključa (ciklički prolazeći
kroz ključ), primijenite XOR (^) između njih i ispišite rezultat kao 8-bitni
binarni broj.

Za dešifriranje slijedite obrnuti postupak — uzmite svaki 8-bitni binarni blok
iz šifriranog teksta, pretvorite ga natrag u cijeli broj (0–255), XOR-irajte s
ASCII vrijednošću odgovarajućeg znaka ključa i pretvorite rezultat natrag u znak.

## Složeniji XOR zadaci (opcionalno)

### Proširite dopuštenu abecedu

Dopustite mala i velika slova, razmake, brojeve i interpunkciju.
Znakovi koji nisu slova XOR-iraju se s ključem na isti način.

## Koristite funkcije

Napravite dvije funkcije: `encrypt()` za šifriranje poruka i `decrypt()` za
dešifriranje poruka. Koristite kreirane funkcije u svom glavnom programu.

### Napravite klasu

Napravite klasu `XorCipher` koja:

* Pohranjuje ključ,
* Pruža metode `encrypt()` i `decrypt()`,
* Opcionalno uključuje privatnu pomoćnu metodu za ponavljanje ključa duž duljine poruke.

Koristite kreiranu klasu u svom glavnom programu.

### Prihvatite argumente naredbenog retka

Umjesto čekanja korisničkog unosa, napravite konzolnu aplikaciju koja
prihvaća sljedeće argumente naredbenog retka:

1. argument `m` za specificiranje poruke,
2. argument `k` za specificiranje ključa, i
3. argument `s` za specificiranje operacije (`1` za šifriranje, `2` za dešifriranje).

### Šifrirajte i dešifrirajte datoteke

Koristite znanje koje ste stekli do sada za izradu programa koji može:

* čitati otvoreni tekst ili binarni šifrirani tekst iz datoteke,
* šifrirati ili dešifrirati ga zadanim ključem, i
* zapisati rezultat u novu datoteku.
