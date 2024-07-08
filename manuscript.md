---
title: Multi-Dataset Integration and Residual Connections Improve Proteome Prediction from Transcriptomics Using Deep Learning
keywords:
- markdown
- publishing
- manubot
lang: en-US
date-meta: '2024-07-08'
author-meta:
- Caleb W. Cranney
- Jesse G. Meyer
header-includes: |
  <!--
  Manubot generated metadata rendered from header-includes-template.html.
  Suggest improvements at https://github.com/manubot/manubot/blob/main/manubot/process/header-includes-template.html
  -->
  <meta name="dc.format" content="text/html" />
  <meta property="og:type" content="article" />
  <meta name="dc.title" content="Multi-Dataset Integration and Residual Connections Improve Proteome Prediction from Transcriptomics Using Deep Learning" />
  <meta name="citation_title" content="Multi-Dataset Integration and Residual Connections Improve Proteome Prediction from Transcriptomics Using Deep Learning" />
  <meta property="og:title" content="Multi-Dataset Integration and Residual Connections Improve Proteome Prediction from Transcriptomics Using Deep Learning" />
  <meta property="twitter:title" content="Multi-Dataset Integration and Residual Connections Improve Proteome Prediction from Transcriptomics Using Deep Learning" />
  <meta name="dc.date" content="2024-07-08" />
  <meta name="citation_publication_date" content="2024-07-08" />
  <meta property="article:published_time" content="2024-07-08" />
  <meta name="dc.modified" content="2024-07-08T20:56:31+00:00" />
  <meta property="article:modified_time" content="2024-07-08T20:56:31+00:00" />
  <meta name="dc.language" content="en-US" />
  <meta name="citation_language" content="en-US" />
  <meta name="dc.relation.ispartof" content="Manubot" />
  <meta name="dc.publisher" content="Manubot" />
  <meta name="citation_journal_title" content="Manubot" />
  <meta name="citation_technical_report_institution" content="Manubot" />
  <meta name="citation_author" content="Caleb W. Cranney" />
  <meta name="citation_author_institution" content="Department of Computational Biomedicine, Cedars Sinai Medical Center" />
  <meta name="citation_author_orcid" content="0000-0001-8482-758X" />
  <meta name="twitter:creator" content="@CalebCranney" />
  <meta name="citation_author" content="Jesse G. Meyer" />
  <meta name="citation_author_institution" content="Department of Computational Biomedicine, Cedars Sinai Medical Center" />
  <meta name="citation_author_orcid" content="0000-0003-2753-3926" />
  <meta name="twitter:creator" content="@j_my_sci" />
  <link rel="canonical" href="https://xomicsdatascience.github.io/transcriptome-proteome-nas-manubot/" />
  <meta property="og:url" content="https://xomicsdatascience.github.io/transcriptome-proteome-nas-manubot/" />
  <meta property="twitter:url" content="https://xomicsdatascience.github.io/transcriptome-proteome-nas-manubot/" />
  <meta name="citation_fulltext_html_url" content="https://xomicsdatascience.github.io/transcriptome-proteome-nas-manubot/" />
  <meta name="citation_pdf_url" content="https://xomicsdatascience.github.io/transcriptome-proteome-nas-manubot/manuscript.pdf" />
  <link rel="alternate" type="application/pdf" href="https://xomicsdatascience.github.io/transcriptome-proteome-nas-manubot/manuscript.pdf" />
  <link rel="alternate" type="text/html" href="https://xomicsdatascience.github.io/transcriptome-proteome-nas-manubot/v/d9b5c2384ee5252dca923b2d2c0e81839f05bfd4/" />
  <meta name="manubot_html_url_versioned" content="https://xomicsdatascience.github.io/transcriptome-proteome-nas-manubot/v/d9b5c2384ee5252dca923b2d2c0e81839f05bfd4/" />
  <meta name="manubot_pdf_url_versioned" content="https://xomicsdatascience.github.io/transcriptome-proteome-nas-manubot/v/d9b5c2384ee5252dca923b2d2c0e81839f05bfd4/manuscript.pdf" />
  <meta property="og:type" content="article" />
  <meta property="twitter:card" content="summary_large_image" />
  <link rel="icon" type="image/png" sizes="192x192" href="https://manubot.org/favicon-192x192.png" />
  <link rel="mask-icon" href="https://manubot.org/safari-pinned-tab.svg" color="#ad1457" />
  <meta name="theme-color" content="#ad1457" />
  <!-- end Manubot generated metadata -->
bibliography:
- content/manual-references.json
manubot-output-bibliography: output/references.json
manubot-output-citekeys: output/citations.tsv
manubot-requests-cache-path: ci/cache/requests-cache
manubot-clear-requests-cache: false
...






<small><em>
This manuscript
([permalink](https://xomicsdatascience.github.io/transcriptome-proteome-nas-manubot/v/d9b5c2384ee5252dca923b2d2c0e81839f05bfd4/))
was automatically generated
from [xomicsdatascience/transcriptome-proteome-nas-manubot@d9b5c23](https://github.com/xomicsdatascience/transcriptome-proteome-nas-manubot/tree/d9b5c2384ee5252dca923b2d2c0e81839f05bfd4)
on July 8, 2024.
</em></small>



## Authors



+ **Caleb W. Cranney**
  <br>
    ![ORCID icon](images/orcid.svg){.inline_icon width=16 height=16}
    [0000-0001-8482-758X](https://orcid.org/0000-0001-8482-758X)
    · ![GitHub icon](images/github.svg){.inline_icon width=16 height=16}
    [CCranney](https://github.com/CCranney)
    · ![Twitter icon](images/twitter.svg){.inline_icon width=16 height=16}
    [CalebCranney](https://twitter.com/CalebCranney)
    <br>
  <small>
     Department of Computational Biomedicine, Cedars Sinai Medical Center
     · Funded by Grant R35GM142502, National Institute of General Medical Sciences (NIGMS)
  </small>

+ **Jesse G. Meyer**
  <br>
    ![ORCID icon](images/orcid.svg){.inline_icon width=16 height=16}
    [0000-0003-2753-3926](https://orcid.org/0000-0003-2753-3926)
    · ![GitHub icon](images/github.svg){.inline_icon width=16 height=16}
    [jessegmeyerlab](https://github.com/jessegmeyerlab)
    · ![Twitter icon](images/twitter.svg){.inline_icon width=16 height=16}
    [j_my_sci](https://twitter.com/j_my_sci)
    <br>
  <small>
     Department of Computational Biomedicine, Cedars Sinai Medical Center
  </small>


::: {#correspondence}
✉ — Correspondence possible via [GitHub Issues](https://github.com/xomicsdatascience/transcriptome-proteome-nas-manubot/issues)

:::


## Abstract {.page_break_before}

Proteomes are well known to poorly correlate with transcriptomes measured from the same sample. 
While connected, the complex processes that impact the relationships between transcript and protein quantities remains an open research topic. 
Many studies have attempted to predict proteomes from transcriptomes with limited success. 
Here we use publicly available data from the Clinical Proteomics Tumor Analysis Consortium to show that deep learning models designed by neural architecture search (NAS) achieve improved prediction accuracy of proteome quantities from transcriptomics. 
We find that this benefit is largely due to including a residual connection in the architecture that allows input information to be remembered near the end of the network. 
Finally, we explore which groups of transcripts are functionally important for protein prediction using model interpretation with SHAP.

## Introduction {.page_break_before}

The central dogma of biology posits a linear flow of information from genetic encoding to mRNA transcripts to functional proteins. 
However, this seemingly straightforward relationship belies a more intricate reality, where the interactions between omic layers are multifaceted and complex. 
Elucidating these relationships is crucial for understanding biological systems in both healthy and diseased states. 
By disentangling these interactions, researchers can identify markers and patterns specific to complex diseases, ultimately enabling the development of targeted treatments. 

Among the multi-omic data type relationships, the connection between transcripts and their corresponding proteins is particularly enigmatic. 
Despite being quantifiable and having a direct derivative relationship, their relative quantities often exhibit only weak correlations [@DOI:10.1128/mcb.19.3.1720], [@DOI:10.1016/j.tibs.2014.10.010]. 
Research has identified several possible causes for this discrepancy, including alternate rates of protein generation and decay [@DOI:10.1038/nrg3185], [@DOI:10.1093/dnares/dsn030], [@DOI:10.1126/science.1160489], varying reactions to environmental stimuli [@DOI:10.1016/j.cell.2016.03.014], [@DOI:10.1128/ec.01.1.22-32.2002], or simply systematic experimentation error bias [@DOI:10.1016/j.crmeth.2022.100288], [@DOI:10.26508/lsa.202201885]. 
Recent works have even found that the most predictive transcripts of a protein include those that are involved in protein-protein interactions [@DOI:10.1371/journal.pcbi.1010702]. 
While predicting protein quantity through direct transcript-to-protein correlation remains elusive, using contextual transcript information may reveal more complex proteomic-transcriptomic relationships that could be leveraged to predict one from the other. 
Moreover, predicting proteins from transcripts could reduce the time and financial costs associated with future studies, as transcript quantification is generally easier to accomplish than protein quantification [@DOI:10.1038/s41467-020-16937-8]. 

The National Cancer Institute's (NCI) Clinical Proteomic Tumor Analysis Consortium (CPTAC) provides a valuable resource for exploring this issue, offering multi-omic datasets that enable research into healthy and cancerous disease states [@url:https://proteomics.cancer.gov/programs/cptac]. 
Specifically, CPTAC datasets comprise transcriptomic and proteomic data (among others) from various cancer types and adjacent healthy tissue, which makes this data useful for detection of inter-omic relationships. 
Several research collaborations have occurred to use this data to study RNA-protein relationships. 
The 2017 NCI-CPTAC DREAM Proteogenomics challenge [@url:https://dreamchallenges.org/nci-cptac-dream-proteogenomics/], a sub challenge of which aimed to predict protein quantities from transcript abundance, is a notable example. 
Contestants used a variety of methods, including random forest regression, genetic models, spline regression, linear regression, and elastic net methods, as well as ensemble combinations [@DOI:10.1186/s12859-019-3253-z]. 
Using a test set only from breast cancer and ovarian cancer, the winning model achieved a pearson correlation of 0.41 and 0.47 between the true and predicted protein quantities, respectively [@DOI:10.1186/s12915-019-0730-9]. 
Notably, deep learning neural networks were not strongly represented in the challenge results. 

Since the close of the challenge, research into deep learning has expanded significantly, with a focus on replicating human behaviors like computer vision and natural language processing (NLP). 
However, the underlying principles of deep learning are equally applicable to biological data [@DOI:10.1038/s42256-020-0217-y], [@DOI:10.1093/bib/bbw068], [@DOI:10.2174/1574893615999200711165743]. 
The key challenge lies in developing a model architecture that best fits a given problem. 
One underutilized strategy for deep learning model design is the NAS [@DOI:10.1145/3447582]. 
NAS serves a function like hyperparameter tuning, in that a range of values for specific hyperparameters are evaluated to obtain the optimal configurations. 
In the case of NAS, the concept is expanded to include model architecture in addition to hyperparameters, designing optimal and unique model architectures in an automated fashion. 
While NAS has been applied to genomic data [@DOI:10.1038/s42256-021-00316-z], its application to predicting proteomic data from transcriptomic data remains unexplored. 

We previously showed how machine learning can accurately predict the metabolome from the proteome, and how model interpretation revealed important biological insights [@DOI:10.1093/bioinformatics/btac631]. 
Here, we extend that work to transcript-to-protein deep learning prediction models and demonstrate that utilizing NAS improved the accuracy. 
Furthermore, we highlight the potential of model interpretation to identify patterns in transcript-protein relations that underpin biological processes characteristic of a disease state.	 

## Methods {.page_break_before}

### Data Acquisition and Preprocessing 

To facilitate readability and reproducibility, the code for downloading, processing, and splitting data was developed as a multi-class in-house package. 
The bridge design pattern specifically was used to allow for interchangeability of data source input to expand beyond CPTAC in the future, as well as for allowing custom processing and splitting depending on the experiment. 
This involved writing an abstract parent data processing class, and individual child classes would utilize compartmentalized class components specific to the experiment. 
This was done to enable external researchers to trace data processing workflows with ease. 

CPTAC data was downloaded directly from zenodo using the cptac python package [@DOI:10.1021/acs.jproteome.0c00919] separately for each cancer type. 
Analyses were only performed using transcripts and proteins common between all datasets. 

Cancer-specific datasets were normalized independently of one another. 
For experiments where each dataset required an identical train-validation split, this normalization was calculated on the training partition then applied to the training and validation partitions both. 
For the five by two cross validation experiments, it was determined that dataset-specific analyses would be enhanced by the inclusion of all other datasets in the training dataset [Supplementary Figure 1]. 
In these instances, the train-validation split was applied only to the target dataset, with a split of 0.45, 0.45, and 0.1 for training, validation and testing, respectively. 
All non-target datasets were normalized on the entire dataset as the training partition, ignoring validation or testing partitioning entirely. 
In a standard data partition, each dataset had a split of 0.8, 0.1 and 0.1 for training, validation and testing, respectively. 

The final dataset contained data for breast cancer (BRCA), kidney cancer (CCRCC), colon cancer (COAD), brain cancer (GBM), squamous cell cancer (HNSCC), lung cancer (LSCC and LUAD), ovarian cancer (OV), and pancreatic cancer (PDAC) as well as adjacent healthy tissue. 
59286 transcripts and 7822 proteins were shared across all datasets with a combined number of 1256 samples.  

### NAS

The search space used in this study chose a model architecture consisting of three segments, or blocks, of sub-architectures. 
These blocks could vary in number of neurons, number of layers, activation functions between layers, intra-block residual connections, dropout rates, or be removed entirely to simplify the network. 
It was determined that while mRNA to encoded protein quantities are not directly correlated, the quantity of one likely has a strong impact on the quantity of the other. 
Thus, the search space also included a residual connection inserting mRNA input quantities for proteins being predicted right before the final output layer of the network. 

The NAS workflow was based on the “Multi-Objective NAS with Ax” workflow tutorial on the official pytorch website [@url:https://pytorch.org/tutorials/intermediate/ax_multiobjective_nas_tutorial.html], utilizing Meta’s Ax package to do so. 
The process includes designing a search space as a separate python script that accepts variables that dictate the model structure, setting up a torchx runner and scheduler for submitting model training scripts concurrently, and defining optimization requirement configurations. 
Ax uses Bayesian optimization to evaluate and compare model configurations and their predictive accuracy, highlighting the impact specific architecture decisions have on the final loss. 

### Model Evaluation and Comparison 

Losses between predicted and true outputs were calculated using mean-squared error. 
The dummy regressor identified the mean of the true output data and used it as the prediction of all data points. 
The random forest regressor was run with log2 max feature and 50 node max depth limitations, as the number of inputs and outputs in creating a forest of full trees would otherwise require upwards of years to calculate. 
The manually designed model consisted of two hidden layers with output sizes of 12k, and 10k, respectively. 
Hidden layers employed batch normalization, a dropout rate of 0.6, and used the leaky ReLU activation function with a negative slope of 0.05 [Supplementary Figure 2]. 
The NAS-optimized model consisted of three blocks of layers, followed by a single output layer. 
The first block consisted of a single neural layer with 319 neurons, a sigmoid activation function, a dropout rate of 0.52. 
The second block consisted of three neural layers with 508 neurons, a sigmoid activation function, a dropout rate of 0.69, and a residual connection skipping the middle layer. 
The third block consisted of a single neural layer with 7822 neurons (the output size), a tanh activation function, and a dropout rate of 0.9. 
The optimal model also sported a batch size of 128 and a learning rate of 1e-4. 

### Model Interpretation Using SHAP Values 

SHAP values [@url:http://papers.nips.cc/paper/7062-a-unified-approach-to-interpreting-model-predictions.pdf] were calculated using all available samples from CPTAC used in training and validation of the optimal model, which included the direct transcript residual connection. 
SHAP values for the top 13 accurately predicted proteins across cancers using the NAS optimized model were extracted and graphed independently, specifically CAVIN1, FERMT2, FLNA, HCLS1, TK3, MCM3, MCM4, MCM6, P4HB, PTPN6, SMC2, STAT1, and VCL. 
MMP14 was included as a candidate because of its role in cancer regulation. 
SHAP values for targeted proteins were extracted and analyzed independently of the raw SHAP outputs for memory efficiency purposes. 

Direct transcripts were determined by directly matching gene names to the list of predicted proteins. 
A cutoff of -15 mean absolute SHAP value was chosen to separate correlated and uncorrelated transcripts. 
Transcripts that had an absolute mean SHAP value above -15 in at least 70% of the chosen proteins were determined to belong to the correlated category. 
Transcripts that had a null or 0 SHAP value were excluded from categorization. 

A SHAP analysis was also run on 3 variations of the optimal model, specifically models with no input residual connection, a correlated transcript residual connection, and an uncorrelated transcript residual connection. 
To accommodate residual connections of varying lengths, the output size of the third block and the input size of the final output layer were altered to match the size of the residual connection for these adjustments. 

### Code Availability

CPTAC data was downloaded using the cptac python package [@DOI:10.1021/acs.jproteome.0c00919]. 
All models were developed using Pytorch [@DOI:10.1145/3620665.3640366] and Pytorch Lightning [@url:https://github.com/Lightning-AI/pytorch-lightning]. 
NAS was implemented with Meta’s Adaptive Experimentation Platform (Ax) [@url:https://github.com/facebook/Ax]. 
NAS evaluation metrics were tracked with tensorboardX [@url:https://github.com/lanpa/tensorboardX]. 
Scikit-learn was used to perform train-validation splits and several non-neural net regression models [@url:http://jmlr.org/papers/v12/pedregosa11a.html]. 
Pandas was used to load, process and save CPTAC data [@DOI:10.5281/zenodo.3509134]. Numpy was used to perform various calculations [@DOI:10.1038/s41586-020-2649-2]. 
SHAP was performed with the shap python package [@url:http://papers.nips.cc/paper/7062-a-unified-approach-to-interpreting-model-predictions.pdf]. 

Code for data processing and model training and evaluation can be found at [https://github.com/xomicsdatascience/RnaToProteinDataModule]. 
Classes for data processing and model generation can be found in the src directory, while scripts for running the different experiments can be found in the scripts directory. 

### Large Language Model Edit

This paper was refined for human readability using Meta’s Llama 3 Large Language Model [@url:https://ai.meta.com/blog/meta-llama-3/]. 

## Results {.page_break_before}

### CPTAC Model Configuration

The CPTAC dataset provides a unique opportunity to investigate the relationships between multi-omic layers, particularly in predicting the proteome from transcriptome data [Figure 1A]. 
A range of approaches were employed to achieve this, including one-to-one mapping of mRNA transcripts to proteins compared with various regressors: dummy, linear, random forest, and neural networks [Figure 1B]. 
The latter proved to be the most variable, with different architectures yielding diverse predictive accuracies. 
To address this, a NAS was utilized to automate the selection of optimal neural network architectures [Figure 1C]. 
The NAS approach iteratively evaluated various model architectures from a search space to identify the most effective structure for predicting protein quantities from transcriptome data [Figures 1C, 1D]. 
The optimal NAS model was benchmarked against other models, including a dummy regressor, and its performance was evaluated using a 100x2 cross-validation metric across different cancer types. 
The results showed that the optimal NAS model consistently outperformed all other models, including the previously optimal random forest model [Figure 1E].  

![**Comparison of methods for predicting the proteome from the transcriptome**
(A) CPTAC cancer datasets were downloaded from the web and processed to match samples across omic layers. 
(B) Four primary methods were evaluated for predicting the proteome from the transcriptome.
They are a dummy regressor to serve as a benchmark, a random forest regressor, a manually designed neural network, and an optimized neural network chosen via NAS. 
(C) The primary outline of the NAS search space used to identify the optimized neural network. 
(D) The model architecture of the optimized neural network. 
(E) A comparison between the four methods via 100x2 cross validation, indicating the optimized neural network outperforms all the others.](images/fig1_overview.svg){#fig:overview tag="1" width="100%"}


## References {.page_break_before}

<!-- Explicitly insert bibliography here -->
<div id="refs"></div>

