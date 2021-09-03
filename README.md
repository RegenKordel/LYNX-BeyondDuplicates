# Lynx - Beyond Duplicates
This repository contains the data, experiments, and analysis for the submission ``Beyond Duplicates: Towards a Better Understanding and Prediction of Link Types in Issue Tracking Systems''.
There are five subfolders;
- data
- data_preprocessing
- RQ1_link_analysis
- RQ2_link_gt_metrics
- RQ3_link_detection

## Structure of the Repository

### data
Contains the data we used for our analysis and machine learning models.
These were extracted with the needed properties from this [MongoDB dump](https://www.dropbox.com/sh/ma1hgeafg34chb2/AAD05Vc9H_shEbkFJ47jjv4Na)

### data_preprocessing
Contains the jupyter notebooks to preprocess the data, this includes a the text cleaning for the ``title`` and ``description`` field and the cleaning of the link data from private issues and links which contain a private issue as well as ambiguous data, such as multiple different link types between two issues.

### RQ1_link_analysis
Contains the jupyter notebooks for Tables 1, 2, and 3 (AnalysisOfLinktypes.ipynb) and for Firgues 1 and 2 (AnalysisOfLinkCategories.ipynb) and the corresponding analysis. 

- [BeyondDuplicates - Categorization.pdf](https://github.com/RegenKordel/LYNX-BeyondDuplicates/files/7105539/BeyondDuplicates.-.Categorization.pdf) The links to the JIRA ITS of each project and the crawled JSON fields.
- [BeyondDuplicates - OverviewLinkTypes.pdf](https://github.com/RegenKordel/LYNX-BeyondDuplicates/files/7105540/BeyondDuplicates.-.OverviewLinkTypes.pdf) An overview of which ITS use which link types prior to cleaning.
- [BeyondDuplicates - Projects.pdf](https://github.com/RegenKordel/LYNX-BeyondDuplicates/files/7105541/BeyondDuplicates.-.Projects.pdf) An overview of the unique link types with explanations.
- [BeyondDuplicates - Usage.pdf](https://github.com/RegenKordel/LYNX-BeyondDuplicates/files/7105542/BeyondDuplicates.-.Usage.pdf) Categorization with examples and semantics from each of the ITS as well as the frequencies
 
### RQ2_gt_metrics
Contains the jupyter notebooks for Tables 4 and 5 (LinkCategoryMetrics.ipynb) and the corresponding analysis.

### RQ3_link_detection
Contains the single-channel and dual-channel models (SingleChannel.ipynb, DualChannelOriginal.ipynb) used in this submission, as well as our results and their analysis (Results_SCCNN.ipynb and Results_DCCNN.ipynb).

# Python Packages
Python Version: Python 3.8.10

- gensim                   4.0.1                      
- Keras                    2.4.3              
- keras-nightly            2.5.0.dev2021032900
- Keras-Preprocessing      1.1.2                     
- matplotlib               3.4.2                        
- networkx                 2.6.2              
- nltk                     3.6.2              
- numpy                    1.19.5                      
- pandas                   1.2.4                         
- pymongo                  3.11.4                   
- regex                    2021.4.4                
- scikit-learn             0.24.2             
- scipy                    1.6.3              
- seaborn                  0.11.1                       
- sklearn                  0.0                      
- spacy                    3.0.6              
- spacy-legacy             3.0.5                   
- stanza                   1.2                
- tensorboard              2.5.0              
- tensorboard-data-server  0.6.1              
- tensorboard-plugin-wit   1.8.0              
- tensorflow               2.5.0              
- tensorflow-addons        0.13.0             
- tqdm                     4.60.0             

# Steps for Replication
1. Download the extraced data from the dropboxlink provided and unzip it in the data folder.
- Optional: Rerun "Link_Preprocessing.ipynb" to get the clean_link csv files
2. Install the python packages on your machine or in a virtual environments
3. Run Jupyter Notebook, a gpu is recommended if you want to rerun the notebooks from RQ3 for larger projects
4. Run the notebooks for RQ1, RQ2, or RQ3, they are independent from each other. RQ3 needs to run the SingleChannel.ipynb or DualChannelOriginal.ipynb before running the respective analysis
