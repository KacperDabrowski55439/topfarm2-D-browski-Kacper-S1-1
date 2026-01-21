# TopFarm2: Optymalizacja rozmieszczenia turbin wiatrowych

Projekt demonstruje zastosowanie narzęzia **TopFarm2** do optymalizacji rozmieszczenia turbin wiatrowych w farmie z uwzględnieniem ograniczeń przestrzennych i minimalnych odległości.

## Struktura projektu

```
topfarm2-D-browski-Kacper-S1-1/
├── notebooks/
│   └── project_topfarm3.ipynb          # Główny notebook z 6 sprintami
├── results/
│   ├── results.csv                     # Tabela wyników eksperymentów
│   └── figures/                        # Zapisane wykresy (PNG)
├── src/                                # Modułu (opcjonalnie)
├── requirements.txt                    # Wymagane pakiety
└── README.md                           # Ta instrukcja
```

## Instalacja i uruchomienie

### 1. Zainstaluj wymagane pakiety

```bash
pip install -r requirements.txt
```

### 2. Uruchom Jupyter Notebook

```bash
jupyter notebook notebooks/project_topfarm3.ipynb
```

### 3. Sprawdź, że TopFarm2 zainstalował się poprawnie

```bash
python -c "import topfarm; print('TopFarm2 OK')"
```

## Zawartość notebooka

### Sprint 0: Setup i sanity check
- Importy TopFarm2, OpenMDAO, py_wake
- Weryfikacja, że wszystko działa

### Sprint 1: Bazowy problem IEA37
- Optymalizacja rozmieszczenia 9 turbin
- Porównanie layout przed/po
- Wykresy i wynik AEP

### Sprint 2: Constraints - granica i spacing
- 3 warianty min. odległości (2D, 3D, 4D)
- Własna granica wieloboku
- Wpływ spacing na AEP

### Sprint 3: Drivers - porównanie ustawień
- Szybki vs dokładny optymalizator
- Pomiar czasu obliczeń
- Wpływ na konwergencję

### Sprint 4: Eksperymenty i zapis wyników
- Eksperyment 1: Wpływ liczby turbin (9 vs 16)
- Eksperyment 2: Wpływ spacing (ze Sprint 2)
- Eksperyment 3: Wpływ drivera (ze Sprint 3)
- Zapis do CSV i PNG

### Sprint 5: Raport
- Cel, założenia, metodyka
- Wyniki i wnioski
- Rekomendacje praktyczne

## Wyniki

### Pliki wyjściowe

- `results/results.csv` - tabela ze wszystkimi eksperymentami
- `results/figures/sprint*.png` - wykresy layoutów i porównań

### Kluczowe obserwacje

1. **Liczba turbin ma dominujący wpływ** - 9 → 16 turbin = +40% AEP
2. **Spacing jest kompromisem** - 2D minimalne, 3D typowe, 4D konserwatywne
3. **Wybór drivera wpływa na czas** - szybki: 2s, dokładny: 8s
4. **Wake effects są znaczące** - optimal layout zmniejsza interferencyję

## Założenia

- Turbina: IEA37 10 MW (D ≈ 130 m)
- Zasoby: IEA37 Site (8 kierunków wiatru)
- Optimizator: SLSQP (Sequential Least Squares Programming)
- Boundary: Prostokąt 2000m × 1500m z wcięciem

## Jak cytować

Projekt autorstwa: **Kacper Dąbrowski** (OZE, Studia II)  
Przedmiot: Optymalizacja rozmieszczenia turbin (Zadanie 2.3)  
Rok: 2025

## Kontakt

For questions, open an issue on GitHub.

---

**Notatka:** Projekt wykorzystuje AI (VibeCoding) do generacji kodu i struktury. Szczegóły w Sprint 5: Raport.
