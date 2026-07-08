# Dane źródłowe / Source data

 **Polski** · [English below](#-english)

## Polski

Dane udostępniono w formacie **CSV** (podgląd bezpośrednio na GitHubie w formie tabeli).

Trzy zbiory zasilające model gwiazdy (star schema) w Power BI:

| Zbiór | Tabela w modelu | Rola | Wiersze |
|---|---|---|---|
| `sprzedaz` ([csv](sprzedaz.csv)) | `FactSprzedaz` | tabela faktów | 2 412 |
| `klienci` ([csv](klienci.csv)) | `DimKlienci` | wymiar | 8 |
| `produkty` ([csv](produkty.csv)) | `DimProdukty` | wymiar | 158 |

Tabela `DimDate` generowana jest w DAX (nie pochodzi z pliku) - patrz [`METHODOLOGY.md`](../METHODOLOGY.md).

**Format CSV:** separator przecinek, kropka dziesiętna, kodowanie UTF-8.
**Klucze relacji:** `numer_gr_klienta` (Fact DimKlienci), `numer kategorii` (Fact DimProdukty), `data` (Fact DimDate).

Wartości netto, bez korekt. Okres: I 2025 – V 2026 (17 mies., dane w 12).
Dane o charakterze rekrutacyjnym/szkoleniowym.

---

<a name="-english"></a>
## English

The data are provided in **CSV** format (previewable directly on GitHub as a table).

Three datasets feeding the Power BI star schema:

| Dataset | Model table | Role | Rows |
|---|---|---|---|
| `sprzedaz` ([csv](sprzedaz.csv)) | `FactSprzedaz` | fact table | 2,412 |
| `klienci` ([csv](klienci.csv)) | `DimKlienci` | dimension | 8 |
| `produkty` ([csv](produkty.csv)) | `DimProdukty` | dimension | 158 |

The `DimDate` table is generated in DAX (not sourced from a file) - see [`METHODOLOGY.md`](../METHODOLOGY.md).

**CSV format:** comma separator, decimal point, UTF-8 encoding.
**Relationship keys:** `numer_gr_klienta` (Fact DimKlienci), `numer kategorii` (Fact DimProdukty), `data` (Fact DimDate).

Net values, corrections excluded. Period: Jan 2025 – May 2026 (17 months, data in 12).
Data is for recruitment/training purposes.
