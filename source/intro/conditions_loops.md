# Uvjeti i petlje

Za uspješno svladavanje materijala u sljedećoj lekciji potrebno je poznavati
osnovne činjenice o radu s uvjetima i petljama.

## Uvjeti

U većini modernih programskih jezika uvjetni iskazi koriste se za donošenje
odluka i upravljanje tokom programa. Najčešće konstrukcije su:

* if
* if-else
* switch-case

Iako se sintaksa razlikuje između jezika, osnovna logika je ista.

### Naredba `if`

Naredba `if` izvršava blok koda samo ako je zadani uvjet
istinit.

```text
if uvjet then
    naredba(e)
```

Na primjer, u C, C++, C# i Javi, ako želite provjeriti je li `x` veće od
`0`, uvjetni iskaz može se napisati ovako:

```csharp
int x = 5;
if (x > 0) {
    // ...
}
```

### Naredba `if-else`

Naredba if-else izvršava jedan blok koda ako je uvjet istinit, a
drugi blok ako je neistinit.

```text
if uvjet then
    naredba(e)
else
    naredba(e)
```

Na primjer, u C, C++, C# i Javi, ako želite provjeriti je li `x` veće od
`0` ili nije veće od `0`, uvjetni iskaz može se napisati ovako:

```csharp
int x = 5;
if (x > 0) {
    // ...
} else {
    // ...
}
```

### Naredba `switch-case`

Naredba `switch-case` korisna je kada uspoređujete istu varijablu s
mnogo mogućih vrijednosti. Može biti čitljivija od korištenja mnogih naredbi
`if-else`.

```text
switch expression do
    case vrijednost1:
        naredba(e)
    case vrijednost2:
        naredba(e)
    ...
    default:
        naredba(e)
```

Na primjer, u C, C++, C# i Javi, ako želite odrediti naziv dana
na temelju rednog broja u tjednu, uvjetni iskaz može se napisati ovako:

```csharp
int day = 3;
string name = "";
switch (day) {
    case 1:
        name = "Monday";
        break;
    case 2:
        name = "Tuesday";
        break;
    case 3:
        name = "Wednesday";
        break;
    // ...
    default:
        name = "";
        break;
}
```

### Ugniježđivanje uvjeta

Uvjetni iskazi mogu se postavljati unutar drugih uvjetnih iskaza — to se
naziva **ugniježđivanje**. Ugniježđeni uvjeti korisni su kada odluka ovisi o
rezultatu prethodne odluke. Na primjer, možete prvo provjeriti je li korisnik
prijavljen, a zatim unutar tog bloka provjeriti ima li dopuštenje za
izvođenje određene radnje.

## Petlje

U većini modernih programskih jezika petlje se obično implementiraju pomoću jedne
od sljedećih konstrukcija:

* `for`,
* `while` (ili `while-do`),
* `do-while` (ili `repeat-until`),
* `foreach` (ili `for-each`).

Iako se sintaksa razlikuje između jezika, osnovna logika je ista.

### Petlja `for`

Petlja `for` koristi se kada je broj ponavljanja konačan i
unaprijed poznat.

```text
for varijabla ← početak to kraj do
    naredba(e)
```

Na primjer, u C, C++, C# i Javi, petlja `for` za iteraciju kroz brojeve
od 0 do 9 može se napisati ovako:

```csharp
for (int i = 0; i <= 9; i++) {
    // ...
}
```

### Petlja `while`

Petlja `while` (ili `while-do`) koristi se kada broj ponavljanja nije
unaprijed poznat. Uvjet se provjerava prije svake iteracije, pa se
to naziva **petlja s preduvjetom**.

```text
while uvjet do
    naredba(e)
```

Na primjer, u C, C++, C# i Javi, petlja `while` za iteraciju kroz brojeve
od 0 do 9 može se napisati ovako:

```csharp
int i = 0;
while (i <= 9) {
    // ...
    i++;
}
```

### Petlja `do-while`

Petlja `do-while` (ili `repeat-until`) također podržava nepoznat broj
ponavljanja, ali se uvjet provjerava nakon svake iteracije. To se naziva
**petlja s postuvjetom** i uvijek se izvršava barem jednom.

```text
repeat
    naredba(e)
until uvjet
```

Na primjer, u C, C++, C# i Javi, petlja `do-while` za iteraciju kroz
brojeve od 0 do 9 može se napisati ovako:

```csharp
int i = 0;
do {
    // ...
    i++;
} while (i <= 9);
```

### Petlja `foreach`

Petlja `foreach` (ili `for-each`) koristi se za iteraciju po svim elementima
kolekcije ili polja. Pojednostavljuje iteraciju kada ne trebate znati indeks.

```text
for-each element in kolekcija do
    naredba(e)
```

Na primjer, petlja `for-each` za iteraciju kroz polje `nums` može se napisati
u C++ ovako:

```cpp
int nums[] = { 0, 1, 2, 3, 4, 5, 6, 7, 8, 9 };
for (int i : nums) {
    // ...
}
```

...ili u C# ovako...

```csharp
int[] nums = { 0, 1, 2, 3, 4, 5, 6, 7, 8, 9 };
foreach (int i in nums) {
    // ...
}  
```

...ili u Javi ovako:

```java
int[] nums = { 0, 1, 2, 3, 4, 5, 6, 7, 8, 9 };
for (int i : nums) {
    // ...
}   
```

### Ugniježđivanje petlji

Petlje se također mogu ugniježđivati, što znači da se jedna petlja postavlja unutar
druge. To je uobičajeno pri radu s višedimenzionalnim podacima, poput prolaska kroz
retke i stupce matrice ili iteracije po mreži u igri. Osim toga, petlje i
uvjeti mogu se slobodno kombinirati — na primjer, petlja može sadržavati naredbu `if`
za obradu samo određenih elemenata, ili naredba `if` može sadržavati petlju za
izvođenje ponavljajućih radnji kada je uvjet istinit. Ova mogućnost miješanja i
ugniježđivanja petlji i uvjeta omogućuje stvaranje složenih algoritama uz
zadržavanje strukturirane temeljne logike.
