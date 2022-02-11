# Traject3d

Directories:
\begin{itemize}
\item CellProfiler: contains a zip file comprised of two CellProfiler pipelines (one per experimental replicate of the test dataset) for segmenting images, tracking objects between frames, and generating measurements of size, shape, and movement. The rules for user-defined state classifications (Round, Spread, Spindle) are also provided as a text file, which may be loaded into the FilterObjects modules of the pipelines. This directory also contains a PDF file showing the settings used to analyse the sample datasets.

\item KNIME: contains KNIME pipeline and associated user manual for software setup and running instructions and tips. Expected installation and set-up time for all dependencies is approximately 2 hours.  The KNIME pipeline was tested on a machine running Windows 10, with 64GB RAM and an Intel Core i7-7740X CPU @ 4.30GHz processor. Expected runtime of the sample data on a machine with similar CPU specifications is approximately 4 hours for all components of the pipeline. Most users will typically only run either the user-defined or data-driven sections, not both.

\item SampleData: contains expected output, and information on the settings used to generate it. Sample data can be accessed at: https://www.dropbox.com/sh/igfpnt174l14ftc/AADq5B6RapGfJ16VOjTawUq9a?dl=0

\end{itemize}