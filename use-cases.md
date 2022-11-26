# UC 1

1. senzor detekuje pohyb
2. senzor odešle systému informaci, že detekoval pohyb
3. systém obdží informaci a zvolí ID světla, které má být spuštěno
4. systém odešlě ID světla nadřazenému systému

# UC 2

1. systém pošle dotaz senzoru
2. senzor odpoví že je v pořádku

## Rozšíření scénáře

- 2.1 senzor neodpoví do požadované doby
    - 2.1.1 systém pošle znovu dotaz senzoru
    - 2.1.2 senzor neodpoví do požadované doby
    - 2.1.3 systém pošle informaci o poruše senzoru nadřazenému systému
- 2.2 senzor odpoví, že není v pořádku
    - 2.2.1 systém pošlě informaci o poruše senzoru nadřazenému systému
