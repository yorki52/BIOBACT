# BIOBACT 🧬🧫
**The Ultimate Bacterial WGS Environment: From Raw Reads to Variants**

BIOBACT is a pre-configured, high-performance environment designed specifically for bacterial Whole Genome Sequencing (WGS). It bridges the gap between **de novo assembly** and **variant calling**, providing a seamless workflow for microbiologists and bioinformaticians.

## 🚀 Key Features
*   **Dual-Path Analysis:** Perform both *de novo* assembly and reference-based mapping in one environment.
*   **Modern Stack:** Includes the latest versions of industry-standard tools (GATK4, BWA-MEM2, SPAdes).
*   **Python Integration:** Pre-installed `pysam`, `pandas`, and `seaborn` for custom data munging and plotting directly in Jupyter.

## 🛠 Toolset (The BioBact Stack)

| Phase | Tools |
| :--- | :--- |
| **Preprocessing** | `fastp`, `FastQC`, `MultiQC` |
| **Assembly** | `SPAdes` (de novo), `QUAST` (evaluation) |
| **Mapping** | `BWA-MEM2`, `Samtools`, `Bedtools` |
| **Variant Calling** | `GATK4` (HaplotypeCaller), `FreeBayes`, `BCFtools` |
| **Annotation** | `snpEff` |

## 📦 Installation & Setup

### 1. Clone the repository
```bash
git clone https://github.com/yorki52/BIOBACT
cd BIOBACT
mamba env create -f biobact_env.yml
conda activate biobact
