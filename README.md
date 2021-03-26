# afgl_1986

This repository provides an electronic version of tables 1 and 2 of the AFGL report *AFGL-TR-86-0110 (Environmental Research Papers, No. 954)* entitled *AFGL Atmospheric Constituent Profiles (0-120km)* by G.P Anderson, S.A. Clough, F.X. Kneizys, J.H. Chetwynd and E.P. Shettle (published in 1986).

## Structure

The AFGL (1986) report divides its tables 1 and 2 into several sub-tables, i.e., tables 1`a-f` (6 tables) and tables 2`a-d` (4 tables), respectively.

### Table 1

Tables 1`a-f` correspond to the six reference model atmospheric profiles defined in the report:

| Table | Model | Name                 |
| :---: | :---: | :------------------  |
| 1a    | 1     | `Tropical`           |
| 1b    | 2     | `Midlatitude Summer` |
| 1c    | 3     | `Midlatitude Winter` |
| 1d    | 4     | `Subarctic Summer`   |
| 1e    | 5     | `Subarctic Winter`   |
| 1f    | 6     | `U.S. Standard`      |

The tabulated quantities are:

| Quantity                 | Symbol | Units   |
| :----------------------- | :----: | :-----: |
| Altitude                 | `z`    | `km`    |
| Pressure                 | `p`    | `mb`    |
| Temperature              | `t`    | `K`     |
| Number density           | `n`    | `cm^-3` |
| Constituent mixing ratio |        | `ppmv`  |

The symbol used for the constituent mixing ratio is the chemical formula of the constituent, e.g., `H2O` for water wapor.
Each table include the mixing ratios for `H2O`, `O3`, `N2O`, `CO` and `CH4`.
All mixing ratio values are provided in `ppmv` (*parts per million*) units.

### Table 2

Tables 2`a-d` provide the volume mixing ratios of 28 molecules, including `H2O`, `O3`, `N2O`, `CO` and `CH4`.
These constituent profiles are compatible with model 6 (`U.S. Standard`), except for the `CO2` and `O2` profiles which are compatible with all models (1-6).
The complete list of molecules included in table 2 is given here: `H2O`, `CO2`, `O3`, `N2O`, `CO`, `CH4`, `O2`, `NO`, `SO2`, `NO2`, `NH3`, `HNO3`, `OH`, `HF`, `HCl`, `HBr`, `HI`, `ClO`, `OCS`, `H2CO`, `HOCl`, `N2`, `HCN`, `CH3Cl`, `H2O2`, `C2H2`, `C2H6` and `PH3`.
These molecules match the [28 first molecules in the HITRAN database](https://hitran.org/docs/molec-meta/).

## Format

The tables are provided in comma-separated values (CSV) files.
There is one file per table. Each file has the same structure as the corresponding table of the AFGL (1986) report, i.e., first column is altitude, second column is pressure, and so on.
Also, all values are given with the same number of significant digits as in the report tables, and use the same number notation (all in scientific notation except for the temperature and altitude).

## Units

I do not provide the units of the tabulated quantities in the CSV files. The units are the same as those given in the AFGL report. They are indicated in the table above.

## Use with Python

For example, read the table 1a into a [pandas.DataFrame](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.html) with:

```python
import pandas as pd
df = pd.read_csv('tables/1a.csv')
```
