# massage-therapy-corpus
This repository contains the oral and written subcorpora used in:

**An AI-Driven Tutoring Intervention for Massage Therapy Education: Corpus Design and Implementation Evaluation**
*José Rivera Moreno, NRC 42137 Discourse Analysis, 2026*

## File Formats

All files are plain text (`.txt`) encoded in UTF-8.

## Corpus Linguistics Replication Guide

This repository contains the complete empirical data assets for the case study analyzing register variation 
in Massage Therapy (MT) education and professional discourse. By utilizing the provided text datasets and 
corpus outputs across our specialized branches, researchers can fully replicate, verify, and audit all statistical findings,
log-likelihood profiles, and n-gram matrices presented in the main paper.Repository & Branch ArchitectureThe structural 
assets of this study are partitioned directly into the following branch locations underneath this main directory:

### Contents

- `oral/` – Contains the raw instructional spoken transcripts (.txt) compiled from video media and classroom tutorials. (YouTube sources)
- `written/` – Contains the 10 preprocessed full-text clinical reference texts (.txt) utilized for the written register baseline
- `further analysis/` – Positioned right below the root directory, this branch hosts the post-hoc exported statistical spreadsheets, keyword outputs, and keyness comparative archives
- `README.md` – This file

### Step-by-Step Replication Pipeline 

#### Phase 1: Environment Setup & Target Ingestion

Download and install AntConc (Version 4.x) or any standard 
corpus analysis software. Clone or download the raw target files from the oral corpus branch and load them into 
AntConc's primary corpus slot. Open a secondary workspace or reference slot and load the 10 preprocessed texts 
from the written corpus branch. (Note: All digital metadata, URLs, DOIs, citation hashes, and secondary multilingual
strings have already been preprocessed out of these files to isolate purely scope-relevant vocabulary).

#### Phase 2: N-Gram and Lexical Bundle Generation 

Navigate to the N-Grams tool within AntConc. Set the N-gram size parameters 
to Min: 3, Max: 4 to isolate 3-word and 4-word lexical bundles. Run the generation tool independently for both the
oral and written subcorpora. Sort the results by Frequency and Range (dispersion across sub-texts). Cross-reference 
the resulting lists against the data tables in the paper to verify the structural behavior of core anchors such as
just, massage, back, were, going, and by.

#### Phase 3: KWIC Concordance Auditing

Navigate to the KWIC (Key Word in Context) tool.Enter the target anchor tokens 
individually (e.g., searching for the token welcome, massage, or back).Set the window span to view 5 words to the left 
and 5 words to the right.Observe the immediate collocational environments to verify the presence of "academic 
shields" (such as the fixed binomial “massage therapy and bodywork”) and prepositional frames that govern institutional 
boundary tracking.

#### Phase 4: Reference Keyness Benchmarking

To replicate the exact Log-Likelihood ($G^2$) surges reported in the text (e.g., were: 2087.417; by: 1781.773; welcome: 18.246), open the 
Corpus Manager settings in AntConc. Select and configure yourstandard reference baseline by choosing the built-in balanced sample 
from the Corpus of Contemporary American English (COCA). Generate the keyword parameters using the Log-Likelihood algorithm 
to calculate statistical salience alongside an effect-size coefficient. Navigate to the further analysis branch to open the exported 
keyness archives. Verify that all targeted professional/clinical tokens surpass the absolute significance threshold of $15.13$ ($p < 0.0001$).

#### Pedagogical Translation Application
The multi-word lexical bundles and structural realignments extracted in this pipeline (such as converting active agent speech into passive clinical frames) serve as the direct empirical foundation for teaching professional-business register awareness. By mapping these localized data strings 
to Biber’s Dimension 5 (Abstract vs. Non-Abstract Style), educators can inductively scaffold a learner's transition from 
casual instructional talk to formal clinical and commercial charting proficiency.

## Citation

If you use this corpus in your research, please cite: Rivera-Moreno, J. (2026). Evaluating an AI-driven tutoring intervention for register variation in massage therapy education: A corpus-guided case study [Unpublished manuscript]. Maestría Profesional de Lingüística Aplicada, Universidad Nacional

## Data DOI

[Zenodo DOI will appear here after archiving]

Zenodo. https://doi.org/10.5281/zenodo.20535483

## License

Creative Commons Attribution 4.0 International (CC BY 4.0)
