
## Funkcionális és nem funkcionális követelmények

## Feledat leírás:

	Egy rakár kezelő alkalmazás fejlesztése, mely pontosan egy raktár készletét tarta nyílván.
	Megfelelő hozzáférési jogosultsággal a raktár készletéhez hozzáadhatunk törölhetünk, 
	lekérdezhetjük egy termékből mennyi van  és hogy hol található.

## Funkcionális követelmények:
	
	Bejelentkezés:
		Alkalmazott:
			csak olyan alkalmazott jelentkezhet be és dolgozhat a raktár kezelő programmal
			aki szerepel az "ALKALMAZOTTAK" adatbázis táblában, melynek kezeléséhez adminisztrátori
			jog kell
		
		Adminisztrátor:
			MInden műveletet elvégezhet amelyet egy alkalmazott képes. Ezeken felül az admnisztrátor
			hozzáadhat alkalmazottat az adatbázishoz, illetve törölhet onnan alkalmazottat.
			Továbbá az adminisztrátornak van joga a beállításokat végezni (PL: ratár maximális kapacitása)
			
	Beállítások:
		Csak az adminisztrátornak van joga ezt a funkciót elérni, mely tartalmazza az alábbiakat:
			- Raktár maximális kapacitása
			- Alkalmazott felvétele
			- Alkalmazott törlése
			- Alkalmazott adatok módosítása
	
	Új készlet elhelyezése:
		Új készletet felvételre kerül a raktár adatbázisába paraméterek szerint melyek az alábbiak
			- egység méret (térbeli kiterjedése)
			- darabszám
			- név
			- egyéni ID
		Ha nem sikerül mindet elhelyezni akkor visszaajda az el nem helyezhető termékek számát
		Alkalmazottak és Adminisztrátorok egyaránt használhatják ezta funkciót.
		
	Készlet csökkentése:
		Az új készlet elhelyezésénél felsorolt paraméterek alpaján csökkenti a készletet
		Hibát dob ha a menyiség meghaladja a raktáron lévő mennyiséget.
		Alkalmazottak és Adminisztrátorok egyaránt használhatják ezta funkciót.

##Nem funkcionális követelmények:
	Használhatóság: 
		Egyszerű, átlátható GUI minden felhasználó számára. Ne legyen szükséges dokumentációt átolcasni
		a használathoz azaz önmagyarázó legyen
	
	Teljesítmény: 
		Mivel minden raktár helység önálló adatbázissal rendelkezik és a raktáerak mérete is igen csak véges, továbbá 				optimalizált SQL lekérdezések biztosítják az alkalmazás gyors futását
		
	Rendelkezésre állás:
		
több esetben százalékban megadott érték. A 99%-os rendelkezésre állás azt jelenti, hogy a felhasználók az esetek 99%-ban elérik a szolgáltatásokat. Többnyire része a a Szolgáltatási Szint Megállapodásnak (SLA: Service Level Agreement ). Jellemzően szolgáltatás-mérési mutató. Mérésének ellenőrzésére egyszerűen alkalmazhatóak a szerver logok.
Skálázhatóság: a rendszer növekedéséből fakadóan milyen bővítéseket kell tennünk, például milyen szervereket kell üzembe helyezni. Jellemzően az elvárt teljesítményből határozhatjuk meg.
Biztonság: adat-védelmi elvárások meghatározása. Webes alkalmazások biztonsági tesztelése nem egyszerű feladat, az alkalmazás normál működésén alapulva megpróbálunk ártalmas tevékenységet véghezvinni, azaz például személyes adatokat próbálunk megszerezni, módosítjuk az oldal tartalmát, esetleg összeomlasztjuk a rendszert.
Karbantarthatóság: olyan a megbízó által adott elvárások, melyek az alkalmazás üzemeltetésével, karbantartásával, bővítésével kapcsolatosak.
