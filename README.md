# SMART výtah

Adaptivní algoritmus výtahu, jehož cílem je zkrátit čekání cestujících a snížit ujetou vzdálenost oproti původnímu algoritmu.

## Spuštění

### Online

**[▶ Otevřít simulátor výtahu](https://ondrejvdf.github.io/smart-vytah/vytah.html)**

1. Stáhněte přiložené [zadání se 400 lidmi](zadani.json). Na GitHubu otevřete soubor a zvolte **Download raw file**.
2. Otevřete simulátor pomocí odkazu výše.
3. Klikněte na **Vybrat soubor** a načtěte stažené `zadani.json`.
4. Zkontrolujte název **Běžný den ve škole**, počet **400 osob** a otisk **B746-8C6D**.

Výsledky se spočítají po načtení zadání. Tlačítkem **Spustit** lze přehrát průběh simulace.



## Jak algoritmus funguje

- Seskupuje čekající podle patra a požadovaného směru.
- Při výběru skupiny zohledňuje počet lidí, dobu čekání a vzdálenost výtahu.
- Cestující v kabině rozváží postupně po směru jízdy.
- Další lidi po cestě přibírá jen za podmínek, které omezují zdržování cestujících uvnitř.
- Když nikdo nečeká, může zaparkovat podle nedávno pozorovaných nástupních pater.
- Před každou simulací resetuje svou paměť.

Algoritmus používá pouze informace dostupné v objektu `stav`. Nezná budoucí příchody ani skryté cíle čekajících.

## Výsledky

Porovnání bylo provedeno na stejném zadání **Běžný den ve škole**, otisk **B746-8C6D**.

| Ukazatel | Původní algoritmus | SMART LIFT 4 |
|---|---:|---:|
| Rozvezeno osob | 400/400 | 400/400 |
| Průměrný čas celkem | 336,1 s | 185,0 s |
| Průměrné čekání | 313,7 s | 165,7 s |
| Průměrná jízda | 22,4 s | 19,3 s |
| Nejdelší čekání | 1 438,7 s | 660,6 s |
| Ujetá vzdálenost | 2 922 m | 2 340 m |

Průměrný čas celkem se snížil přibližně o **44,9 %** a ujetá vzdálenost o **19,9 %**.


