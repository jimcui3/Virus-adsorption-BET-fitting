# Virus-adsorption-BET-fitting

## Virus Spectra Dataset

This repository contains experimental averaged and linearly-decomposed SERS spectra for single‐virus and binary‐virus mixtures in two media (water and saliva), both with SiO₂ substrates and Gaussian-Lorentzian baseline correction (GLF).

---

## 📂 Repository structure
```
.
├── Virus_in_Water/
│   ├── Least squares fitting of mixture (water).ipynb
│   ├── test_virus_in_water.csv
│   ├── SiO2 - only GLF.txt
│   ├── 05132025 - Average Spectra for Each Concentration - Single Virus in Water with SiO2 - GLF.csv
│   ├── 05132025 - Average Spectra for Each Concentration - Binary Mixture in Water with SiO2 - GLF.csv
│   ├── 05132025 - Reconstructed Spectra for Each Concentration - Single Virus in Water with SiO2 - GLF.csv
│   ├── 05132025 - Reconstructed Spectra for Each Concentration - Binary Mixture in Water with SiO2 - GLF.csv
│   └── Reconstructed Spectra vs Actual Average Spectra - Water with SiO2 - GLF/
│       └── *.png  (one figure per virus/mixture + concentration)
│
└── Virus_in_Saliva/
    ├── Least squares fitting of mixture (saliva, with background).ipynb
    ├── test2_virus_in_saliva.csv
    ├── 05062025 - saliva (GLF 450-1700).txt
    ├── SiO2 - only GLF.txt
    ├── 05142025 - Average Spectra for Each Concentration - Single Virus in Saliva with SiO2 - GLF.csv
    ├── 05142025 - Average Spectra for Each Concentration - Binary Mixture in Saliva with SiO2 - GLF.csv
    ├── 05142025 - Reconstructed Spectra for Each Concentration - Single Virus in Saliva with SiO2 - GLF.csv
    ├── 05142025 - Reconstructed Spectra for Each Concentration - Binary Mixture in Saliva with SiO2 - GLF.csv
    └── Reconstructed Spectra vs Actual Average Spectra - Saliva with SiO2 - GLF/
        └── *.png  (one figure per virus/mixture + concentration)
```

## 📝 File descriptions

### IPYNB files  
1. Each of the two `.ipynb` files in both `Virus_in_Water/` and `Virus_in_Saliva/` are used for calculating the linear decomposition coefficients and creating reconstructed vs real spectra plots. 

### CSV files  
1. Each of the two **test** `.csv` files in both `Virus_in_Water/` and `Virus_in_Saliva/` are used for linear decomposition. They have rows indexed by Raman shift (in cm⁻¹) and the following columns:

| Column name                          | Description                                                      |
| ------------------------------------ | ---------------------------------------------------------------- |
| `450, 451, ..., 1700`                | Measured average SERS intensity of corresponding Raman shift (cm⁻¹)|
| `Label`                              | Virus or mixture name                                              |
| `Conc`                               | Concentration of the virus, or concentration combination of the mixture |

2. Each of the two **Single Virus** `.csv` files in both `Virus_in_Water/` and `Virus_in_Saliva/` has rows indexed by Raman shift (in cm⁻¹) and the following columns:

| Column name                          | Description                                                      |
| ------------------------------------ | ---------------------------------------------------------------- |
| `Virus`                              | Virus name                                                       |
| `Concentration`                      | Concentration of the virus                                       |
| `450, 451, ..., 1700`                | Measured average SERS intensity of corresponding Raman shift (cm⁻¹)|

3. Each of the two **Binary Mixture** `.csv` files in both `Virus_in_Water/` and `Virus_in_Saliva/` has rows indexed by Raman shift (in cm⁻¹) and the following columns:

| Column name                          | Description                                                      |
| ------------------------------------ | ---------------------------------------------------------------- |
| `Virus_A`                            | Name of the first virus component                                |
| `Concentration_A`                    | Concentration of the first virus component                       |
| `Virus_B`                            | Name of the second virus component                               |
| `Concentration_B`                    | Concentration of the second virus component                      |
| `450, 451, ..., 1700`                | Measured average SERS intensity of corresponding Raman shift (cm⁻¹)|

### TXT files  
1. Each of the two `SiO2 - only GLF.txt` files in both `Virus_in_Water/` and `Virus_in_Saliva/` represent the SiO2 background spectrum.

2. The `05062025 - saliva (GLF 450-1700).txt` file in `Virus_in_Saliva/` represent the saliva background spectrum.

### PNG plots
Under each `Reconstructed Spectra vs Actual…` folder you’ll find one plot per concentration for each single virus, and one per concentration combination for each binary mixture. 

Each **Single Virus** figure shows:
1. **Blue solid line** – measured (average) spectrum for this concentration
2. **Yellow dashed line** – reconstructed spectrum for this concentration
3. **Green dash-dotted line** – pure (highest concentration) virus component spectra
4. **Purple dash-dotted line (only exists in saliva)** – saliva component spectra
5. **Grey dotted line** - SiO2 component spectrum

Each **Binary Mixture** figure shows:
1. **Blue solid line** – measured (average) spectrum for this concentration
2. **Yello dashed line** – reconstructed spectrum for this concentration
3. **Green dash-dotted line** – pure (highest concentration) virus_A component spectra
4. **Purple dash-dotted line** – pure (highest concentration) virus_B component spectra
5. **Orange dash-dotted line (only exists in saliva)** – saliva component spectra
6. **Grey dotted line** - SiO2 component spectrum
---

<!-- ## 🚀 Citation -->
<!-- If you use this dataset in your work, please cite: -->

<!--  J. Cui et al., “MultiplexCR: Deep learning for multi‐virus SERS quantification,” Journal of Raman Spectroscopy, 2025. DOI: 10.xxx/yyy -->

## ⚖️ License
This dataset is released under the MIT license.
