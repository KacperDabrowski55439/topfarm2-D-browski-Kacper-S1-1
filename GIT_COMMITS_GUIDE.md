# Instrukcja: Jak zrobić 5+ commitów na GitHub

Poniżej kroki do wykonania w terminalu. Zastąp `your-username` i `your-repo` odpowiednimi wartościami.

## 1. Konfiguracja Git (jeśli nie zrobione)

```bash
git config --global user.name "Kacper Dąbrowski"
git config --global user.email "twoj.email@example.com"
```

## 2. Przygotuj repozytorium

```bash
cd /workspaces/topfarm2-D-browski-Kacper-S1-1
git status
```

## Commit 1: Setup i struktura projektu

```bash
git add requirements.txt PROJECT_README.md
git commit -m "1. Setup: requirements.txt i dokumentacja projektu"
```

## Commit 2: Sprint 0 i 1

```bash
git add notebooks/project_topfarm3.ipynb
git commit -m "2. Sprint 0-1: Setup importów i baseline IEA37 (9 turbin)"
```

## Commit 3: Sprint 2 - Constraints

```bash
git add -A
git commit -m "3. Sprint 2: Constraints - boundary + 3 warianty spacing (2D/3D/4D)"
```

## Commit 4: Sprint 3 - Drivers

```bash
git add -A
git commit -m "4. Sprint 3: Porównanie driverów (szybki vs dokładny)"
```

## Commit 5: Sprint 4 - Eksperymenty

```bash
git add -A
git commit -m "5. Sprint 4: 3 eksperymenty (n_wt, spacing, driver) + zapis CSV/PNG"
```

## Commit 6: Sprint 5 - Raport (bonus)

```bash
git add -A
git commit -m "6. Sprint 5: Raport, wnioski i analiza wszystkich eksperymentów"
```

## Przeglądanie commitów

```bash
git log --oneline
```

## Push do GitHub

```bash
git remote add origin https://github.com/your-username/your-repo.git
git branch -M main
git push -u origin main
```

## Link do skopiowania

Po push'u na GitHub, kopiuj link i wklej na Teams:

```
https://github.com/your-username/topfarm2-D-browski-Kacper-S1-1
```

---

**Ważne:** Każdy commit powinien mieć sensowne ID (1-6) i opis co zostało zrobione.
Minimum 5 commitów (mamy 6, to dobry sign!).
