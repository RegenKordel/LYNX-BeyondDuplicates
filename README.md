# Lynx
This repository contains the data, experiments, and analysis for the submission ``Beyond Duplicates: Towards a Better Understanding and Prediction of Link Types in Issue Tracking Systems''.
There are five subfolders;
- data
- data_preprocessing
- RQ1_link_analysis
- RQ2_link_gt_metrics
- RQ3_link_detection

## data

Contains the data we used for our analysis and machine learning models.
These were extracted with the needed properties from this [MongoDB dump](https://www.dropbox.com/sh/ma1hgeafg34chb2/AAD05Vc9H_shEbkFJ47jjv4Na)

## data_preprocessing

Contains the jupyter notebooks to preprocess the data, this includes a the text cleaning for the ``title`` and ``description`` field and the cleaning of the link data from private issues and links which contain a private issue as well as ambiguous data, such as multiple different link types between two issues.

## RQ1_link_analysis

Contains the jupyter notebooks for Tables 1, 2, and 3 (AnalysisOfLinktypes.ipynb) and for Firgues 1 and 2 (AnalysisOfLinkCategories.ipynb) and the corresponding analysis. 
 The .pdfs in the main repository
 - BeyondDuplicates - Projects, the links to the JIRA ITS of each project and the crawled JSON fields
 - BeyondDuplicates - Usage, an overview of which ITS use which link types prior to cleaning
 - BeyondDuplicates - OverviewLinkTypes, an overview of the unique link types with explanations
 - BeyondDuplicates - Categorization, the categorization with examples and semantics from each of the ITS as well as the frequencies
 
## RQ2_gt_metrics

Contains the jupyter notebooks for Tables 4 and 5 (LinkCategoryMetrics.ipynb) and the corresponding analysis.

## RQ3_link_detection

Contains the single-channel and dual-channel models (SingleChannel.ipynb, DualChannelOriginal.ipynb) used in this submission, as well as our results and their analysis (Results_SCCNN.ipynb and Results_DCCNN.ipynb).
