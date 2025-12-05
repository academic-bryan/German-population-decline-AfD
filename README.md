# Population Decline and Far-Right Support in Germany

**Author:** Bryan Lockwald  
**Institution:** University of Nevada, Las Vegas  
**Dissertation Paper:** Part of three-paper dissertation

## Abstract

With the emergence of far-right populist parties throughout Europe, scholars are directing increasing amounts of attention to the politics of changing demographics.  Most of this work focuses on whether far-right political views are a response to immigration or the economy. This study examines the relationship between support for the AfD party municipalities with declining populations. Have municipalities that experience net declines of population exhibited more political support for far-right parties?  I explore this question with municipal-level and district level data on population and voting patterns in Germany using spatial econometrics. I use a Spatial Durbin Error Model to test for lacal and spill over effects I show that areas experiencing higher levels of net population decline exhibit more support for the AfD party, while controling for unemployment and the presence of foreignors

## Key Findings

- Strong positive correlation between population decline and AfD vote share growth
- East-West asymmetry: effects significantly stronger in former East Germany
- Direct effects present at both municipal and district levels
- Spatial spillover effects present at both municipal and district levels
- High spatial autocorrelation (λ ≈ 0.75-0.77)
- Patterns robust across geographic scales

## Repository Structure

This repository contains three interconnected RStudio projects:

1. **`Municipal_Level_Analysis/`** - Fine-grained analysis of ~8,300-9,500 municipalities
2. **`District_Level_Analysis/`** - Robustness checks at district level (~400 units)
3. **`German_Population_Decline/`** - Main paper integrating both analyses

See individual README files in each folder for detailed documentation.

## Reproducibility

### Prerequisites

- R (≥ 4.3.0)
- RStudio (≥ 2023.06.0)
- Quarto (≥ 1.3)

### Required R Packages
```r
install.packages(c(
  "tidyverse", "sf", "spdep", "spatialreg", "tmap",
  "gt", "here", "gerda", "restatis", "quarto"
))
```

Or use `renv` to restore exact package versions:
```r
renv::restore()
```

### Data Access

**Due to file size constraints, data files are not included in this repository.**

Data can be obtained from:
- **Election data:** [GERDA (German Electoral Research Data Archive)](https://github.com/awiedem/german_election_data)
- **Population data:** [Regional Statistics (Destatis)](https://www.regionalstatistik.de/)
- **Shapefiles:** [Federal Agency for Cartography and Geodesy](https://gdz.bkg.bund.de/)
- **Download Directly:** [RESTATIS R Package](https://github.com/CorrelAid/restatis)

See `Data_Download_Instructions.md` for step-by-step data acquisition guide.

### Running the Analysis
```bash
# 1. Clone the repository
git clone https://github.com/yourusername/german-population-decline-afd.git
cd german-population-decline-afd

# 2. Download data (see Data_Download_Instructions.md)
# Place data files in respective Data/ folders

# 3. Run municipal analysis
cd Municipal_Level_Analysis
# Open Municipal_Level_Analysis.Rproj in RStudio
# Run muncipal_level_analysis_V3_4_1.qmd

# 4. Run district analysis
cd ../District_Level_Analysis
# Open District_Level_Analysis.Rproj in RStudio
# Run district_level_analysis_1_2.qmd

# 5. Compile paper
cd ../German_Population_Decline
# Open German_Population_Decline.Rproj in RStudio
# Render German Population Decline and AfD.qmd
```

## Citation

If you use this code or data in your research, please cite:
```bibtex
@phdthesis{lockwald2025geography,
  title={Population Decline and Far-Right Support in Germany},
  author={Lockwald, Bryan},
  year={2025},
  school={University of Nevada, Las Vegas}
}
```

## License

This project is licensed under the MIT License - see [LICENSE](LICENSE) file for details.

## Contact

Bryan Lockwald  
PhD Candidate, Political Science  
University of Nevada, Las Vegas  
lockwald@unlv.nevada.edu | 

## Acknowledgments

- Committee members:
    - Chair: Dr. Christian Jensen
        Professor, Political Science Department, UNLV. christian.jensen@unlv.edu
    - Member: Dr. Michelle Kuenzi
        Professor, Political Science Department, UNLV. michele.kuenzi@unlv.edu
    - Member: Dr. Austin Wang
        Associate Professor, Political Science Department, UNLV. austin.wang@unlv.edu
    - Member: Dr. Tirth Bhatta
      Associate Professor of Sociology, Sociology Department, UNLV. tirth.bhatta@unlv.edu
      
- Data sources: GERDA, Destatis, BKG

- Dedicated to Neysa Lockwald who listened to everything.
- 
