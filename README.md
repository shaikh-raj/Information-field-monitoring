# Information-field-monitoring
## Parsing news from russian mass media and it content analysis

<b>TARGET STAGE 1</b> - build a system of multiclass classification of news reflecting the dynamics of changes in the information field in Russia

![PIPELINE_1](REP_base_pipeline_news.png)

To achieve the goal of the project it is necessary:
- create a module for parsing news feeds of the most popular news agencies in the country;
- develop and deploy a database for storing news texts;
- mark the test data set as many data classes, such as negative or positive news, type of news, news topic, etc.;
- configure a neural network with the pre-trained linguistic module BERT;
- train the neural network on a test data set;
- test the effectiveness of the neural network on new unlabeled data;
- design the information panel Power BI to visualize the result of the classifier;
- upload data to the report and deploy it on the local server / in the cloud

The repository contains the following blocks of program code:
- tass_parser.py - module for parsing the news feed of the TASS news agency;
- ria_parser.py - module for parsing the news feed of the RIA news agency;
- interfax_parser.py - module for parsing the news feed of the INTERFAX news agency;
- SCHEMA - structure and configuration of a relational database for storing project data;
- app_parser.py - application for parsing all the required news and saving them in the local project database (see SCHEMA);
- train.csv - labled data set for neural network training;
- NN.py - neural network;
- dashboard.pbix - visualized of the result of the NN classifier

<b>TARGET STAGE 2</b> - creation of an analytical platform that meets the needs of various businesses in the analysis of their information field

![PIPELINE_2](REP_commercial_pipeline.png)
