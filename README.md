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



## 📦 Portable Version (No-Install Offline Archive)
If you don't have internet access or want to skip the `mamba` setup, you can download a pre-packaged portable version of the BIOBACT environment.

1. **Download the archive:** [Download BIOBACT Portable (tar.gz)]((https://disk.yandex.ru/d/OLsrTdnmfVJgmA))
2. **Extract to a folder:**
   mkdir biobact_env
   tar -xzf biobact_portable.tar.gz -C biobact_env
3. source biobact_env/bin/activate

# Ready to use! Test with: spades.py --version


## 📚 Citations & Tool References
If you use BIOBACT in your research, please cite the following tools:

### 🧬 Alignment & Mapping
*   **BWA / BWA-MEM2:** Li H. (2013) & Vasimuddin Md. et al. (2019). "Efficient Architecture-Aware Acceleration of BWA-MEM2." IEEE IPDPS.
*   **Samtools / BCFtools:** Danecek P. et al. (2021). "Twelve years of SAMtools and BCFtools." GigaScience.
*   **Bedtools:** Quinlan AR & Hall IM. (2010). "BEDTools: a flexible suite of utilities for comparing genomic features." Bioinformatics.

### 🔍 Variant Calling
*   **GATK4:** Van der Auwera GA & O'Connor BD. (2020). "Genomics in the Cloud." O'Reilly Media.
*   **FreeBayes:** Garrison E & Marth G. (2012). "Haplotype-based variant detection from short-read sequencing." arXiv:1207.3907.

### 🧱 Assembly & Evaluation
*   **SPAdes:** Prjibelski A. et al. (2020). "Using SPAdes De Novo Assembler." Current Protocols in Bioinformatics.
*   **QUAST:** Gurevich A. et al. (2013). "QUAST: quality assessment tool for genome assemblies." Bioinformatics.

### 📊 Quality Control
*   **FastQC:** Andrews S. (2010). "FastQC: A Quality Control Tool for High Throughput Sequence Data."
*   **fastp:** Chen S. et al. (2018). "fastp: an ultra-fast all-in-one FASTQ pre-processor." Bioinformatics.
*   **MultiQC:** Ewels P. et al. (2016). "MultiQC: summarize analysis results for multiple tools and samples in a single report." Bioinformatics.

PyOrthoANI: Larralde M, Zeller G, Carroll LM. (2025). "PyOrthoANI, PyFastANI, and Pyskani: a suite of Python libraries for computation of average nucleotide identity." NAR Genomics and Bioinformatics.
OrthoANI (Original Algorithm): Lee I, et al. (2016). "A proposed system for the taxonomic identification of prokaryotes using whole genome sequences." Int J Syst Evol Microbiol.
Shovill: Seemann T, "Fast bacterial assembly".
Prokka: Seemann T. (2014) "Prokka: rapid prokaryotic genome annotation", Bioinformatics.
Abricate: Seemann T, "Mass screening of contigs for AMR and virulence genes".
