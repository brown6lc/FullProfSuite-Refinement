# FullProf Suite Guide  
## Rietveld and LeBail Refinement of XRD Data

This repository contains a step-by-step guide for performing **Rietveld refinement** and **LeBail refinement** of X-ray diffraction (XRD) data using the **FullProf Suite**. The included documentation explains data preparation, PCR file generation, refinement configuration, and extraction of refined lattice parameters.

The FullProf Suite software can be downloaded at this link:
https://www.ill.eu/sites/fullprof/downloads.html

---

## 📁 Contents
- **FullProfGuide_revised.pdf** – Complete illustrated tutorial for:
  - Formatting and preparing XRD data
  - Background point selection using WinPlotr
  - CIF-to-PCR conversion
  - Pre-refinement configuration
  - Rietveld refinement procedure
  - LeBail refinement steps
  - Extracting lattice constants and uncertainties

---

## 🧪 Workflow Overview

### 1. Data Formatting & Background Subtraction
Format XRD data into a `.dat` file with two columns: **2θ** and **intensity**.  
Use WinPlotr to select background points and save them as a `.BGR` file.

### 2. Creating a PCR File from a CIF
Download a CIF file (e.g., from the Crystallography Open Database) and convert it into a PCR file using the **CIF → PCR** tool inside EdPCR.

### 3. Pre-Refinement Configuration
Configure:
- General calculation options  
- Data file format and pattern settings  
- Peak shape parameters  
- Background function  
- Phase information and contributions

### 4. Running Rietveld Refinement
Import background points, set instrumental parameters (including zero correction), verify profile settings, and run the refinement. Example output is shown in the guide.

### 5. Running LeBail Refinement
Duplicate the refinement directory and:
1. Run LeBail with constant scale factor.  
2. Create a second subfolder and refine again with asymmetry and X-parameter enabled.

This two-step approach helps stabilize lattice parameter extraction.

### 6. Extracting Lattice Parameters
Open the output results file in the LeBail subfolder and locate the **Cell Parameters** section.  
The lattice constants and associated errors are listed there.

---

## 🛠 Requirements
- **FullProf Suite**
- Powder XRD data (converted to `.dat`)
- CIF file for the target compound

---

This guide is intended for students, researchers, and scientists working on powder XRD analysis and requires no prior experience with FullProf. It provides a complete workflow for both structural refinement and profile fitting.


