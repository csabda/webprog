
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
		
	Készlet csökkentése:
		Az új készlet elhelyezésénél felsorolt paraméterek alpaján csökkenti a készletet
		Hibát dob ha a menyiség meghaladja a raktáron lévő mennyiséget.
