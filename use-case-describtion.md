# Use Case Diagram

### Obecné
- **Obsluha** je aktér, který reprezentuje člověka mající přístup do systému
	- Aktér je ověřen na základě znalosti hesla
	- Obsluha může:
		- *zobrazit aktuální stav*, tedy, zdali senzory fungují správně a aktuální výstupy
		- *zobrazit historické záznamy* v podobě logů ukládaných do nerelační databáze
		- *přepnout režim aplikace*, tedy aktivovat běžný režim nebo nouzový režim. Nouzový režim se bude řídit podle instrukcí nadřazeného systému.
- **Senzory** jsou zařízení, které budou systému přes definované komunikační rozhraní zasílat informace systému.
	- senzory budou:
		- *zasílat v pravidelných intervalech stav*, tedy zda-li senzory fungují správně
		- *zasílat při detekci objektu impuls*, na základě kterého systém aktivuje osvětlení v dané části, kde se senzor nachází.
- **Osvětlení** bude příjmat od systému impulsy, na základě kterých se bude osvětlení zapínat a vypínat
- **Nadřazený systém** zajišťuje v případě chyby chod systému, aby byla zajištěna funkčnost osvětlení i v případě poruchy.
