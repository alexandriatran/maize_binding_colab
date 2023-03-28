#### Monday, February 13, 2023
- Send DRS PDF to Amy/Alex.
- Get started in GitHub: https://github.com/skills/introduction-to-github. 
- Kinetics website: https://web.ics.purdue.edu/~drhodes/models/mo00004.htm
- Play around, install Visual Basic if not too much work.
- Pick platform for new version: Python (Flask) or R (Shiny)
- Talk about omics/binding tomorrow
- For Alex: get together some binding papers, show state of omics data collected.

#### Tuesday, February 14, 2023
- Thoughts about this grant: https://diversity.illinois.edu/diversity-campus-culture/broadening-inclusion-grant/
- My work: https://docs.google.com/presentation/d/19tSBHQIrvCNVIrB-7QDUQhLKc6n4Q8k7AfKo-z0d4NE/edit?usp=sharing
    - Regulatory gene binding papers:
        https://www.cell.com/cell/pdf/S0092-8674(21)00493-1.pdf
        https://epigenome.genetics.uga.edu/PlantEpigenome/index.html?data=zea_mays_v4&cat=Maize%20Epigenome&loc=1%3A16843778..17029986&tracks=genes%2Ctransposons%2Catac_leaf-1%2Cmethyl_leaf%2Cchip_leaf-h2az%2Cchip_leaf-h3k4me1%2Cchip_leaf-h3k4me3%2Cchip_leaf-h3k27me3%2Cchip_leaf-h3k36me3%2Cchip_leaf-h3k56ac%2Ca_leaf-atac-1%2Catac_leaf-2&highlight=
- Genome browser: https://software.broadinstitute.org/software/igv/
	https://www.nature.com/articles/s41467-020-18832-8.pdf
    - Learn about BED and BIGWIG file formats. See if you can write a script to get binding locations, check if they’re near genes, and output a table for each TF saying it binds near a gene or not. 
    - Other data of interest:
        - RNA-seq: https://docs.google.com/presentation/d/1TV1hf3VFUsH6L9mMFzx4k13rhapGZIIR8JlxOb-aoe4/edit?usp=sharing
        - An differential expression analysis of a nitrogen dataset I'm working on: https://docs.google.com/presentation/d/18wid79dh5V8k92BS9Po5sAvYNsdF4KCbJHlChxYp_aY/edit?usp=sharing
        - A network-based analysis in progress: https://docs.google.com/presentation/d/10iN6dgRo_G3xpv2D0K_-3HN0UAKkzYg-i79bzppNGRo/edit?usp=sharing
- Command line introduction: 
- Bash scripting intro: https://cs.lmu.edu/~ray/notes/bash/
You'll use bash whenever you log into a remote server like the Biocluster. 
The MacOS command line language is ZShell (aka zsh). They're pretty similar, so most bash scripts will work when run with zsh. This is important because some useful scripts written by others to help convert between file formats are bash scripts. 
- A lot of biological file formats can be parsed with packaged in R or Python, so you can also likely do file handling/conversion with some R package. 
- Todo for Mikhaiya: Play around with R. See where files in R are saved to on your system. Try to read in a BED file into an R dataframe using read.csv().
Or: consider doing all your code development on Google Colab. You can set up R using this tutorial: https://towardsdatascience.com/how-to-use-r-in-google-colab-b6e02d736497. It's like Google Docs but for Python/R notebooks and it can be run there too. You can also put your files on Google Drive and mount your Drive so you don't take up room on your laptop.
- Files to download:
* B73 v5 genome (FASTA) (on second thought you don't need this taking up space on your computer). This is the overall site for any B73 v5-related files you may want: https://download.maizegdb.org/Zm-B73-REFERENCE-NAM-5.0/
* Genome annotation (GFF3): Download "Zm-B73-REFERENCE-NAM-5.0_Zm00001eb.1.gff3.gz" from the above link. It is a compressed file, similar to ZIPs. This compression is a common one used by bash users called gzip. In the command line, you can uncompress it with the command "gunzip". Open the terminal and navigate to the same directory you've put the GFF3 file. Then just enter "gunzip m-B73-REFERENCE-NAM-5.0_Zm00001eb.1.gff3.gz" to uncompress it. You navigate through your file system using the command "cd" for change directory (aka folder). "cd .." will bring you back out of a directory you've entered. "cd directory_name" will move you into a directory. The "ls" command will list the files and folders in the directory you're in. I believe when you open your terminal you'll be in your home directory, "~". To navigate to Downloads, you run "cd Downloads". Not too sure about the MacOS file system.
- Todo for Mikhaiya: Look for a BED format file binding peak data to compare to annotated genes

#### Tuesday, February 21, 2023
- Talked about trouble with opening annotation file
- Alex suggested uploading it to Drive and using Colab to unzip it.
- Downlaoded rtracklayer package in R on Colab
- Mikhaiya will do do browseVignettes command when done downloading
https://bioconductor.org/packages/release/bioc/html/rtracklayer.html
#### Tuesday, February 28, 2023
- Variety show invite: cultural diversity, Apr 11, 5:30PM SDRP lobby.
- Ran into some issues opening BED files on Mac
- Problem of file permissions and likely has to do with .bed being an uncommon file extension. For the future, see about how to fix this.
- Uploading BED to Colab to view and read into R using rtracklayer
- Follow this guide to learn how to mount to your personal Google Drive and read files from it: https://towardsdatascience.com/access-google-drive-using-google-colab-running-an-r-kernel-3736db7835
- Debugging issue with non-interactive session: https://stackoverflow.com/questions/54595285/how-to-use-r-with-google-colaboratory
https://stackoverflow.com/questions/56679549/how-to-mount-google-drive-to-r-notebook-in-colab
- The basic tree of the Mac file system and how to traverse it from the terminal:
- Use this genome browser so that all of our genome locations correspond to the maize b73v5 assembly: https://jbrowse.maizegdb.org/
- To access transcription factor binding information, open the left tab "Epigenetics and DNA Binding". It is sorted by the uploader. Our interest is ChIP and DAP-seq. Download the BED or GFF file for the whole reference sequence.
- It seems it doesn't let you download when a file is too big, need to figure out.
#### Tuesday, March 7, 2023
- Meeting just Tuesday from now on, next week over Zoom
- Continue to download TF binding sites from jbrowse. Do not download histone ChIP-seqs (e.g. H3K27me3). 
- TODO: Mikhaiya email for bigger BED files, starting with John Portwood. 
john.portwood@ars.usda.gov 
- Alex hunt down someone at Maize Meeting
- Getting set up with BioPython
- Mikhaiya's collab link: https://colab.research.google.com/drive/14RgYijXGVbR4IARXJ3koEnNoqjEYqGdH
- Reading the Zm...gff file using a GFF parser compatible with BioPython: https://biopython.org/wiki/GFF_Parsing
- Python library for data/tables: Pandas https://pandas.pydata.org/docs/reference/api/pandas.read_csv.html code below. The top 4 lines of the GFF3 file are not part of the table and just give information about the gene annotation, so i skip them with the parameter "skiprows")
maize_gene_annotation_table = pandas.read_csv("Zm-B73-REFERENCE-NAM-5.0_Zm00001eb.1.gff3", sep="\t", skiprows=4)
- TODO: Mikhaiya set up Github with Colab. Clone the maize_binding_colab repo. 
#### Tuesday, March 21, 2023
- Installed PyBedGraph, uploaded necessary chromosome sizes file
- TODO: Mikhaiya try reading a bedGraph fil with this package: https://pypi.org/project/pyBedGraph/
- Notes on grad school:
* Doing a research thesis heavily recommended for bioinformatics/bio. It demonstrates independence and many jobs will ask why if you don't do it.
* Many places will require 3 letters of recommendation. UIUC explicitly said they prefered research supervisors. If you want our lab to write a letter, let's start thinking about it now so we can have some good things to say.
* I applied fall of 2019 and got into UCSD and UIUC, rejected from UWashington, Cold Spring Harbor, and later Duke. We can talk odds/good schools for your objectives.
* Graduate fellowship resources (Alex has bank of personal and research statements available): https://www.nsfgrfp.org/

#### Tuesday, March 28, 2023
- Got response from John Portwood and Ethy about TF data for MaizeGDB, pointed to Grassius for data.
- Grassius lacks comprehensive binding data and is not up to date with many ChIP-seq experiments
- Useful template for goal table can be found at Grassius Downloads page in file Grassius_RegNet: https://grassius.org/download.php?download_file=Grassis_RegNet.xls
- Mikhaiya will consider writing own algorithm for binding site location annotation or if Alex will provide basic pseudocode.
- Learn the basics of logic flow in Python from this page: https://www.openbookproject.net/books/bpp4awd/ch04.html
