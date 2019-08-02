# Snomed2Vec : 

This repository provides a reference implementation of Snomed2Vec as described in the paper:

Snomed2Vec :Poincare and Random Walk Embeddings of a clinical knowledge base for healthcare analytics.

**Download Snomed2Vec Embeddings**

The medical concept embeddings for Snomed graph as described in paper can be found here:
https://drive.google.com/drive/folders/1zre60Kd0nmQubgQO4iaf0TtWpVLaEKZO


**Citing**

If you found the work useful, please consider citing the following paper:

 
@inproceedings{Snomed2Vec-DSHealth2019,

author = {K Agarwal, T Eftimov, R Addanki, S Choudhury, S Tamang, R Rallo},

title = {Snomed2Vec :Poincare and Random Walk Embeddings of a clinical knowledge base for healthcare analytics},

booktitle = {KDD Workshop on Applied Data Science for Healthcare: Bridging the Gap between Data and Knowledge},

year = {2019}

}

**Generating SNOMED-X graph**
	
To provide SNOMED-X version for learning the embeddings we should use the tables: MRSTY.RRF, MRCONSO.RRF, and MRREL.RRF, which are available under the UMLS license and can be download from https://www.nlm.nih.gov/research/umls/.
Additionally the UMLS semantic group file should be used, which is available at https://metamap.nlm.nih.gov/SemanticTypesAndGroups.shtml


	1	Use the script src/concept_similiarity/prunningSNOMEDCT.R to create the SNOMED-X graph
	2	Follow the steps available in the script to generate the SNOMED-X graph
	3	Input data are:  MRSTY.RRF, MRCONSO.RRF, and MRREL.RRF and the UMLS semantic group file
	4	Output data: SNOMED-X graph (relations between concepts)


**Concept similarity**
	
To calculate the concept similarity  between pairs of concepts using their embeddings, we generated five benchmark files available in src/concept_similiarity/Benchmark_files.
To calculate the statistical power for each benchmark data set and each embedding method:

	1	Use  the script src/concept_similarity/Benchmkarking_script.R
	2	Follow the steps documented in the script
	3	Input data are:  benchmark data set
	4	Output data: statistical power for every embedding method
