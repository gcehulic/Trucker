Goran Čehulić
# Dijagram slijeda "Upravljanje zaposlenicima"
![Dijagram slijeda "Upravljanje zaposlenicima"](https://github.com/foivz/r16030/blob/master/dijagrami/dijagram_slijeda_zaposlenici.jpg)
Dijagram slijeda za „Upravljanje zaposlenicima“ nalazi se na slici iznad. Prije početka bilo kakve akcije administrator se prijavljuje u sustav.
* Dodavanje zaposlenika- Otvara se forma za dodavanje zaposlenika. Nakon što se popune podaci o novom zaposleniku , odnosno nakon što se popuni forma ti podaci se prosljeđuju u bazu nad kojom sustav izvršava upit kojim se upisuju podaci o zaposleniku. Ako je upit uspješno izvršen baza šalje potvrdu o unosu aplikaciji. Temeljem te potvrde aplikacija ispisuje korisniku poruku o unosu.
* Izmjena zaposlenika- Otvara se forma za izmjenu određenog  zaposlenika. Na toj formi izmjenimo podatke o zaposleniku koje želimo mijenjati. Ti novi podaci prosljeđuju se u bazu. Nad bazom se izvršava upit koji mijenja podatke u bazi. Potom baza šalje aplikaciji potvrdu o promjeni podataka, a temeljem te potvrde aplikacija ispisuje poruku o promjeni podataka.
* Birsanje zaposlenika- Nakon što se otvori forma za brisanje zaposlenika odabere se zaposlenik i taj odabir se prosljeđuje bazi. Izvršava se upit koji briše toga zaposlenika iz baze. O tome baza šalje potvrdu temeljem koje aplikacija ispisuje poruku o brisanju.
* Izvještaj o zaposlenicima- u formi za prikaz izvježtaja odabire se zaposlenik za kojeg želimo vidjeti izvještaj.  Temeljem tog odabira kreira se upit kojim se iz baze povuku podaci o zaposleniku. Ti podaci prosljeđuju se aplikaciji koja temeljem njih  popunjava izvještaj i ispisuje ga korisniku.

# Dijagram slijeda "Upravljanje kamionima"
![Dijagram slijeda "Upravljanje kamionima"](https://github.com/foivz/r16030/blob/master/dijagrami/dijagram_slijeda_kamioni.jpg)
Pošto su funkcionalnosti upravljanja kamionima jednake kao i funkcionalnosti za upravljanje zaposlenicima, dijagram slijeda za "Upravljanje kamionima" gotovo je jednak onome za "Upravljanje zaposlenicima".