
OPIS PROJEKTA: Web aplikacija za online prodaju proizvoda s korisničkim i administratorskim sučeljem.

TEHNOLOGIJE:
 Backend: Laravel
 Frontend: Vue3
 Baza: MySQL
 Autentifikacija: Laravel Sanctum

 VRSTE KORISNIKA:
   Gost - pregled stranica
   Korisnik - kupnja proizvoda (košarica + chackout)
   Administrator- upravljenje proizvodima, statistika
   SuperAdmin- sve kao admin+ dodavanje novog admina

         Dashboardu pristup imaju samo admin i superAdmin. SuperAdmin moze dodat novog administratora
           superAdmin
            k.ime: superadmin
            k.lozinka: 1234567
          admin:
            k.ime: mario
            k.lozinka: 888888

  FUNKCIONALNOST:
    Registracija/ Prijava
    Web košarica
    Checkout narudzbe
    Pretraga proizvoda
    Dodavanje/ uređivanje artikala
    Pregled najprodavanijeg artikla
    Pregled najvjernijeg kupca

  BAZA PODATAKA:
   Glavne tablice:
     - user
     - roles
     - products
     - categories
     - orders
     - order_items
     - payment_methods

  POKRETANJE PROGRAMA

    Backend
       composer install
       php artisan migrate
       php artisan serve

    Frontend
       npm install
       npm run dev
    
