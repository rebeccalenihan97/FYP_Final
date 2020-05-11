The Flavour of Disorder: Predicting Intrinsically Disordered Regions in Proteins by Deep Learning

-   Rebecca Lenihan
-   Supervisor: Dr. Gianluca Pollastri

Prerequisites
--------------------------------

The runnable scripts for this project were written in Python 3 using
Jupyter Notebooks, therefore to run programs the following points need
to be in place:

-   Access to Jupyter Notebooks: Download
    [Anaconda](https://www.anaconda.com)
-   Jupyter Notebooks launched directly through Anaconda application
-   Please download the Original dataset from
    [MobiDB](https://mobidb.bio.unipd.it/dataset), titled "Indirect
    disorder (PDB)". **Please see Note**
-   Please ensure that all datasets are located in the same directory as
    the notebooks

Note
==============

-   Some of the datasets were too large to upload to GitHub, namely the
    "dataset.csv" file and the original dataset
    "derived\_disorder.mjson" are not uploaded.

The following steps should be followed to acquire the datasets in order
to run the relevant notebooks.

-   1: Go to [MobiDB](https://mobidb.bio.unipd.it/dataset) and download
    the dataset "Indirect disorder (PDB)". A .gz file will download.
-   2: Unzip the file and ensure the file is named:
    "derived\_disorder.mjson"
-   3: Move the file to the same directory as the downloaded notebooks,
    in particular the "initialAnalysis.ipynb" notebook.
-   4: Compile the "initialAnalysis.ipynb" notebook, and as a result,
    the "dataset.csv" dataset will be created in the same directory.

Files Included
----------------------------------

-   The models used in this project (i.e. the Feed-Forward Neural
    Network and the Bi-Directional Recurrent Neural Network) were
    provided by Dr. Pollastri, and therefore not included in this
    repository.
-   Included are the notebooks created to complete the associated tasks
    of the project (namely, parsing and processing the data)
-   Included are also the log files, experiments, resulting files, and
    other files created upon the use of the models for which analysis
    was conducted on.
-   Also included are a number of datasets which were used throughout
    the project and will be explained in further detail below

Datasets
----------------------

-   **derived\_disorder.mjson**: Original dataset from
    [MobiDB](https://mobidb.bio.unipd.it/dataset), titled "Indirect
    disorder (PDB)"
-   **dataset.csv**: Resulting dataset from initial analysis and
    pre-processing of MobiDB dataset
-   **Alignmentfiles.csv**: Dataset containing the aligned sequences for
    proteins
-   **finalReducedDataset.csv**: Redundancy reduced dataset
-   **nnPrepFirstData.csv**: Initial dataset used to train models using
    one-hot encoding

    > -   /Evaluation/Non-Alignment Datasets
    >     -   **test.dataset**: test set in required format for input of
    >         NN (non-aligned sequences)
    >     -   **train.dataset**: train set in required format for input
    >         of NN (non-aligned sequences)
    > -   /Evaluation/Alignment Datasets
    >     -   **test.dataset**: test set in required format for input of
    >         NN (aligned sequences)
    >     -   **train.dataset**: train set in required format for input
    >         of NN (aligned sequences)

-   **result.fasta**: Dataset to be redundancy reduced in FASTA format
-   **result.txt**: Textfile version of result.fasta file

Notebooks
------------------------

*Note: **FYP\_FinalCode\_BeforeRR** and **InputFilesforNN** contain the
formatted information and code established in the other notebooks.
Initially, tasks were performed separately, before I combined them into
these two notebooks to reduce complexity and increase ease of
understanding for reviewer.*

#### Final Notebooks:  

-   **initialAnalysis.ipynb**: This notebook contains the initial
    analysis and pre-processing of the dataset. Namely adding more
    information to the dataset, removing redundant information
    (non-referenced amino acids), updating indexes, etc.

-   **InputFilesforNN.ipynb**: This notebook contains the code used to
    format the dataset in order to use as input for the Neural Networks.
    Namely, the data is formatted in a specific format as outlined in
    Report, this process is intially completed for the proteins using
    one-hot encoding representation of the amino acids, followed by the
    process being repeated using aligned sequences.

#### Previous Notebooks: 

-   **FormattingInputforNN\_initial.ipynb**: This notebook contains the
    initial code used to format the input files for the Neural Networks
    without the use of aligned sequences. This approach was adopted into
    the **InputFilesforNN.ipynb** notebook to apply to data once
    evolutionary information was included

-   **Index\_Fixing.ipynb**: This notebook contains the initial code
    used to establish what proportion of the sequences were not being
    referenced, the removal of those amino acids and the updating of
    their corresponding indexes to mirror the changes being made in the
    sequences.

Other Folders 
--------------------------------

-   **FYP Experiments**: Contains the log files which resulted from
    running experiments using the Neural Networks. Each file shows a
    different experiment (i.e.) Different parameters were used. Each
    file contains the parameters used, and shows the error rates
    returned as the model trains. There is a range of experiments for
    both FFNN and BRNN models.
-   **Evaluation**: Contains multiple folders used to evaluate the
    performance of the models

    > -   **Non-Alignment Datasets**: Contains the test and train
    >     dataset used for the models with non-aligned ptrotein
    >     sequences
    > -   **Alignment Datasets**: Contains the test and train dataset
    >     used for the models with aligned protein sequences
    > -   **Evaluation Excel Files**: Contains a range of excel files
    >     used to evaluate the models
    >
    >     > -   **ComparingAlignmentvsNoAlignment.xlsx**: Contains the
    >     >     resulting prediction values of the models, contains the
    >     >     calculation of the metrics used to evaluate the model
    >     >     (outlined in report), contains graphs used to evaluate
    >     >     models, etc...
    >     > -   **More\_Eval\_Graphs.xlsx**: Contains further analysis
    >     >     of the models, results of best experiments displayed in
    >     >     tables, Comparison between my results and previous
    >     >     prediction methods, explanation of parameters, etc.
    >
    > -   **Alignment Models**: Consists of the models which are
    >     returned as the Neural Network trains. These models are used
    >     in order to make predictions. Files in folder correspond to
    >     models returned from best experiments when using aligned
    >     sequences
    > -   **Non-Alignment Models**: Consists of the models which are
    >     returned as the Neural Network Trains. These models are used
    >     in order to make predictions. Files in folder correspond to
    >     models returned from best experiments without using aligned
    >     sequences
    > -   **Evaluation Graphs**: Consists of the graphs created while
    >     evaluation the performance of the models, and the tables
    >     created
    > -   **Appendix Tables**: Consists of the tables explaining the
    >     parameters used in best performing experiments

-   **AlignmentFile.txt**: Contains the protein ID, the sequence length
    and the corresponding aligned sequence


     
