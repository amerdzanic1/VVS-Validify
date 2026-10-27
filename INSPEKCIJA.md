Ručna inspekcija programskog koda – VVS

Projekat: LoanManagement (VVS-Validify)
Predmet: Verifikacija i validacija softvera
Metoda: Ručna inspekcija programskog koda
GitHub Pull Request: #1

1. Cilj inspekcije

Cilj inspekcije je identifikacija funkcionalnih, strukturnih i sigurnosnih defekata u programskom rješenju LoanManagement.

Inspekcija je organizovana u dva prolaza:

Prvi prolaz – funkcionalne greške i kvalitet koda (Predavanje 2).

Drugi prolaz – sigurnosni propusti (Predavanje 3).
## 2. Izvještaj o nalazima

| ID | Tip defekta | Datoteka / lokacija | Opis defekta | Ozbiljnost | GitHub Issue |
|---|---|---|---|---|---|
| S-01 | Sigurnost – generisanje tokena | Storage/Sesija.cs, linija 14 | Korištenje System.Random za generisanje sesijskog tokena, što nije kriptografski sigurno. | Visoka | #3 |
| S-02 | Sigurnost – unos lozinke | Program.cs, opcije 1 i 2 | Lozinka se unosi pomoću Console.ReadLine(), zbog čega su znakovi vidljivi tokom unosa. | Visoka | #2 |

## 3. Sumarni izvještaj

| Pokazatelj | Vrijednost |
|---|---|
| Pregledane datoteke u dosadašnjoj analizi | Program.cs, Storage/Sesija.cs |
| Broj dokumentovanih defekata | 2 |
| Broj sigurnosnih defekata | 2 |
| Broj funkcionalnih defekata | Nije konačno utvrđen |
| Broj GitHub Issue kartica | 2 |
| Broj učesnika | Unijeti nakon timskog pregleda |
| Trajanje inspekcije | Unijeti stvarno trajanje |
| Status inspekcije | Djelimično završena |

4. Odluke o naknadnoj provjeri

Pronađeni sigurnosni defekti evidentirani su kroz GitHub Issue kartice #2 i #3.

Preporučuje se implementacija sigurnog unosa lozinke i korištenje kriptografski sigurnog generatora slučajnih brojeva za sesijske tokene.

Nakon ispravki potrebno je izvršiti ponovnu provjeru navedenih dijelova programskog koda.

5. Zaključak

Dosadašnjom analizom datoteka Program.cs i Storage/Sesija.cs identificirana su dva sigurnosna defekta.

Za pronađene defekte kreirane su GitHub Issue kartice, a inspekcija je dokumentovana kroz izvještaj o nalazima i sumarni izvještaj.

Konačni izvještaj potrebno je dopuniti nakon završetka timskog pregleda kompletnog programskog rješenja u oba prolaza.
