# AFGL 1986

In this directory, I provide an electronic version of tables 1 and 2 of the AFGL report *AFGL-TR-86-0110 (Environmental Research Papers, No. 954)* entitled *AFGL Atmospheric Constituent Profiles (0-120km)* by G.P Anderson, S.A. Clough, F.X. Kneizys, J.H. Chetwynd and E.P. Shettle (published in 1986).

## Structure

The AFGL (1986) report divides its table 1 and 2 into several sub-tables, tables 1a-f (6 tables) and tables 2a-d (4 tables), respectively. Tables 1a-f correspond to the six reference model atmospheric profiles defined in the report:

| Table | Model | Name                 |
| :---: | :---: | :------------------  |
| 1a    | 1     | `Tropical`           |
| 1b    | 2     | `Midlatitude Summer` |
| 1c    | 3     | `Midlatitude Winter` |
| 1d    | 4     | `Subarctic Summer`   |
| 1e    | 5     | `Subarctic Winter`   |
| 1f    | 6     | `U.S. Standard`      |

The tabulated quantities are

* altitude (km)
* pressure (mb)
* temperature (K)
* number density (cm^-3)
* water (H2O) volume fraction (ppmv)
* ozone (O3) volume fraction (ppmv)
* nitrogen oxide (N2O) volume fraction (ppmv)
* carbon monoxide (CO) volume fraction (ppmv)
* methane (CH4) volume fraction (ppmv)

Tables 2a-d provide the volume mixing ratios of 28 molecules. These constituent profiles are compatible with model 6 (`U.S. Standard`), except for the CO2 and O2 profiles which are compatible with all models (1-6).

## Format

The tables are provided in comma-separated values (CSV) files. There is one file per table. Each file has the same structure as the corresponding table of the AFGL (1986) report, i.e., first column is altitude, second column is pressure, and so on. Also, all values are given with the same number of significant digits as in the report tables, and use the same number notation (all in scientific notation except for the temperature and altitude).

## Units

I do not provide the units of the tabulated quantities in the CSV files. The units are the same as those given in the AFGL report.

## Use with Python

```python
import pandas as pd
df = pd.read_csv('table_1a.csv')
```
