# Bayesian Inference of the Antikythera Mechanism

This project applies Hamiltonian Monte Carlo (HMC) to infer the number and arrangement of holes in the calendar ring of the Antikythera mechanism—an ancient Greek astronomical calculator dated to ~100 BC. The aim is to understand whether the mechanism was based on a **solar (365-hole)** or **lunar (354-hole)** calendar by modeling X-ray data of surviving fragments.
---

## Summary

- Modeled the fractured calendar ring as a regular circular structure with sections allowed to rotate/translate independently
- Implemented two likelihood models:
  - Isotropic Gaussian error model
  - Radial/tangential anisotropic Gaussian error model
- Derived and implemented analytic gradients for the log-likelihood function
- Used HMC to sample the posterior distribution of key parameters (e.g. number of holes, ring radius, transformation parameters)
- Compared posterior predictions and model fits
---

## Data

- Public X-ray data and measured hole coordinates were provided by Thoeni et al. (see Reference [3])
- Data file include:
    - Measured hole posistions

## References

[1] Budiselic, Thoeni, Dubno & Ramsey,  
**Antikythera Mechanism Shows Evidence of Lunar Calendar**,  
*The Horological Journal*, March 2021  
[https://doi.org/10.31235/osf.io/fzp8u](https://doi.org/10.31235/osf.io/fzp8u)

[2] Woan & Bayley,  
**An Improved Calendar Ring Hole-Count for the Antikythera Mechanism: A Fresh Analysis**,  
*The Horological Journal*, July 2024  
[https://arxiv.org/abs/2403.00040](https://arxiv.org/abs/2403.00040)

[3] Thoeni, Budiselic & Ramsey,  
**Replication Data for: Antikythera Mechanism Shows Evidence of Lunar Calendar**,  
Harvard Dataverse, Version 3  
[https://doi.org/10.7910/DVN/VJGLVS](https://doi.org/10.7910/DVN/VJGLVS)

  - The public data
---
## Setup Instructions

### 1. Data

- `data.csv` should be placed in the `data/` folder. It contains the coordinates of hole locations across different sections of the Antikythera calendar ring.

### 2. Install Required Packages

Make sure you're using **Python 3.10 or higher**. Then install dependencies using:

```bash
pip install -r requirements.txt
```

## Acknowledgments

- This project was originally developed as part of a graduate-level advanced statistical method course at the University of Cambridge.
