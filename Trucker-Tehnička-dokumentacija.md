# Korisnički zahtjevi
* Profil kamiona (unos, izmjena i brisanje) - Mia Tomašević
* Profil zaposlenika (unos, izmjena i brisanje) - Mia Tomašević
* Dodavanje putovanja - Goran Čehulić
* Definiranje rute i prikaz na mapama uz mogućnost pohrane trajanja i duljine izabrane rute – Goran Čehulić
* Izrada troškovnika putovanja - Goran Čehulić
* Izrada izvješća o radu zaposlenika - Danijel Jurinjak
* Izrada izvješća o stanju i troškovima kamiona - Danijel Jurinjak
* Automatsko generiranje izvještaja o kamionima i zaposlenicima – Mia Tomašević
* Kreiranje i ispis računa za obavljenu uslugu – Danijel Jurinjak


##Specifikacija projekta
Aplikacija „Trucker“ imat će dvije vrste korisnika, administratora i običnog korisnika. Administratorski tip korisnika namijenili smo vlasniku poduzeća dok je obični korisnički tim namijenjen zaposlenicima poduzeća.
* **Administrator**- ima sve mogućnosti korištenja aplikacije poput uređivanja podataka o zaposlenicima, kamionima, putovanjima, te uvid u izvještaje o svakoj navedenoj kategoriji.
* **Obični korisnik**- može koristiti dio aplikacije koji se odnosi isključivo na putovanja. Može pogledati putovanja koja slijede, traju te dodati novo. Ovaj korisnik nema mogućnost uvida u administraciju kao ni dodavanje ili izmjene resursa (kamiona, zaposlenika i sl.).



Funkcionalnosti koje će imati ova aplikacija podijelili smo u tri skupine:
* **Zaposlenici** - Unutar ove skupine omogućeno je unositi nove, mijenjati podatke o starim i brisati postojeće zaposlenike. Omogućen je ispis izvještaja o zaposlenicima.
* **Kamioni** - Unutar ove skupine omogućen je unos, izmjena i brisanje kamiona u vlasništvu poduzeća. Također, omogućeno je kreiranje izvještaja o kamionima.
* **Putovanja** - Ovdje je sadržana mogućnost dodavanja putovanja. Definiranjem  polazišta i odredišta temeljem sustava GoogleMaps aplikacija će predložiti nekoliko ruta putovanja. Nakon što korisnik odabere rutu koja mu najviše odgovara ta ruta će se prikazati na karti te će se ispisati detalji o toj ruti (trajanje, duljina...). Ti podaci koriste se za izradu putnih računa i troškovnika.

##Specifikacija zahtjeva software-a (SRS)

### Uvod
Software je razvijen u obliku Windows Forms korisničke aplikacije. Aplikacija je namjenjena isključivo za upotrebu na računalu. Temeljna svrha aplikacije je omogućiti lakše i brže vođenje poslovanja manjih autoprijevozničkih poduzeća.

### Opis
Aplikacija ima dva pogleda, korisnički i administratorski. U korisničkom pogledu moguće je koristiti isključivo dio aplikacije koji je namjenjen za upravljanje putovanjima. Dio o administraciji i resursima dostupan je samo u administratorskom modu.
* **Aplikacija ima sljedeće mogućnosti:**
*  Prijava korisnika- kako bi bilo moguće korištenje aplikacije potrebno se prijaviti u sustav. Temeljem ovlasti koja je dodjeljena prijavljenom korisniku otvara se glavni izbornik u nekom od pogleda.
*  Upravljanje zaposlenicima- omogućen unos izmjena i brisanje zaposlenika. Moguće je generirati izvještaj o angažmanu zaposlenika tokom određenog perioda.
* Upravljanje kamionima- omogućen unos izmjena i brisanje kamiona. Moguće je generirati izvještaj o stanju kamiona i korištenju tokom nekog perioda.
*  Upravljanje putovanjima- omogućen je unos novog putovanja, uvid u sva putovanja, brisanje i izmjena statusa nekog od putovanja. Omogućeno je i dodavanje nove rute, brisanje postojeće i uvid u detalje unesenih ruta. Rutu je moguće prikazati u sustavu GooglMaps. Korisnik može upisti podatke o ruti poput trajanja i duljine te ih pohraniti.
* Administracija- Kreiranje prikaz i brisanje troškovnika i računa. Svako izvješće moguće je preuzeti kao pdf dokument. Omogućeno je upravljane popisom stavki koje su u sustavu.
* Pristup korisničkoj dokumentaciji koja je ujedno i "Help dokument" pritiskom na tipku f1. Ona se otvara kao zasebni pdf dokument.

###Zahtjevi za rad aplikacije
Za ispravan rad aplikacije potrebno je aplikaciju instalirati na računalo s upravljačkim sustavom Windows 7 i noviji. Također je potrebno osigurati pristup internetu zbog baze podataka koja se nalazi na udaljenom poslužitelju. Zbog prikaza karte potrebno je imati instaliran web preglednik.




## Razvoj projekta

![Vodopadni_model](https://github.com/foivz/r16030/blob/99ec2114862b5e93b11aadcf02beab60c6c16951/dijagrami/Vodopadni_model.png)

Prilikom razvoja ovog projekta odlučili smo se odabrati vodopadnu metodu jer ju smatramo najprimjerenijom budući da nam je ovo prvi ozbiljniji projekt. Razvoj vodopadnog modela odvija se kroz niz faza, počevši od analize i zahtjeva pa sve do primjene i isporuke. Napredak se odvija kroz niz faza i to na način da se prelazi s jedne faze u drugu, s napomenom da svaka faza započinje kad se prethodna završi. Na kraju svake faze obavezno se provjerava da li su svi zadaci uspješno i korektno obavljeni te da li projekt ide dobrim smjerom ili treba obustaviti prelazak u sljedeću fazu te ispraviti pogreške. Ukoliko ćemo se pridržavati navedenih faza trebali bismo uspješno realizirati projekt od početka do kraja, a rezultat toga bi bila aplikacija koja će uspješno ispunjavati zadatke koji se stave pred nju.
***

# Korištene tehnologije
* **Visual Studio 2015 (C#)**
Microsoft platforma za razvoj Windows, Android, iOS i Web aplikacija.
* **MS SQL**
Alat za izradu baze podataka.
* **Visual Paradigm**
Alat za Izradu dijagrama. Koristit ćemo ga za izradu dijagrama aktivnosti, slijeda i klasa te ERA modela.
* **MS Project**
Alat za izradu projektnog plana i vođenje projekta.
* **GitHub**
Sustav za verzioniranje koda i projektne dokumentacije.


# Dijagram slučajeva korištenja
![Use Case dijagram aplikacije](https://github.com/foivz/r16030/blob/master/dijagrami/Use%20Case%20Diagram%20Trucker.jpg)
Na slici iznad prikazan je UseCase dijagram aplikacije. Autentifikacijom korisnika, korisnike aplikacije separiramo u dvije skupine. Vlasnik poduzeća je administrator i on može koristiti sve funkcionalnosti aplikacije. Zaposlenik može koristiti samo funkcionalnosti koje se odnose na upravljanje putovanjima.
Pregledati putovanja otvara mogućnost upravljanja putovanjima. Upravljanje putovanjima podrazumijeva unos i brisanje putovanja. Za svako putovanje moguće je prikazati njegovu rutu. Pregledati putovanje uključuje upravljanje statusom putovanja. 
Pregledati zaposlenike omogućuje upravljanje zaposlenicima(unos, izmjenu i brisanje) i prikaz izvještaja s popisom zaposlenika.
Pregledati kamione omogućuje upravljanje kamionima(unos, izmjenu i brisanje) i prikaz izvještaja s popisom kamiona.
Pregledati troškovnik omogućuje pregled troškovnika za putovanje. Pruža mogućnost upravljanja troškovnicima(unos i brisanje) te preuzimanje troškovnika u pdf formatu.

# Dijagram klasa
![Dijagram klasa]
(https://github.com/foivz/r16030/blob/master/dijagrami/DijagramKlasa.PNG)

Za izradu našeg programskog rješenja koristit ćemo iznad navedeni dijagram klasa.

# Model podataka
![ERA model](https://github.com/foivz/r16030/blob/master/dijagrami/era.jpg)
Na slici iznad možete vidjeti ERA model podataka. On sadrži ukupno četrnaest entiteta, tri slaba i jedanaest jakih. Slabi entiteti su : Stavke_racuna, Stavke_troskovnika, Putovanje_zaposlenik. Svaki zaposlenik ima jednu skupinu ovlasti, a neka skupina ovlasti moze pripadati više zaposlenika. U istom odnosu su putovanje i ruta. Neko putovanje može imati 0 ili više troškovnika, dok troškovnik pripada samo jednom putovanju. Troškovnik može sadržavati više stavaka. Situacija sa stavkama je ista i kod računa. Stavke_racuna odnosno Stavke_troskovnika sadrže atribut cijena, pošto je stavkama poput cestarine, goriva i sl. nemoguće definirati fiksnu cijenu. Što se tiče zaposlenika na putovanju, na jedno putovanje može ići više zaposlenika.

# Dijagrami aktivnosti

## Dijagram aktivnosti "Prijava korisnika"
Goran Čehulić
![Dijagram aktivnosti za prijavu korisnika](https://github.com/foivz/r16030/blob/master/dijagrami/Log_in.jpg)
Korisnik pokrene aplikaciju. Potom se inicijalizira i otvara forma za prijavu korisnika. Korisnik unosi korisničko ime i lozinku. Potom slijedi provjera podataka. Iz baze se dohvaćaju podaci o korisnicima i uspoređuju s unesenima. Ako provjera podataka pokaže da su podaci ispravni otvara se glavna forma. Ako nisu onda se vraća na ponovni unos. Korisnik prilikom unosa može odustati od unosa i tada se aplikacija zatvara.

## Dijagram aktivnosti "Dodavanje putovanja"
Goran Čehulić
![Dijagram aktivnosti za dodavanje putovanja](https://github.com/foivz/r16030/blob/master/dijagrami/Dodavanje%20putovanja.jpg)
Na slici iznad prikazan je dijagram aktivnosti za „Dodaj putovanje“. Sve započinje zahtjevom korisnika za dodavanjem putovanja. Potom se inicijalizira i otvara forma za upravljanje putovanjima. Dio te forme koristi se za dodavanje novog putovanja. Unos podataka počinje odabirom datuma, kamiona i vozača. Nakon toga odabire se ruta. Ako ona postoji njezinim odabirom je proces unosa podataka završen. Ako ruta ne postoji u bazi potrebno je dodati novu rutu u bazu. Ako su uneseni svi podaci o putovanju, novo putovanje se dodaje u bazu i time se završava unos putovanja.

## Dijagram aktivnosti "Dodavanje rute"
Goran Čehulić
![Dijagram aktivnosti za izradu troškovnika](https://github.com/foivz/r16030/blob/master/dijagrami/dodaj%20rutu.jpg)

Prilikom unosa novog putovanja dolazi do zahtjeva za dodavanje nove rute. Otvara se forma za dodavanje rute. Korisnik unosi podatke o novoj ruti. Temeljem tih podataka sa servisa GoogleMaps dohvaća se ruta i prikazuje na formi. Potvrdom unosa rute, nova ruta se unosi u bazu podataka. Nakon unosa rute otvara se forma za upravljanje putovanjima na kojoj je sada dostupna novododana ruta.

## Dijagram aktivnosti "Izrada troškovnika"
Goran Čehulić
![Dijagram aktivnosti za izradu troškovnika](https://github.com/foivz/r16030/blob/master/dijagrami/Izrada%20tro%C5%A1kovnika.jpg)
Izrada troškovnika započinje zahtjevom korisnika za izradom troškovnika. Potom se otvara forma s prikazom putovanja i njihovih troškovnika. Nakon odabira putovanja za koje želimo izraditi troškovnik otvara se forma za unos imena novog troškovnika. Potom se novi prazni troškovnik dodaje u bazu podataka. U sljedećem koraku otvara se forma za dodavanje stavki na taj novi troškovnik. Nakon unosa stavki troškovnika podaci o njima se spremaju u bazu. Ponovno se otvara forma s prikazom putovanja i njihovih troškovnika.

## Dijagram aktivnosti "Unos kamiona"
Mia Tomašević
![Dijagram aktivnosti za unos kamiona]
(https://github.com/foivz/r16030/blob/master/dijagrami/UnosKamiona.png)

Dijagram aktivnosti za unos kamiona započinje zahtjevom za dodavanje kamiona, zatim se inicijalizira forma za unos kamiona. Korisnik unosi podatke o kamionu kao što su registracijska oznaka, marka, kilometraža, godina proizvodnje te potrošnja. Podaci se unose u bazu podataka, te se potom otvara glavna forma.

## Dijagram aktivnosti "Unos zaposlenika"
Mia Tomašević
![Dijagram aktivnosti za unos zaposlenika]
(https://github.com/foivz/r16030/blob/master/dijagrami/UnosZaposlenika.png)

Dijagram aktivnosti za unos zaposlenikazapočinje zahtjevom za dodavanje zaposlenika, zatim se inicijalizira forma za unos zaposlenika. Korisnik unosi podatke o zaposleniku kao što su ime i prezime, mail, lozinka, OIB te ovlasti. Podaci se unose u bazu podataka, te se potom otvara glavna forma.
 
## Dijagram aktivnosti "Izmjena podataka"
Mia Tomašević
![Dijagram aktivnosti za izmjenu podataka zaposlenika]
(https://github.com/foivz/r16030/blob/master/dijagrami/UrediZaposlenikaaaaa.png)

Dijagram aktivnosti za izmjenu podataka zaposlenika započinje zahtjevom za izmjenom podataka. Potom se inicijalizira forma za izmjenu podataka te se otvara forma za izmjenu podataka. Nakon korisnikovog odabira zaposlenika inicijalizira se forma za prikaz podataka o zaposleniku te se otvara forma za prikaz podataka o zaposleniku. Nadalje, korisnik odabire podatke za izmjenu te unosi izmijenjene podatke koji se izmjenjuju u bazi. Nakon toga se prikazuje glavna forma.

## Dijagram aktivnosti "Izmjena podataka"
Mia Tomašević
![Dijagram aktivnosti za izmjenu podataka kamiona]
(https://github.com/foivz/r16030/blob/master/dijagrami/IzmjenaKamiona.png)

Dijagram aktivnosti za izmjenu podataka kamiona započinje zahtjevom za izmjenom podataka. Potom se inicijalizira forma za izmjenu podataka te se otvara forma za izmjenu podataka. Nakon korisnikovog odabira kamiona inicijalizira se forma za prikaz podataka o kamionu te se otvara forma za prikaz podataka o kamionu. Nadalje, korisnik odabire podatke za izmjenu te unosi izmijenjene podatk ekoji se izmjenjuju u bazi. Nakon toga se prikazuje glavna forma.

## Dijagram aktivnosti "Brisanje zaposlenika"
Mia Tomašević
![Dijagram aktivnosti za brisanje zaposlenika]
(https://github.com/foivz/r16030/blob/master/dijagrami/BrisanjeZaposlenika.png)

Dijagram aktivnosti prikazan na slici iznad započinje korisnikovim zahtjevom za brisanjem zaposlenika, potom se inicijalizira forma za brisanje zaposlenika. Nakon toga se otvara forma za brisanje zaposlenika, te korisnik odabire zaposlenika kojeg želi izbrisati iz baze podataka. Nadalje, aplikacija prikazuje unesene podatke, te ukoliko korisnik odabere, briše se odabrani zaposlenik iz baze podataka. Nakon toga se prikazuje glavna forma.

## Dijagram aktivnosti "Brisanje kamiona"
Mia Tomašević
![Dijagram aktivnosti za brisanje kamiona]
(https://github.com/foivz/r16030/blob/master/dijagrami/BrisanjeKamiona.png)

Dijagram aktivnosti prikazan na slici iznad započinje korisnikovim zahtjevom za brisanjem kamiona, potom se inicijalizira forma za brisanje kamiona. Nakon toga se otvara forma za brisanje kamiona, te korisnik odabire kamion kojeg želi izbrisati iz baze podataka. Nadalje, aplikacija prikazuje unesene podatke, te ukoliko korisnik odabere, briše se odabrani kamion iz baze podataka. Nakon toga se otvara glavna forma. 

## Dijagram aktivnosti "Izvješća o kamionima"
Mia Tomašević
![Dijagram aktivnosti za izradu izvješća o kamionima]
(https://github.com/foivz/r16030/blob/master/dijagrami/Izvjescekamion.png)

Na slici je prikazan dijagram aktivnosti za izradu izvješća o kamionima. Započinje zahtjevom korisnika za izradu izvješća o kamionima. Inicijalizira se forma za izradu izvješća o kamionima te se ista i otvara. Iz baze prikupljamo podatke o kamionima koji se prikazuju u izvještaju. Potom korisnik zatraži ispis istoga. Započinje ispis putnog računa te se na kraju otvara glavna forma aplikacije.

## Dijagram aktivnosti "Izvješća o zaposlenicima"
Mia Tomašević
![Dijagram aktivnosti za izradu izvješća o zaposlenicima]
(https://github.com/foivz/r16030/blob/master/dijagrami/IzvjesceZaposlenici.png)

Na slici je prikazan dijagram aktivnosti za izradu izvješća o zaposlenicima. Započinje zahtjevom korisnika za izradu izvješća o zaposlenicima. Inicijalizira se forma za izradu izvješća o zaposlenicima te se ista i otvara. Iz baze prikupljamo podatke o zaposlenicima koji se prikazuju u izvještaju. Potom korisnik zatraži ispis istoga. Započinje ispis putnog računa te se na kraju otvara glavna forma aplikacije.


## Dijagram aktivnosti "Dodavanje računa"
Danijel Jurinjak
![D_A_dodavanje_racuna](https://github.com/foivz/r16030/blob/d745fbb0d6d581288980bd3ec661976e58dfe110/dijagrami/Dodavanje_racuna.jpg)

Dijagram prikazan na slici iznad započinje zahtjevom korisnika za dodavanje računa. U aplikaciji se inicijalizira forma za dodovanje računa te se ona i otvara. Nakon toga potrebno je odabrati putovanje koje želimo. U aplikaciji se popunjava forma nekim općim podacima o računu te se prikupljaju podaci o troškovniku iz baze podataka. Nakon toga se ti podaci prihvaćaju  te se dodaju stavke troškovnika na račun. Nadalje započinje obavljanje izračuna te se prikazuje račun koji se dodaje u bazu podataka. Nakon što smo dodali račun u bazu podataka aplikacija nam vraća poruku o dodavanju računa te korisnik zatražuje ispis računa. Sukladno tome i započinje ispis računa te se na kraju svega otvara glavna forma aplikacije. 

##Dijagram aktivnosti "Izrada izvješća o radu zaposlenika"
Danijel Jurinjak
![D_A_rad_zaposlenika](https://github.com/foivz/r16030/blob/d745fbb0d6d581288980bd3ec661976e58dfe110/dijagrami/Izvjesce_o_radu_zaposlenika.jpg)

Dijagram započinje zahtjevom korisnika za izradu izvješća o radu zaposlenika.  Nadalje u aplikaciji se inicijalizira forma za prikaz izvješća te se ona i otvara.  Kada ta aktivnost završi, korisnik odabire zaposlenika o kojem želi izvješće o radu te se uneseni podaci moraju potvrditi. Ako je kojim slučajem došlo do greške u odabiru zaposlenika, aplikacija nas baca natrag u odabir zaposlenika. Međutim, ako smo zadovoljni s odabirom tada se prikupljaju podaci o radu zaposlenika iz baze podataka. Kada se svi potrebni podaci sakupe, aplikacija nam prikaže podatke te nam kreira potrebno izvješće. Na kraju svega se otvara glavna forma aplikacije.

##Dijagram aktivnosti "Izrada izvješća o stanju i troškovima kamiona"
Danijel Jurinjak
![D_A_kamioni](https://github.com/foivz/r16030/blob/d745fbb0d6d581288980bd3ec661976e58dfe110/dijagrami/Izvjesce_o_kamionu.jpg)

Dijagram započinje zahtjevom korisnika za izradu izvješća. Nadalje u aplikaciji se inicijalizira forma za prikaz izvješća te se nakon toga otvara. Nakon toga korisnik odabire kamion o kojem želi izvješće te se uneseni podaci moraju potvrditi . Ako je došlo do greške u odabiru, aplikacija nas baca natrag u odabir. Međutim, ako smo zadovoljni s odabirom tada se prikupljaju podaci o tom kamionu iz baze podataka. Kada se potrebni podaci sakupe aplikacija nam prikaže podatke te nam kreira potrebno izvješće.  Na kraju svega se otvara glavna forma aplikacije. 

#Dijagrami slijeda

## Dijagram slijeda "Upravljanje zaposlenicima"
![Dijagram slijeda "Upravljanje zaposlenicima"](https://github.com/foivz/r16030/blob/master/dijagrami/dijagram_slijeda_zaposlenici.jpg)
Dijagram slijeda za „Upravljanje zaposlenicima“ nalazi se na slici iznad. Prije početka bilo kakve akcije administrator se prijavljuje u sustav.
* Dodavanje zaposlenika- Otvara se forma za dodavanje zaposlenika. Nakon što se popune podaci o novom zaposleniku , odnosno nakon što se popuni forma ti podaci se prosljeđuju u bazu nad kojom sustav izvršava upit kojim se upisuju podaci o zaposleniku. Ako je upit uspješno izvršen baza šalje potvrdu o unosu aplikaciji. Temeljem te potvrde aplikacija ispisuje korisniku poruku o unosu.
* Izmjena zaposlenika- Otvara se forma za izmjenu određenog  zaposlenika. Na toj formi izmjenimo podatke o zaposleniku koje želimo mijenjati. Ti novi podaci prosljeđuju se u bazu. Nad bazom se izvršava upit koji mijenja podatke u bazi. Potom baza šalje aplikaciji potvrdu o promjeni podataka, a temeljem te potvrde aplikacija ispisuje poruku o promjeni podataka.
* Birsanje zaposlenika- Nakon što se otvori forma za brisanje zaposlenika odabere se zaposlenik i taj odabir se prosljeđuje bazi. Izvršava se upit koji briše toga zaposlenika iz baze. O tome baza šalje potvrdu temeljem koje aplikacija ispisuje poruku o brisanju.
* Izvještaj o zaposlenicima- u formi za prikaz izvježtaja odabire se zaposlenik za kojeg želimo vidjeti izvještaj.  Temeljem tog odabira kreira se upit kojim se iz baze povuku podaci o zaposleniku. Ti podaci prosljeđuju se aplikaciji koja temeljem njih  popunjava izvještaj i ispisuje ga korisniku.

## Dijagram slijeda "Upravljanje kamionima"
![Dijagram slijeda "Upravljanje kamionima"](https://github.com/foivz/r16030/blob/master/dijagrami/dijagram_slijeda_kamioni.jpg)
Pošto su funkcionalnosti upravljanja kamionima jednake kao i funkcionalnosti za upravljanje zaposlenicima, dijagram slijeda za "Upravljanje kamionima" gotovo je jednak onome za "Upravljanje zaposlenicima".