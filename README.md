# TDA_Consonant_Recognition
Code material for Topological Data Analysis in Consonant Recognition. The data that support the findings of this study are openly available in SpeechBox, ALLSSTAR Corpus, L1-ENG division at [Home Page of SpeechBox](https://speechbox.linguistics.northwestern.edu/#!/home)

## Data Preprocessing
Using [Montreal Forced Aligner (MFA)](https://montreal-forced-aligner.readthedocs.io/en/latest/index.html) to align each speech into phonetic segments. To install MFA, simply try the following command:
```
conda create -n aligner -c conda-forge montreal-forced-aligner
```
The detailed installation of MFA can be found on the [Installation Page](https://montreal-forced-aligner.readthedocs.io/en/latest/installation.html). After installation, use `conda activate aligner` to activate the aligner environment. The following steps help align each speech into phonetic segments. See [Montreal Forced Aligner Tutorial](https://eleanorchodroff.com/tutorial/montreal-forced-aligner.html) for more explanations.

- Download the acoustic model and dictionary.
  ```
  mfa model download acoustic english_us_arpa
  mfa model download dictionary english_us_arpa
  ```
- Align speeches in the dataset, the output files are in `.TextGrid` format.
  ```
  mfa align ~/mfa_data/my_corpus english_us_arpa english_us_arpa ~/mfa_data/my_corpus_aligned
  ```
  



