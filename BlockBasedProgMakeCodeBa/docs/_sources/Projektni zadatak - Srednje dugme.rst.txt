Projektni zadatak - Srednje dugme
=================================

Promenljiva čuva neku vrednost koju kasnije možemo da koristimo u programu.

Promenljive mogu biti:

•	Numerička (čuva broj)

•	Logika (čuva logičke vrednosti tačno / netačno)

•	Tekst (čuva tekst… „Zdravo“)

Promenljivu možemo da shvatimo kao prostor u memoriji računara, sličan kutiji, u kome se, za vreme izvršavanja programa, čuvaju neke međuvrednosti. Promenljive imaju svoja imena. Kada u programu želiš da koristiš vrednost promenljive, dovoljno je da navedeš  njeno ime.

Promenljivu kreiraš tako što, u kategoriji Variables (1), klikneš na dugme Make a variable (Napravi promenljivu) (2) i u polje uneseš ime promenljive (3). Klikom na dugme OK (4), kreirana je promenljiva.

.. image:: ../_images/_imageEV3/42.png
      :align: center

Promenljive ćemo da demonstriramo kreiranjem programa koji prikazuje koliko je korisnik puta pritisnuo srednje dugme na briku?

Kreirajmo promenljivu |Brojac|. Postavimo početnu vrednost brojača na 0, korišćenjem bloka |setBrojac|.
Ovaj blok prevučemo u blok |Start|. U okviru ovog bloka prikazujemo i vrednost brojača na samom početku na ekranu EV3 brika, korišćenjem bloka |show|.

.. |Brojac| image:: ../_images/_imageEV3/69.png
.. |setBrojac| image:: ../_images/_imageEV3/70.png
.. |Start| image:: ../_images/_imageEV3/8.png
.. |show| image:: ../_images/_imageEV3/77.png

Izgled koda:

.. image:: ../_images/_imageEV3/74.png
      :align: center

Na osnovu postavke zadatka potrebno je da se registruje pritisak korisnika na srednje dugme na briku, to ćemo postići korišćenjem bloka:

.. image:: ../_images/_imageEV3/78.png
      :align: center

Kada se registruje pritisak srednjeg dugmeta na briku, potrebno je povećati vrednost brojača za 1. To ćemo uraditi pomoću bloka |change| iz kategorije |Variable|. Za prikaz nove vrednosti promenljive Brojač koristimo blok |show|.

.. |change| image:: ../_images/_imageEV3/79.png
.. |Variable| image:: ../_images/_imageEV3/80.png

Izgled koda:

.. image:: ../_images/_imageEV3/75.png
      :align: center

Izgled konačnog koda:

.. image:: ../_images/_imageEV3/76.png
      :align: center

.. youtube:: BrojanjePritiska
      :width: 735
      :height: 415
      :align: center

Priključite EV3 Brick na računar pomoću USB kabla i klikom na dugme |dugme1| preuzmite .uf2 fajl na vaš računar. Prevlačenjem fajla na EV3 on je spreman za rad.

.. |dugme1| image:: ../_images/_imageEV3/download.png
              :width: 199px

Simulacija:

.. image:: ../_images/_imageEV3/78_.png
      :align: center

Upotreba promenljive demonstriraćemo i kroz još jedan primer kreiranja programa koji prebrojava preko koliko crnih linija je prešao Lego robot.

Kreirajmo promenljivu |Brojac|. Postavimo početnu vrednost brojača na 0, korišćenjem bloka |setBrojac|.
Ovaj blok prevučemo u blok |Start|. U okviru ovog bloka prikazujemo i vrednost brojača na samom početku na ekranu EV3 brika, korišćenjem bloka |show|.
U dati blok prevlačimo i blok |pravo| kojim ćemo obezbediti da se robot kreće beskonačno.

.. |pravo| image:: ../_images/_imageEV3/6.png

Izgled koda:

.. image:: ../_images/_imageEV3/81_.png
      :align: center

Na osnovu postavke zadatka potrebno je da senzor registruje crnu boju, to ćemo postići korišćenjem bloka u čijoj padajućoj listi biramo crnu boju:

.. image:: ../_images/_imageEV3/25.png
      :align: center

Kada se senzor registruje crnu boju, potrebno je uvečati vrednost brojača za 1. To ćemo uraditi pomoću bloka |change| iz kategorije |Variable|. Za prikaz nove vrednosti promenljive Brojač koristimo blok |show|.

Izgled koda:

.. image:: ../_images/_imageEV3/82_.png
      :align: center

Izgled konačnog koda:

.. image:: ../_images/_imageEV3/81.png
      :align: center

.. youtube:: BrojanjeLinija
      :width: 735
      :height: 415
      :align: center

Priključite EV3 Brick na računar pomoću USB kabla i klikom na dugme |dugme1| preuzmite .uf2 fajl na vaš računar. Prevlačenjem fajla na EV3 on je spreman za rad.
