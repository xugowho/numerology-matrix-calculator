# Matrix of Destiny Visualization and Arcana Interpretation

## Project Overview

The **Numerology Matrix Calculator** is a computational tool designed to generate and visualize the "Matrix of Destiny" based on an individual's birth date. This matrix is derived from classical numerological principles and combines elements of number reduction, karmic analysis, and symbolic interpretation from special dataset through arcana representations. The repository provides both the computational algorithms and visualization tools for a clear, aesthetically pleasing representation of the numerological matrix.

The tool serves as a bridge between **numerical analysis, symbolic interpretation, and graphical representation**, offering both researchers and enthusiasts a means to study the relationships between birth date components and their derived numerological values.

---

## Features

* Calculates numerological numbers based on the date of birth
* Computes main matrix numbers: Top, Right, Bottom, Left, Center
* Calculates corner numbers for the large square
* Visualizes the Matrix of Destiny
* Reads arcana interpretations from a tab-separated file (`matrix_interpretation.txt`)
* Outputs detailed interpretations for:

  * Center
  * Portrait (Left corner)
  * Other numbers

---


## Theoretical Background

The Destiny Matrix is a numerological model based on your date of birth. It combines mathematical reduction (summing and reducing digits to a number ≤ 22) with symbolic meanings from the 22 Major Arcana of Tarot cards.
Each zone of the matrix reflects a specific area of your life from your visible personality to your inner purpose and karmic lessons.

### Diamond

| Position   | Name                  | Meaning                                  | Number 
| ---------- | --------------------- | ---------------------------------------- | --------------
| **Center** | Comfort / Core Energy | Soul essence, inner peace, life purpose. | Day + month + year + Spiritual Karma
| **Left**   | Portrait              | How others see you, social image.        | Day
| **Top**    | Hidden Talents        | Natural gifts and potential.             | Month
| **Right**  | Material Karma        | Financial or practical challenges.       | Year
| **Bottom** | Spiritual Karma       | Past-life lessons to resolve.            | Day + month + year


### Square (Ancestral Programs)

| Position         | Meaning                     |
| ---------------- | --------------------------- |
| **Top Left**     | Father’s spiritual lineage. |
| **Top Right**    | Mother’s spiritual lineage. |
| **Bottom Left**  | Father’s material lineage.  |
| **Bottom Right** | Mother’s material lineage.  |

Each corner = sum of two nearby sides.

---

## Input Data Format

1. **Birth Date** – entered as `DD.MM.YYYY`
   Example:

   ```
   12.12.2012
   ```

2. **Arcana Interpretation File (`matrix_interpretation.txt`)** – tab-separated values with columns in folder `data\`:

   ```
   number |	name |	general meaning	| central meaning	| outer expression
   ...
   ```
Meanings:
   * `number` – numeric identifier
   * `name` – arcana name
   * `general meaning` – general interpretation
   * `central meaning` – meaning for the central number
   * `outer expression` – meaning for portrait
---

## Output

The program outputs:

* **Matrix Visualization** saved as a PNG file (`Matrix_of_Destiny_{DD-MM-YYYY}.png`)
* **Arcana Interpretation** in the console, including:

  * Center: number, name, center-specific value
  * Birth Card (Left): number, name, potrait value
  * Other main sides: number, name, general value
  * Big square corners: number, name, general value

Example output:

```
=== ARCANA INTERPRETATION ===

Center: 11 - Strength  - As a core energy, this Arcanum represents self-mastery and emotional intelligence. The main task is to harmonize passion with reason, expressing strength through empathy. 
Birth Card (Left): 20 - Judgement  - Outwardly serious, insightful, and dignified. Often carries an aura of purpose or moral depth. Speech and posture convey gravity and awareness. 


Other main Arcanas:
9 - The Hermit  - Symbol of solitude, introspection, and pursuit of truth. Associated with wisdom, patience, and spiritual maturity. 
8 - Justice  - Symbolizes fairness, balance, law, and moral accountability. Represents evaluation and rational clarity. 
10 - Wheel of Fortune  - Represents destiny, cycles, and transformation through chance. Symbol of life’s impermanence and karmic rhythm. 

Big Square Corners:
Corner 1 : 17 - The Star  - Represents hope, inspiration, and spiritual rejuvenation. Symbol of idealism, faith, and gentle creativity. 
Corner 2 : 18 - The Moon  - Symbol of emotion, imagination, illusion, and subconscious influence. Represents intuition and hidden fears. 
Corner 3 : 3 - The Empress  - Embodies abundance, beauty, and creative manifestation. Symbol of nurturing energy, growth, and natural prosperity. Reflects harmony between material and emotional fulfillment. 
Corner 4 : 11 - Strength  - Embodies inner courage, endurance, and compassionate control over instincts. Represents calm power and moral fortitude. 
```

---

## How to Use

1. Place the Python script and `matrix_interpretation.txt` in the **same folder**.
2. Run the script in Python 3.8+ or in Jupyter Notebook.
3. Enter your birth date when prompted (`DD.MM.YYYY`).
4. The program will automatically:

   * Calculate all matrix numbers and corners
   * Visualize the Matrix of Destiny as a PNG file
   * Print arcana interpretations for center, birth card, other sides, and corners

---

## Test

For testing, use the provided `matrix_interpretation.txt` dataset. 

1. Run the script.
2. Verify that `Matrix_of_Destiny_{DD-MM-YYYY}.png` is generated and compare to image from `data\example`

---

## Authors

| GitHub       | Name                 | Role                     |
| ------------ | -------------        | ------------------------ |
| mariika1306  |	Vlasova Maria       | Co-author & Developer     |
| xugowho	     | Demchenko Alexander |	Co-author & Developer     |
| aadergileva	 | Dergileva Anastasia |	Co-author & Developer     |
> Project developed independently. All code, formulas, interpretations and visualizations are original.

## License

This repository is distributed under the MIT License. Users are free to use, modify, and share the code and data for research and educational purposes.
