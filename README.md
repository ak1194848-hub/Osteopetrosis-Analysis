# Identification of a Causative Nonsense Mutation in the CA2 Gene for Osteopetrosis

## 1. Project Overview
This project demonstrates a complete clinical bioinformatics pipeline to identify the genetic cause of **Osteopetrosis** (Albers-Schönberg disease) in a pediatric patient. By analyzing Whole Exome Sequencing (WES) data, we successfully identified a rare, high-impact variant that explains the clinical phenotype.

## 2. Acknowledgments
The genomic data used in this project was provided for educational and research purposes by:
**Dr. Mohammed E. El-Asrag**
*Associate Professor in Medical Genomics and Bioinformatics*
*Aston University Medical School, UK.*
*Program Director - MSc & MRes Bioinformatics and Genomic Medicine.*

---

## 3. The Bioinformatics Pipeline
The analysis followed a rigorous clinical workflow:
1. **Mapping & Alignment:** Raw reads were aligned to the human reference genome (**hg19**) using `BWA-MEM`.
2. **Post-Alignment Processing:** Sorting and indexing were performed using `Samtools`.
3. **Variant Calling:** SNVs and Indels were called to generate a raw `VCF` file.
4. **Variant Annotation:** Functional annotation was performed using `SnpEff` to predict the biological impact of each variant.
5. **Filtering:** Variants were filtered based on:
   - Gene of interest (**CA2**).
   - Functional impact (**HIGH**).
   - Rarity and clinical relevance.

---

## 4. Key Findings: The "Smoking Gun"
The pipeline successfully isolated a critical variant:
- **Gene:** `CA2` (Carbonic Anhydrase II)
- **Location:** `chr8:86385980`
- **Mutation Type:** `Nonsense (Stop Gained)`
- **Protein Change:** `p.Trp97*` (Truncated protein)
- **Clinical Significance:** This mutation leads to a total loss of function of the Carbonic Anhydrase II enzyme, which is a known cause of Autosomal Recessive Osteopetrosis.

## 5. Visual Validation (Trio Analysis)
Using **Integrated Genomics Viewer (IGV)**, a Trio Analysis was performed to confirm the inheritance pattern:
- **Proband (Patient):** Homozygous for the mutation.
- **Father:** Heterozygous (Carrier).
- **Mother:** Heterozygous (Carrier).
*This confirms an **Autosomal Recessive** inheritance pattern.*

---

## 6. Tools Used
- **BWA-MEM:** Alignment.
- **Samtools:** BAM processing.
- **SnpEff:** Variant annotation.
- **IGV:** Visual inspection and validation.
- **Linux/Bash:** Data filtering and automation.
