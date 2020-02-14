Projektni zadatak - Upotreba senzora
====================================

**Upotreba senzora dodira**

Najpre ćemo programirati jednostavno kretanje robota sve dok senzor dodira ne dotaknemo rukom. Cilj ovog programa je da se robot kreće sve dok se ne dodirne senzor rukom.

.. image:: ../_images/_imageEV3/17_.png
      :align: center

Na osnovu postavke zadatka robot se kreće pravo, da bi to uradili prevlačimo blok |pravo| (robot se kreće pravo).

.. |pravo| image:: ../_images/_imageEV3/6.png

Zatim, se iz kategorije |senzor| izabere blok |Pause|. Iz padajuće liste bloka biramo opciju 1 koja predstavlja port na kome je vezan senzor dodira.
Zatim, se bira opcija pritisnuto (pressed), koja predstavlja stanje senzora dodira. (Kada ruka dodirne senzor).
A zatim, na osnovu uslova zadatka, robot treba da se zaustavi, tako što izaberemo blok |Stop|.
Na taj način robot se zaustavio.

.. |senzor| image:: ../_images/_imageEV3/22.png
.. |Pause| image:: ../_images/_imageEV3/23.png
.. |Stop| image:: ../_images/_imageEV3/14.png

Izgled programa:

.. image:: ../_images/_imageEV3/24.png
      :align: center

.. youtube:: SenzorDodira
      :width: 735
      :height: 415
      :align: center

Priključite EV3 Brick na računar pomoću USB kabla i klikom na dugme |dugme1| preuzmite .uf2 fajl na vaš računar. Prevlačenjem fajla na EV3 on je spreman za rad.

.. |dugme1| image:: ../_images/_imageEV3/download.png
            :width: 199px

**Upotreba senzora boje**

Senzor za boje je digitalni senzor koji može da detektuje boju ili intenzitet svetlosti koja ulazi kroz mali prozor na prednjoj strani sezora. Ovaj senzor se može koristiti na tri različita načina:

•	Color Mode,

•	Reflected Light Intensity Mode (Intenzitet reflektovane svetlosti), i

•	Ambient Light Intensity Mode (Intenzitet ambijentalnog osvetljenja).

U Color Mode-u, Color senzor prepoznaje sedam boja - crna, plava, zelena, žuta, crvena, bela, i braon i plus bez boje:

.. image:: ../_images/_imageEV3/24_.png
      :align: center

Ova sposobnost da razlikuje boje znači da robot može biti programiran da razvrsta obojene kugle ili blokove, da govori imena boja koje su detektovane, ili da zaustavi akciju kada vidi crveno.

.. image:: ../_images/_imageEV3/27.png
      :align: center

U Reflected Light Intensity Mode-u, Color senzor meri intenzitet svetlosti koja se reflektuje. Senzor koristi opciju dark (veoma tamno) I light (veoma svetlo). To znači da robot može biti programiran da se kreće na beloj površini dok se crna linija ne detektuje, ili da interpretira kodiranu boju lične karte.

U Ambient Light Intensity Mode-u, Color senzor meri jačinu svetlosti koja ulazi kroz prozor iz okruženja, kao što je sunčeva svetlost ili snop baterijske lampe. Senzor koristi opciju dark (veoma tamno) I light (veoma svetlo). To znači da robot može biti programiran da pokrene alarm kada sunce izlazi ujutro, ili da zaustavi akciju ako se svetla ugase.

.. image:: ../_images/_imageEV3/28.png
      :align: center

Upotrebu senzora boje demonstriraćemo kreiranjem programa pomoću koga se robot kreće sve dok ne vidi zelenu boju. Kada registuje zelenu boju robot se zaustavlja.

Na osnovu postavke zadatka robot treba da se kreće pravo. Kretanje robota pravo, postižemo prevlačenjem bloka |pravo| robot se kreće pravo).
Zatim, se iz kategorije |Senzor| izabere blok |PauseColor|. Iz padajuće liste bloka biramo opciju 3 koja predstavlja port na kome je vezan senzor boje. Zatim, se iz padajućeg menija |Boja| bira boja, klikom na željenu boju (u našem slučaju zelena). A zatim, na osnovu uslova zadatka, robot treba da se zaustavi, tako što izaberemo blok |Stop|. Na taj način robot se zaustavio.

.. |PauseColor| image:: ../_images/_imageEV3/29.png
.. |Boja| image:: ../_images/_imageEV3/30.png

Kod programa i izgled simulacije (robot se kreće, sve dok ne vidi zelenu boju):

.. image:: ../_images/_imageEV3/313233.png
      :align: center

.. youtube:: SenzorBoje
      :width: 735
      :height: 415
      :align: center

Priključite EV3 Brick na računar pomoću USB kabla i klikom na dugme |dugme1| preuzmite .uf2 fajl na vaš računar. Prevlačenjem fajla na EV3 on je spreman za rad.


**Upotreba ultrazvučnog senzora**

Upotrebu ultrazvučnog senzora demonstriraćemo kreiranjem programa tako da se robot kreće sve dok ne naiđe na prepreku.

Na osnovu postavke zadatka robot treba da se kreće pravo. Kretanje robota pravo, postižemo prevlačenjem bloka |pravo| (robot se kreće pravo).

Zatim, se iz kategorije |Senzor| izabere blok |ultra|. Iz padajuće liste bloka biramo opciju ``4`` koja predstavlja port na kome je vezan ultrazvučni senzor.
Iz padajućeg menija |meni| biramo ociju ``near`` (u našem slučaju zelena). Kako na osnovu uslova zadatka, robot treba da se zaustavi, tako što izaberemo blok |Stop|. Na taj način robot se zaustavio.

.. |ultra| image:: ../_images/_imageEV3/38.png
.. |meni| image:: ../_images/_imageEV3/39.png

Kod programa i izgled simulacije (robot se kreće, sve dok ne vidi predmet):

.. image:: ../_images/_imageEV3/353637.png
      :align: center

.. youtube:: SenzorDaljine
      :width: 735
      :height: 415
      :align: center

Priključite EV3 Brick na računar pomoću USB kabla i klikom na dugme |dugme1| preuzmite .uf2 fajl na vaš računar. Prevlačenjem fajla na EV3 on je spreman za rad.
