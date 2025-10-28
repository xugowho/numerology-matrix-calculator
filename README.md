# numerology-matrix-calculator
A computational numerology tool that generates and visualizes the personal Matrix of Destiny from a birth date, providing a structured analytical framework for exploring numerical patterns and symbolic relationships.

# Numerology Matrix Calculator

## Overview

The **Numerology Matrix Calculator** is a computational tool designed to generate and visualize the "Matrix of Destiny" based on an individual's birth date. This matrix is derived from classical numerological principles and combines elements of number reduction, karmic analysis, and symbolic interpretation through arcana representations. The repository provides both the computational algorithms and visualization tools for a clear, aesthetically pleasing representation of the numerological matrix.

The tool serves as a bridge between **numerical analysis, symbolic interpretation, and graphical representation**, offering both researchers and enthusiasts a means to study the relationships between birth date components and their derived numerological values.

---

## Theoretical Background

The Matrix of Destiny is constructed according to the following principles:

1. **Birth Date Input:** The user provides a birth date in the format `DD.MM.YYYY`.
2. **Day Reduction:** The day component is reduced to a value ≤22 by repeatedly summing its digits.
3. **Month Reduction:** The month is converted to a number between 1 and 12 (no additional reduction necessary unless desired for consistency).
4. **Year Reduction:** The year component is reduced by summing all its digits repeatedly until the result is ≤22.
5. **Karmic Number:** Calculated as the sum of the reduced day, month, and year numbers. If >22, it is further reduced.
6. **Comfort Point:** Calculated as the sum of day, month, year, and karmic numbers. If >22, it is further reduced.
7. **Corner Numbers:** Derived by summing adjacent diagonal square numbers of the main matrix. These are also reduced to ≤22 if necessary.
8. **Arcana Interpretation:** Optionally, each number can be associated with symbolic meanings loaded from a tab-separated file, providing general, central, and birth card interpretations.

This approach allows for both **quantitative reduction methods** and **qualitative symbolic interpretation**, creating a comprehensive framework for numerological analysis.

---

## Computational Implementation

The repository contains the following core components:

- **Input Processing:** Validates and parses the user's birth date into day, month, and year integers.
- **Reduction Function (`reduce_to_22`):** Public function to repeatedly sum digits until the number is ≤22. Implements the core reduction logic used for all subsequent calculations.
- **Matrix Calculation:** Computes main numbers (Top, Right, Bottom, Left, Center), karmic, comfort, and corner values.
- **Visualization:** Uses Matplotlib to generate a two-overlapping-squares (octagon) plot. Main numbers and corners are displayed as colored circles for clarity and aesthetic appeal.
- **Arcana Interpretation Loader:** Reads tab-separated text files mapping numbers to symbolic meanings, enabling detailed interpretations for research or personal insight.
- **Output:** Displays numerical results in the console and saves a publication-quality PNG image of the matrix with a title indicating the birth date.



---

## Usage

1. Open the Jupyter Notebook `matrix_calculator.ipynb`.
2. Run the first cell to input your birth date in `DD.MM.YYYY` format.
3. Execute subsequent cells sequentially to:
   - Calculate all numerological numbers
   - Generate the matrix visualization
   - Load and display arcana interpretations
4. The visualization will be saved automatically as a PNG file named according to the birth date (e.g., `Matrix_of_Destiny_15-04-1990.png`).

---

## Example

**Input:** `15.04.1990`  
**Output Matrix Values:**
- Top (Month): 4  
- Right (Year): 1  
- Bottom (Karmic): 6  
- Left (Day): 6  
- Center (Comfort): 7  
- Corners: 5, 7, 12, 10  

Visualization: two overlapping squares forming an octagon with colored circles, each number marked clearly in the plot.

Arcana interpretations are displayed in the console.

---

## Scientific Significance

The Numerology Matrix Calculator provides a **systematic framework for numerological research**, combining:

- **Mathematical reduction techniques** (digit summing, modulo reduction)
- **Karmic and comfort point calculations**
- **Geometric visualization of numerical relationships**
- **Symbolic interpretation via arcana mappings**

This approach allows researchers to explore patterns in birth dates, study symmetry in numerical matrices, and connect numerical structures to symbolic systems in a reproducible and verifiable computational environment.

---

## Requirements

- Python ≥3.7
- Matplotlib (for visualization)
- Jupyter Notebook (optional but recommended for interactive use)

---

## License

This repository is distributed under the MIT License. Users are free to use, modify, and share the code and data for research and educational purposes.

---

## References

1. PEP 257 – Python Docstring Conventions: https://www.python.org/dev/peps/pep-0257/  
2. Classical numerology texts on digit reduction and karmic calculations.  
3. Visualization and color-coding inspired by best practices in data representation.


