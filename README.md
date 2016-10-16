Dokumentáció

Követelményanalízis

A program hivatása hogy egy szállítócég raktárában nyilván tudják tartani a beérkező és a kimenő árukat. Lehetőség lesz regisztrálni, a regisztráció után a felhasználó tud beérkező árut rögzíteni, aszerint, hogy hova kell szállítani (belföldre, az Európai Unión belülre vagy azon kívülre, azaz vámos területre), illetve raktárban levő árut továbbítani a megfelelő helyre.

Funkcionális követelmények
	
•	Regisztráció
•	A raktárban levő áruk megtekintése
•	Bejelentkezés
o	beérkező áru rögzítése
o	beérkező áruhoz a szállítási ország szerint a megfelelő dokumentumok hozzárendelése
o	bent levő áru törlése
o	bent levő áru állapotának megváltoztatása (szállításra kész vagy nem)
o	bent levő áruhoz megjegyzés fűzése

Nem funkcionális követelmények

•	Áttekinthetőség
•	Biztonság: jelszavak megfelelő védelme, csak regisztráció után elérhető funkciók, hibák megfelelő kezelése
•	Karbantarthatóság

Szakterületi fogalomjegyzék

	Áru típusok
•	Belföld: Magyarországon belülre szállítandó
•	Európai Unió: az Európai Unió területére szállítandó, tehát vámmentes
•	Európai Unión kívüli: az Európai Unió területén kívülre szállítandó, tehát vámköteles
•	Vámmentes: A személyre tekintet nélkül jószág, áru, melyet vámdíj nélkül szállítani lehet, szabad.
•	Vámköteles: Áru, melyért a feladó vámot köteles fizetni.

Használatieset-modell

	Szerepkörök
•	Vendég:
o	Főoldal
o	Raktárban levő áruk megtekintése
o	Bejelentkezés
o	Regisztráció

•	Bejelentkezett felhasználó
o	Beérkező áru rögzítése
o	Raktárban levő áruk megtekintése
o	Raktárban levő áru törlése
o	Raktárban levő áru adatainak módosítása
o	Raktárban levő áru továbbítása szállításra (állapot megváltoztatása „szállítható”-ra)
o	Raktárban levő áruhoz megjegyzés fűzése





Példa folyamat: Beérkező áru rögzítése
	
1.	A felhasználó bejelentkezik vagy regisztrál a főoldalon.
2.	Bejelentkezés után a felhasználó megnyomja az „Áru rögzítése” gombot.
3.	A megjelenő űrlapon rögzíti a szükséges adatokat.
4.	Rákattint a „mentés” gombra.






















Tervezés

Architektúra terv

	Oldaltérkép
•	Publikus
­	Főoldal
­	Bejelentkezés
­	Regisztráció
­	Áruk böngészése
•	Bejelentkezett felhasználó
­	Főoldal
­	Kijelentkezés
­	Áruk böngészése
­	Új áru rögzítése
­	Áru adatainak módosítása
­	Áru törlése
­	Megjegyzés fűzése áruhoz
­	Áru szállításra bocsátása

Végpontok
•	GET/: főoldal
•	GET/login: bejelentkező oldal
•	POST/login: bejelentkezési adatok felküldése
•	GET/signup: regisztrációs oldal
•	POST/signup: regisztrációs adatok felküldése
•	GET/logout: kijelentkező oldal
•	GET/products: áruk listájának oldala
•	GET/products/newProduct: új áru rögzítése
•	POST/products/newProduct: új áru adatainak felküldése
•	GET/products/getProduct/:id: áru adatok
•	POST/products/newComment/:id: megjegyzés hozzáfűzése az áruhoz
•	GET/products/editProduct/:id: áru adatainak módosítása
•	POST/products/editProduct/:id: módosított adatok felküldése
•	GET/products/deleteProduct/:id: áru törlése

Adatmodell

			


