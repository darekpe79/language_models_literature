# language_models_literature

Repozytorium zawiera zestaw modeli językowych opartych na HerBERT (od Allegro) do przetwarzania i analizy tekstów literackich. Projekty obejmują klasyfikację binarną, klasyfikację wieloklasową oraz rozpoznawanie nazwanych bytów (NER).

## 📦 Zawartość

| Plik | Opis |
|------|------|
| `True_false_31.12.2024.py` | Klasyfikacja binarna „do PBL” (czy artykuł nadaje się do bazy wiedzy) |
| `model_gatunki_earlystop_bez_wagi.py` | Klasyfikacja **gatunku/typu literackiego** na podstawie tytułu i treści |
| `model_hasla_17.04.2024.py` | Klasyfikacja **haseł przedmiotowych** |
| `nery_earlystop.py` | Rozpoznawanie nazwanych bytów (NER) z użyciem HerBERT i `seqeval` |

## 🚀 Szybki start

1. Zainstaluj wymagane biblioteki:
   pip install -r requirements.txt

2. Uruchom wybrany skrypt:
   python True_false_31.12.2024.py

## 📁 Dane wejściowe

Każdy projekt używa danych w formacie:
- `JSON` – z kolumnami np. `Link`, `Tekst artykułu`
- `Excel (.xlsx)` – z kolumnami jak `Tytuł artykułu`, `forma/gatunek`, `do PBL`, `hasła przedmiotowe`

## 🧠 Wymagania sprzętowe

Modele mogą działać na CPU (`no_cuda=True`), ale dla przyspieszenia zalecany jest GPU z obsługą CUDA.

## 📊 Wyniki

Modele zapisują:
- wytrenowane wagi (`model.save_pretrained`)
- tokenizer (`tokenizer.save_pretrained`)
- zakodowane etykiety (`LabelEncoder` jako `.joblib`)
- logi z treningu (`./logs`, `./results`)

## 📬 Autor

**darekpe79**  
https://github.com/darekpe79
