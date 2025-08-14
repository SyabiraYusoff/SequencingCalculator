# Sequencing Calculator for BD Rhapsody™ Libraries

This web-based tool is tailored for BD Rhapsody™ Libraries. It helps users calculate the number of reads needed for sequencing based on various assay types, dependent on the final pooling concentration and volume needed by the sequencing facility.

The tool provides a user-friendly interface to input project details, select assay types, specify cell numbers, and reads per cell intended for sequencing. It then calculates the values from individual libraries for library normalization and the pooling volume from each respective normalized library. The tool also provides platform recommendations suitable based on the sequencing reads needed.

---

## 🚀 Usage

1. **Open** the tool in your browser.
2. **Enter** your memorable project name, username, and number of libraries (plexity).
3. **Fill in** the required library and assay details as prompted.
4. **Submit** to generate calculation tables and recommendations.
5. **Copy** results for record-keeping or further analysis (Excel/CSV).

---

## 📝 Features

- User-friendly interface with step-by-step instructions and tooltips.
- Dynamic table generation for up to 50 pooled libraries.
- Assay-specific recommendations and info buttons.
- Calculation of required reads, pooling ratios, dilution volumes, and normalization.
- Automatic correction factors for TCR/BCR and NovaSeqX and AVITI workflows.
- Warnings for low/high pipetting volumes and insufficient concentrations.
- Sequencer and platform recommendations based on user input.
- Copy results as HTML for Excel or as CSV.
- Feedback form for user suggestions.

---

## 🆕 Changelog

### Version 3.0.0

#### Features
- Added sample sheet recommendation table.
- Included AVITI sequencing recommendations.
- Added feedback form.
- Added Illumina MiSeq, NextSeq2000 p4, more NovaSeqX/X and AVITI  recommendation
- Removed HiSeq4000
- ATAC libraries can now be pooled with WTA and SMK, but only for AVITI sequencers.

#### Bug Fixes
- Unified correction factor for NovaSeqX and AVITI for VDJ.
- Added tooltips and info buttons for each table column and assay type.

---

### Version 2.0.0

#### Features
- Enter project name, username, and number of libraries (plexity) for pooling.
- Copy results to a CSV file for sharing.
- Visualize BD Rhapsody library structure.
- Sequencer recommendations included in the output.
- ATAC assay selection disables other assays to prevent pooling issues.

#### Bug Fixes
- Replaced "Save as PDF" with "Save to CSV."
- All rows for input table can now be removed.

---

## 🛠️ Pre-Release (Feb 2025)

### UI
- Responsive header design for different screen sizes.

### Technical
- Added 10% of Indexed library and Elution Buffer for pooling to consider pipetting error.
- Added index 7 and calculated Qubit nM conc to output table.
- Qubit Concentration tooltip is checked for each assay against the Excel calculator. WTA and ATAC have a 1 ng/µL cutoff. The rest have a 1.5 ng/µL cutoff.
- NOVASEQX: Added a message that the volume correction factor is set to 1 when using NOVASEQX.
- NOVASEQX: Only NOVASEQX sequencer recommendations are displayed in the recommendation table when the user checks the box.
- **If SMK libraries pipetting is lower than 1 µL, a warning is triggered. Recommendation: increase rpc or pipette carefully.**
- **If any Indexed libraries pipetting is above 20 µL, a warning is triggered. You are using the majority of your sample for dilution and pooling – so there might not be much leftover in case re-sequencing is needed.**
- Recommendation: Please consult with the sequencing provider for the possibility to reduce the final library concentration (nM).

---

## 🔄 Second Round Feedback (Jan 2025)

### Improvements
- Major restructure: Table input and output are now in a more concise format.
- PhiX and calculation have been tested and validated, and should be fully functional.
- Table for user input: Hover over the header for details. After an assay is selected, hover over the info button for assay-specific recommendations.
- The library can go as high as 50 libraries for pooling.
- If SMK is lower than 0.5 µL for pooling, a warning is triggered with a recommendation.
- If there aren’t enough indexed libraries, a warning is triggered with a recommendation.
- Customers can now remove libraries if needed (but not the last row).

### What We Keep
- The calculation for library dilution is back-calculated from the volume for pooling, meaning there’s no leftover of normalized library after pooling.
- The save PDF feature.
- The Information tabs feature.
- The retrospective calculation in the background, correction factor adjustment, and the PhiX percentage.
- If ATAC is selected, no other libraries can be selected, and vice versa.

---

## 📝 First Round Feedback (Dec 2025)

### Updates
- Update the section and add copy button to paste in Excel.

### Fixes
- Remove Save to PDF to avoid large file with increment of plexity.
- Row indexing strategy to match remove rows button.
- ATAC bioanalyser range correction.
