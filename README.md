# Dokumentáció
## Raktár nyilvántartás

### Követelményanalízis 
A program hivatása hogy egy szállítócég raktárában nyilván tudják tartani a beérkező és a kimenő árukat. 
Lehetőség lesz regisztrálni, a regisztráció után a felhasználó tud beérkező árut rögzíteni, aszerint, 
hogy hova kell szállítani (belföldre, az Európai Unión belülre vagy azon kívülre, azaz vámos területre), 
illetve raktárban levő árut továbbítani a megfelelő helyre.

**Funkcionális követelmények**
* Regisztráció
* A raktárban levő áruk megtekintése
* Bejelentkezés
  - beérkező áru rögzítése
  - beérkező áruhoz a szállítási ország szerint a megfelelő dokumentumok hozzárendelése
  -	bent levő áru törlése
  -	bent levő áru állapotának megváltoztatása (szállításra kész vagy nem)
  -	bent levő áruhoz megjegyzés fűzése
  
**Nem funkcionális követelmények**
*	Áttekinthetőség
*	Biztonság: jelszavak megfelelő védelme, csak regisztráció után elérhető funkciók, hibák megfelelő kezelése
*	Karbantarthatóság

**Szakterületi fogalomjegyzék**
##### Áru típusok
*	Belföld: Magyarországon belülre szállítandó
*	Európai Unió: az Európai Unió területére szállítandó, tehát vámmentes
*	Európai Unión kívüli: az Európai Unió területén kívülre szállítandó, tehát vámköteles
*	Vámmentes: A személyre tekintet nélkül jószág, áru, melyet vámdíj nélkül szállítani lehet, szabad.
*	Vámköteles: Áru, melyért a feladó vámot köteles fizetni.

**Használatieset-modell**
##### Szerepkörök
* Vendég
  -	Főoldal
  -	Raktárban levő áruk megtekintése
  -	Bejelentkezés
  -	Regisztráció
* Bejelentkezett felhasználó
  -	Beérkező áru rögzítése
  -	Raktárban levő áruk megtekintése
  -	Raktárban levő áru törlése
  -	Raktárban levő áru adatainak módosítása
  -	Raktárban levő áru továbbítása szállításra (állapot megváltoztatása „szállítható”-ra)
  -	Raktárban levő áruhoz megjegyzés fűzése



