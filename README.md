# SPSS-Data-Weighter

[EN] SPSS Data Weighter - Raking/IPF Automation Tool
A professional GUI-based tool designed for Data Processing (DP) specialists to automate the process of sample weighting in SPSS using the Raking (Iterative Proportional Fitting) algorithm.

🚀 Key Features
Smart Mapping: Automatically maps Excel labels (e.g., "Female") to SPSS numeric codes (e.g., "2") using metadata analysis.

Flexible Target Entry: Load target proportions directly from Excel or enter them manually via a dynamic interface.

Weight Trimming: Built-in capping (min/max limits) to prevent extreme weights and ensure statistical validity.

Metadata Preservation: Saves the weighted file while keeping all original SPSS variable labels and value labels intact.

🛠️ Requirements
Python 3.x

Libraries: pandas, numpy, pyreadstat, openpyxl

Bash
pip install pandas numpy pyreadstat openpyxl
📖 How to Use
Load SPSS File: Select your .sav data file.

Define Targets: - Use an Excel file with 3 columns: Variable Name, Category, Target Proportion (e.g., 0.5 for 50%).

OR use Manual Mode to enter proportions directly.

Set Limits: Define the minimum and maximum allowed weights (default 0.33 - 3.0).

Run: The tool will generate a new file with the WAGA variable in C:\WAGA SPSS\.

[PL] Ważarka SPSS - Automatyzacja Ważenia Danych (Raking/IPF)
Profesjonalne narzędzie z interfejsem graficznym (GUI) stworzone dla specjalistów Data Processing (DP), automatyzujące proces ważenia prób w plikach SPSS przy użyciu algorytmu Raking (Iterative Proportional Fitting).

🚀 Kluczowe Funkcje
Inteligentne Mapowanie: Automatycznie zamienia etykiety z Excela (np. "Kobieta") na kody numeryczne SPSS (np. "2") dzięki analizie metadanych.

Elastyczne źródła danych: Możliwość wczytania proporcji docelowych z pliku Excel lub ręcznego wpisania ich w interfejsie.

Trimming (Przycinanie wag): Wbudowana funkcja limitowania wag (min/max), zapobiegająca powstawaniu wag ekstremalnych.

Zachowanie Metadanych: Zapisuje zważony plik, zachowując wszystkie oryginalne etykiety zmiennych i wartości.

🛠️ Wymagania
Python 3.x

Biblioteki: pandas, numpy, pyreadstat, openpyxl

Bash
pip install pandas numpy pyreadstat openpyxl
📖 Instrukcja Obsługi
Wybierz plik SPSS: Wskaż bazę danych .sav.

Zdefiniuj cele (Targets):

Użyj Excela z 3 kolumnami: Nazwa Zmiennej, Kategoria, Proporcja Docelowa (np. 0.4 dla 40%).

LUB wybierz Tryb Ręczny, aby wpisać dane w oknach dialogowych.

Ustaw Limity: Określ dolną i górną granicę wagi (domyślnie 0.33 - 3.0).

Generuj: Program utworzy folder C:\WAGA SPSS i zapisze tam gotowy plik z nową zmienną WAGA.
