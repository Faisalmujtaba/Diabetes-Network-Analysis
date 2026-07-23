Project Overview
This project applies Social Network Analysis (SNA) techniques to healthcare data by constructing a disease co-occurrence network from diabetic patient records. ICD-9 diagnosis codes are grouped into disease categories, allowing diseases to be represented as nodes and their co-occurrences as weighted edges.
The resulting network is analyzed using graph analytics, centrality measures, shortest path analysis, and community detection to identify important disease relationships and influential disease categories.

Objectives
Build a disease co-occurrence network from patient diagnosis records. 
Map ICD-9 diagnosis codes into broader disease categories. 
Identify frequently co-occurring diseases. 
Detect disease communities. 
Compute multiple network centrality measures. 
Identify hub and bridge diseases. 
Export the network for Gephi visualization. 
Generate graph statistics and logs. 

Dataset
Dataset: Diabetic Patient Records (diabetic_data.csv)
The dataset contains:
Patient ID 
Primary diagnosis (diag_1) 
Secondary diagnosis (diag_2) 
Tertiary diagnosis (diag_3) 
ICD-9 diagnosis codes are mapped into disease categories such as:
Diabetes 
Circulatory 
Respiratory 
Digestive 
Musculoskeletal 
Endocrine 
Skin 
Injury 
Mental Disorders 
Genitourinary 
Neoplasms 
Other 

Features
ICD-9 diagnosis mapping 
Disease categorization 
Disease co-occurrence extraction 
Weighted graph construction 
Disease network visualization 
Community detection using Louvain algorithm 
Degree Centrality 
Betweenness Centrality 
Closeness Centrality 
Eigenvector Centrality 
PageRank 
Hub disease detection 
Bridge disease identification 
Disease influence analysis 
Shortest path analysis 
Graph statistics generation 
GraphML and GEXF export 
Gephi compatibility 

Methodology
1. Data Preprocessing
Load diabetic patient dataset 
Remove missing diagnosis values 
Convert ICD-9 codes into disease categories 
Group diagnoses by patient 

2. Disease Co-occurrence Extraction
For each patient:
Collect all diagnosed disease categories 
Remove duplicate diseases 
Generate every unique disease pair 
Count co-occurrences across patients 
Remove infrequent disease pairs using a minimum threshold 

3. Network Construction
Each disease category becomes:
Node: Disease category 
Edge: Co-occurrence between diseases 
Weight: Number of patients sharing both diseases

Graph Analysis
The project evaluates the disease network using several graph analytics techniques.

Degree Centrality
Measures how many direct disease connections each disease has.
Application:
Identify highly connected (hub) diseases. 

Betweenness Centrality
Measures how frequently a disease lies on the shortest paths between other diseases.
Application:
Identify bridge diseases linking different disease communities. 

Closeness Centrality
Measures how close a disease is to all other diseases in the network.
Application:
Detect diseases capable of rapidly influencing the network. 

Eigenvector Centrality
Measures the importance of diseases based on their connections to other influential diseases.
Application:
Identify globally influential disease categories. 

PageRank
Ranks diseases according to their importance within the network.
Application:
Measure overall disease influence. 

Community Detection
The project uses the Louvain Community Detection Algorithm to identify clusters of highly interconnected diseases.
Community visualization includes:
Community coloring 
Node scaling based on centrality 
Individual community plots 

Shortest Path Analysis
The shortest path between two disease categories is computed and visualized to illustrate indirect disease relationships.
Example:
Diabetes
     │
Circulatory

Network Outputs
The project generates:
Disease co-occurrence edge list 
Disease network graph 
Community visualizations 
Centrality rankings 
Shortest path visualization 
Graph statistics log 
GraphML file 
GEXF file (Gephi compatible) 

Technologies Used
Python 
Pandas 
NumPy 
NetworkX 
Matplotlib 
Python-Louvain 
itertools 
collections 
Logging 
Gephi 

Evaluation Metrics
The network is analyzed using:
Number of Nodes 
Number of Edges 
Degree Distribution 
Graph Density 
Connected Components 
Average Degree 
Average Clustering Coefficient 
Diameter 
Average Shortest Path Length 
Community Count 

Applications
This project can be applied to:
Healthcare analytics 
Disease surveillance 
Clinical decision support 
Comorbidity analysis 
Public health research 
Medical network analysis 
Epidemiology 
Hospital management 
Disease progression studies 


Required Libraries
pip install pandas
pip install numpy
pip install matplotlib
pip install networkx
pip install python-louvain


Future Improvement
Apply Graph Neural Networks (GNNs) 
Add temporal disease progression analysis 
Integrate patient demographic information 
Predict future disease associations using link prediction 
Build an interactive dashboard with Streamlit 
Analyze larger healthcare datasets 
Develop disease recommendation systems 

Learning Outcomes
This project demonstrates expertise in:
Social Network Analysis (SNA) 
Graph Theory 
Healthcare Analytics 
Network Science 
Disease Network Modeling 
Community Detection 
Centrality Analysis 
Medical Data Analysis 
Python Data Science 
Gephi Visualization 
