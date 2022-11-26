## Role
David - Vedoucí projektu<br>
Lucka - Designer<br>
Boris - Programátor

- distribuovaný systém
- senzory: PIR, kamery (volitelné)
- komunikace: ethernet + ideálně i napájení pomocí PoE,
- prostředí (GUI): Webová aplikace (JS)

## Autorizace
- Použít SSO VŠB-TUO nebo vlastní
- Vlastní přihlášení, soubor ve formě JSON s jménem a heslem

## Aplikace
- GUI, webová aplikace
- Bude zobrazovat aktuální stav
- Umožňuje přepínat na manuální režim
- Konfigurace zařízení
- Design: Použije se šablona - třeba Material, Boostrap...

## Služba
- běží na serveru
- asi JavaScript, ve stylu spouštění jednotlivých skriptů

## Data
- aktuální data (projekce) budou k dispozici pomocí HTTP API
- historie bude obsahovat události (změny stavů jednotlivých zařízení - světel), historii přihlášení a (možná) veškerou historii úprav/konfigurace zařízení
- historie se nebude mazat - zůstane celá
- data se budou ukládat lokálně v místě, kde běží služba
- zálohování denně, 1 soubor = 1 den + záloha konfigurace(?)
- (MOŽNÁ) Zkusit nerelační databázi, třeba Mongo - otázka výkonu/stability/rychlosti a preferencí

## Bezpečnost
- Je-li požadavek na 100% spolehlivost systému, bude služba informovat o svém stavu
- Pak bude existovat druhý, nezávislý systém, který bude hlídat hlavní - v případě výpadku tento systém zareaguje nouzovým režimem 
- Otázka: Zpětná vázba z světel, jak kontrolovat, že fungují správně?

## Je třeba dořešit - vyřešeno
- Jak a kam vést komunikační / napájecí vodiče
- Je k dispozici server na kterém může služba běžet + spolehlivost + přístup k němu?
- Jak lze světla aktuálně ovládat, jaké jsou možnosti?
- Je nějaký plán/mapa parkoviště?
- Výběr PIR
- Výběr ethernet modulů k PIR
- Výběr kamer
