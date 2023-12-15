# Project Context
This repository is the final product for the course PRA3006 at the Maastricht Science Programme. The objective of this project is to find potential drug targets for Duchenne Muscular Distrophy. A list of disregulated genes compared to control was given. The goal of the project was to use the CHEMBL webservice to identify potential drugs based on targets related to the given genes. 

# Description
The first step was to find the CHEMBLID for these genes. Three were found:  CHEMBL5742, CHEMBL1841, and CHEMBL2093862. Then, a SPARQL query was developed that retrieves additional information about the genes of interest using the CHEMBL RDF, eventually retrieving information about small molecules that target said genes. In addition, the bioactivity that is used to measure this is retrieved. There are several bioactivities given, but the query filters for IC50 for significance. IC50 measures the necessary concentration of a drug for it to have a desired effect. Therefore, low IC50 values are indicative of potency. For this reason, the query filters the result in ascending order. 
The results are the top 10 molecules targetting the proteins of the genes of interest based on lowest IC50.

These results are displayed in a bubble graph representation using the D3 library. Each bubble corresponds to a small molecule that targets a gene of interest. The size of the bubble corresponds to its IC50 value. 

# Potential Improvements
Unfortunately, most bubbles do not contain a relevant name, but only their CHEMBL IDs. While they should correspond to their names in CHEMBL, it is possible that some are not registered on CHEMBL. Two drugs of interest have registered names: DASATINIB and PONATINIB. 

The size of the bubbles is inversely proportional to their relevance. 

# Instructions
To open the visualization, it is necessary to download the file "DMD final project-final.html". By opening the given file, the visualization should open as a website in your default web browser.
