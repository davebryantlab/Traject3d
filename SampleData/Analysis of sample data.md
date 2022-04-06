Sample data (ExampleshRNA_live cysts.zip) and expected output (ExpectedOutput.zip) can be obtained from the following URL: https://www.dropbox.com/sh/igfpnt174l14ftc/AADq5B6RapGfJ16VOjTawUq9a?dl=0


After KNIME (with R and Python integrations) set-up, open the provided pipeline (Traject3D_v1.knwf) in KNIME. Uncompress ExampleshRNA_live cysts.zip and load the resulting "ExampleshRNA_live cysts" directory into the first node/component of the pipeline. This is a dummy dataset containing a scrambled shRNA control sample ("Scramble"), and two shRNAs ("shRNA_1", "shRNA_2"). Two experimental replicates were performed, each with four wells per condition, which were imaged hourly for 2 days (48hrs). The images were segmented, and acini tracked using CellProfiler. A user-defined shape classification ("Round", "Spindle", "Spread") was also applied. We provide the output from this CellProfiler analysis.

Due to the variability in tSNE and PhenoGraph analyses, even when using the same parameter values the output will not be exactly identical, but it should be similar.

Settings used to generate expected output: 
		- In "Select Samples and Frames to Include" (Data pre-processing section) component, "filter by timepoints" was set to "no" in order to include all timepoints in the subsequent analysis.
		- In all components where time chunking is applied ("Calculate TimeChunks", "Trajectory Timechunk Plots (Frequency Motifs and Transitions)"), we used a time chunk of 6hrs.
	User-defined classification:
		- For identification of user-defined classification trajectories, PhenoGraph k-nearest neighbours = 50.
	Data-driven classification:	
		- For data-driven state identification, data was subsampled to 20,000 points using GeoSketch. PhenoGraph k-nearest neighbours = 40.
		- For data-driven trajectory identification, PhenoGraph k-nearest neighbours was = 40. 
		- Data was subsampled to 20,000 points using GeoSketch prior to tSNE. tSNE was then performed with PCA initiation, iterations = 5000, theta = 0.25, perplexity = 50.