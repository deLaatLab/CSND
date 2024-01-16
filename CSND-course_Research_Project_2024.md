**Research Project:**

**Uncovering functional consequences of a risk variant**


Notes:

- Store your answers in a PowerPoint (i.e., \*.pptx) presentation. 
- In case a coordinate is requested, an approximate is sufficient (+/- 1kb). There is no need to provide these coordinates at a base pair resolution.
- In case a screenshot (i.e., “print screen”) is requested, simply paste the picture into a slide within the .pptx file. 
- In case you are asked to take a screenshot of a webpage, but the web page is larger than a single page, you can take the screenshot of the most relevant part of the page. There is no need to take a screenshot for each page.
- The title of each slide should specify which question (**Q1**, **Q2** etc.) is being answered.
- Make sure to save the final .pptx file under your full name and follow this pattern: John\_Green.pptx
- An internet search can be used to find an answer to a given question. Meanwhile, we highly recommend you think about the question and try to produce an answer first. Then, if preferred, you can use your internet queries to confirm the correctness of your answer. This approach helps you learn much better and the answer will stay in your mind much longer.
- Be sure to keep using the GRCh37/hg19 assembly (or version) of the reference genome across this assignment. Otherwise, you may not find the element that you are interested in.

**Aim**: Aim of this project is to experimentally validate functional relevance of a risk variant (rs7258891) and identify the affected gene. Once that is done, we will design a CRIPSR-Cas9 guide-RNA to be used for genome editing and delete the affected regulatory element. Finally, we will design primers to be used for cDNA qPCR experiments with the aim of checking whether this modification would be causing any of the candidate target genes to be up or downregulated in the K562 cell line. 

**--------------------------------**

**Background**: <a name="_int_ejaoichm"></a>Let’s assume that a variant called “rs7258891” is identified in a <a name="_int_kscxcnfw"></a>GWAS study to be related to a blood disease (for example leukemia). 

**Q1.** What is the definition and aim of GWAS? How are such studies performed? Explain the intuition behind the GWAS approach in a few (8-10) sentences.

**Q2.** What is the chromosomal coordinate of rs7258891 in the human genome? Which genes are surrounding this variant?

Hints:

- You can use the [UCSC Genome Browser](http://genome-euro.ucsc.edu/) for this question.
- Once opened, on the top left of the screen, hover over “Genomes” and click on “Human GRCh37/hg19”. 
- Wait for the page to load completely.
- Now you are working with hg19 version of the human reference genome.
- It is advisable to clear your environment on the website and <a name="_int_sithg31q"></a>start from scratch. To do this, search for “hide all” text on the page. This will point you to a “hide all” button. Click on this button to clear your environment.
- We would like to add a “gene track” so that we can see genes and their genomic locations on the browser. To this end, search for “UCSC Genes” text on the web page. Once found, you will see a drop-down list underneath. Click on it and choose “full<a name="_int_btjs6hat"></a>”. Then, on the right side of the page click on “refresh” button (there could be multiple “refresh” buttons, all would do the same). Once refreshed, you can see several genes on the newly loaded track above.
- Next, we would like to find our variant of interest. On the top center of the page, there is a search box which says: “gene, chromosome range, …<a name="_int_bkgj4sij"></a>”. There, you can search for the variant of interest, which is: rs7258891.
- On the right side of the opened page, you will see many links pointing to the same variant (across different databases) or similar variant across <a name="_int_eqrriz1a"></a>different species.
- Besides each link, you can also see the corresponding coordinate of that variant.
- We will work with the variant shown below “Common (1000 Genomes Phase 3 MAF >= 1%) Short Genetic Variants from dbSNP Release 153” category. 
- Note its chromosomal coordinate in your “answer” slides and click on the corresponding link.
- Once the genome browser loads again, you will see a tiny (colored) vertical line that indicates the location of our variant.
- On the top of the page, you can see several “Zoom in” and “Zoom out” buttons. <a name="_int_fgyrypzg"></a>Most likely, you are very much zoomed in. Adjust the zoom (by zooming out) to see multiple genes surrounding our variant.
- Take a screenshot such that the surrounding (4 to 8) genes and the variant of interest are seen on the screenshot.
- To reduce the clutter in the web page, you can hide the “variant track<a name="_int_6lwnw5ed"></a>”. To do this, find the gray vertical bar on the left side of the track, right click on it, and choose “hide track set<a name="_int_da0umvpn"></a>”.
- Note that the highlighted vertical bar is still present. This helps to know where the variant is located.

\--------------------------------

As seen in **Q2**, the variant of interest (i.e., rs7258891) localizes to a non-coding part of the genome. As no gene is directly hit with this variant, the functional impact of this variant is therefore not immediately clear to us. We hypothesize that this region may harbor an enhancer that influences the expression of its surrounding genes. 

**Q3.** Which histone modification is classically indicative for active enhancers? 


Hints:

- For this question, we are interested in acetylation modifications only. 
- Note that the latest research added further histone modifications that could be indicative of active enhancers. If you prefer, you can mention other modifications as well.

**Q4.** Does rs7258891 localize inside an active enhancer in K562 cell line?

Hints:

- You can load the relevant ChIP-seq track into UCSC genome browser and look at the coverage of this mark to answer this question. 
- You can use “Track search” button on the UCSC Genome Browser for this.
- Once you click on the “Track search” button, a new page will load. There, you will see a search box. Use “K562 <name of histone modification>” to find relevant ChIP-Seq tracks. Be sure to replace “<name of histone modification>” with the histone mark of interest (see **Q3**).
- Choose the track that is described as: “K562 Cells from ENCODE”. Search for this term on the webpage to easily find the track.
- Put the check mark beside this track. Make sure no other tracks are checked.
- Set “Visibility” to “full” and click on “View in Browser” or “Return to Browser” whichever is available.
- Note that histone modifications are often assessed from a general point of view. In other words, look at the overall coverage, not individual or small peaks. Number of peaks is not relevant in this question.
- Adjust the zoom of the browser to easily see the variant as well as the histone mark coverage related to the variant.
- Take a screenshot to show the variant’s chromosomal position and the active enhancer. 

\----------------------------------

**(Background information) Linkage disequilibrium (LD)** 

Variants in the genome do not appear (or occur) independently. For example, once a variant is observed in a sample, we can already tell if another adjacent (for example within 1-5 kb) variant is present in that sample too. This is because within a certain population (say Europeans), genomic variations tend to be inherited together as a block of variants, or in other words they are within “Linkage disequilibrium” (LD) of each other. A collection of these related variants (or chromosomal blocks of the genome) that are inherited together is called a haplotype (also known as LD-block). This knowledge is especially useful in genomic research to reduce cost or gain further insights from incomplete data. For example, we do not need to sequence every base of a genome to identify all occurred variants. Even if we sequence some of these variants (which reduces cost of sequencing), we can make the full overview of occurred variants as long as we know which genomic blocks are likely to be inherited together. These LD-blocks are often <a name="_int_o4swcujv"></a>very similar in samples that originate from the same geographical location (e.g., Europe). So, knowing the population origin of a sample, we only need to sequence part of their genome to infer the full set of their occurred variants.

LD-blocks have additional applications in genomic research. We show one of these applications in the current assignment. In our case, even if no gene or regulatory element is hit by our variant (i.e., rs7258891), other variants within its LD-block can hit genomic elements nearby and therefore have a functional impact. Consequently, it is important to know the LD-block of our variant.


**Q5.** Knowing about Linkage disequilibrium and the relationship between variants in a certain population, how can we reduce the sequencing cost in a “GWAS” study? 

Hints:

- To answer this, you can investigate how GWAS is done and what exactly is being sequenced in a typical GWAS sequencing experiment. You can see the above **Background information** for more details.

**Q6.** Mention the coordinate of the LD block that encloses our variant. Note that the exact coordinates are not intended here. An estimated (+/- 1kb) is sufficient.

Hints:

- You can use ENSEMBL to identify the corresponding LD-block for this variant:
  - Go to <https://grch37.ensembl.org/Homo_sapiens/Info/Index>
  - Search for the variant’s name: rs7258891
  - It might take 10-30 seconds before the page loads. Be patient 😉
  - Once the page is loaded, select “Linkage disequilibrium” on the left menu.
  - On the bottom of the page, you see a list of populations that can be used to define the LD-blocks. In this assignment, we are interested in the European population: “1000GENOMES:phase\_3:CEU”. Select the corresponding “View table” link for this population. This link is located on the far right of the row (i.e., last column).
  - In the opened page, you can see the LD-block coordinates on the top. The coordinates of the LD-block interval are mentioned after “Pairwise D' values for” text.
  - In this page, note the LD-block coordinate in your answer slide, or take a screenshot of the web page.
  - (Just for your information) Each table provides an overview of variants within an LD-block. Each number within the table is related to a pair of variants. This number indicates how likely it is to see one of the variants when the other variant is already observed in a given dataset. If you are interested, you can use Google to find and read more about LD-blocks and how they are identified and used in a wide variety of genomics or bioinformatics applications.

**Q7.** Identify the coordinates of the affected enhancer(s). Simply take a screenshot of the ChIP-seq track and annotate the regions that you think are related to the enhancer (for example using multiple hollow “rectangle” shape in the PowerPoint).

Hints:

- You can try to load the relevant ENCODE ChIP-Seq in the UCSC genome browser (as you did before in **Q4**)
- Use the relevant LD-block coordinate (found in **Q6**) to find the neighbor enhancers in the same LD-block.
- Take a screenshot of the ChIP-seq track and annotate the regions that you think are related to the enhancer(s). 
- To annotate, you can use a “rectangle” shape from PowerPoint and set the “Shape Fill” color as” No Fill<a name="_int_0uawhdgg"></a>”. 
- Here, each cluster of coverage would be an enhancer. 
- Note that it is fine if you combine multiple enhancers and consider them as one. The exact number of identified enhancers is not the point here.

\-----------------------------------

Now we know which enhancers are most likely affected by this variant. The next step is to determine the most likely affected genes. For this, we want to understand which genes co-localize with the affected enhancers within the 3D space of the nucleus. In other words, they are residing in a particular Topologically Associating Domain (TAD). (Optional) You can Google this term to learn more about it.

**Q8.** What are the chromosomal coordinates of the affected TAD(s)? 

Hints:

- Go back to UCSC genome browser. 
- Make sure you are using hg19 as the reference genome.
- Use “track search” button and search for: “K562 Hi-C”
- Check the box beside “K562 Hi-C”, make sure the “Visibility” is set to “full”
- Click on “View in Browser” or “Return to Browser” whichever is available.
- Make sure you are limiting the UCSC genome browser to coordinates of the LD-block (you got this coordinate in **Q6**) only.
- In the “zoom out” section of UCSC Genome Browser on the top right, click on the “10x” button. This will zoom out of this area 10 times.
- Make sure the browser is showing you approximately the following coordinate interval: chr19:18,425,701-18,625,700
- Configure the track (by right-clicking on the recently loaded Hi-C track) and selecting “Configure K562 Hi-C”. Specifically, in the opened window:
  - Select “NONE” in the “Score normalization” section. 
  - For “Draw mode<a name="_int_ntotqic1"></a>”, select “triangle<a name="_int_ukfdby11"></a>”.
  - Check “Auto Scale” check box.
  - For “Resolution” select “5.0 kB<a name="_int_2cf4fzlg"></a>”.
  - Click OK.
- Make a screenshot of the TAD(s).

**Q9.** Consider varying the other parameters that could be changed in the HiC track’s configuration panel (these configurations can be accessed by right	 clicking on the HiC track). Describe on a slide, the aim of at least one configuration and how it changes the shown track.

**Q10.** Using the identified TAD(s), determine the most likely set of genes that are affected by our variant of interest. Mention their name in the corresponding slide.

\--------------------------------------

We can perform additional confirmatory analyses to verify that indeed the identified TADs are correct. One example analysis could be to check and see if the TADs borders are bound by genomic elements that restrict chromatin interactions (and form TADs as a result). In particular, we want to validate the presence of bound architectural proteins at the TAD borders.


**Q11.** Which architectural protein is typically found to be bound at TAD boundaries? Is this factor present at our TAD(s) boundaries? Take a screenshot of the TAD in a way that the loaded factor track is also visible.

Hints:

- Using “track search” functionality, search for: “K562 *<Factor Name>*”.
- Many tracks will be shown, choose the one that has the following description “ChIP-seq Signal from ENCODE/Broad<a name="_int_ydz1ud1x"></a>”. With this, we are loading a track with maximum details (hence the name “Signal”), instead of only looking at the peaks in the data.
- Make sure the “Visibility” is set to full.
- Click on “View in browser” or “Return to Browser<a name="_int_0of721hs"></a>”.

**------------------------------------**

For a gene to be controlled by enhancers within a TAD, it should be an actively expressed gene. If a gene is inactive (i.e., silent), it is unlikely to be affected by a non-functional enhancer (or a variant). We will look at the expression of the genes located within our region of interest in the genome.

**Q12.** Which genes are active (or expressed) in the K562 cell line? Take a screenshot of the recently loaded track in which genes and their expression in the tissue of origin is shown. No need to include all loaded tracks in this screenshot.

Hints:	

- The tissue of origin of the K562 cell line is blood.
- You can use GTEx expression track for this. In the UCSC Genome Browser, scroll down until you find the “Expression” section. Look for “GTEx Gene V8” track. Once found, click on the text to go to its configuration page.
- Underneath, there are many check boxes. Click on “clear all” button to make sure all check boxes are inactive.
- Click on “Whole\_Blood” mark and make it active.
- On the top of the page, look for a dark blue “Go” button at the center. Before clicking the button, make sure the “full” option on its left is selected.
- In this visualization, each bar represents expression of a gene in “Whole Blood” tissue.

\--------------------------------------

Further, we hypothesize that the affected gene is unlikely to be a housekeeping gene (i.e., a gene that is ubiquitously expressed across tissues) and it should be a more tissue-restricted gene that is causing the disease (e.g., leukemia). To examine this, we will compare expression of the candidate genes across multiple cell types.

Hints:

- You can again use “GTEx Gene V8” track (you added this track in **Q12**).
- Again, click on “GTEx Gene V8” link that is located below the visualized tracks to start the configuration.
- This time, select the following tissue types:
  - Brain-Cortex
  - Liver
  - Pancreas
  - Heart - Atrial Appendage
  - Skin - Not Sun Exposed (Suprapubic)
  - Whole Blood
- On the top of the page, click on the “Go” button.
- In this visualization, each bar represents expression of a gene in a particular cell-type. Each color represents gene expressions of a specific cell-type. Using this visualization, you can easily see the expression levels of genes in multiple cell-types at the same time.


**Q13.** What are the remaining candidate genes that are expressed in a more tissue-restricted manner (i.e., mostly active *only* in the whole blood and no other tissue types)?


\----------------------------------

Now that we understand the genomic context of our risk variant, it would be nice to validate this experimentally by deleting the enhancer and subsequently checking the expression of its prime candidate gene by cDNA qPCR (RT-qPCR). The first step for this is to design two CRISPR-Cas9 guide-RNAs to delete the enhancer. To delete the entire enhancer region, one guide-RNA should target the 5’side of the enhancer, the other one the 3’.

**Q14.** Design the two CRISPR-Cas9 guide-RNAs that are necessary for the deletion of our enhancer.

Hints:

- You can use the following tools:
  - <https://www.atum.bio/eCommerce/cas9/input> (recommended)
  - <http://chopchop.cbu.uib.no/>
- We suggest you use the enhancer’s coordinates in the above websites. 
- Select either the start or end coordinate and subtract or add up-to 3 kb, respectively. The exact result is not important here, we aim to learn how this should be done. Just keep in mind that we are aiming to delete the entire enhancer region.
- We recommend selecting a region around 3 kb (not larger) to facilitate the computational requirements on the website.
- If you are using atum, make sure to select “Wild-type Cas9”
- Click “Search”
- In the corresponding slide, include the coordinates of the sequence that needs to be deleted. Then, add a screenshot of the designed guide RNAs delivered by the website. 

\-------------------------------------

**Q15.** In this assignment, we would like to measure the expression level of the identified candidate gene after deletion of the enhancer. We will do this by performing cDNA qPCR which requires designing primers. In the corresponding slide, provide the sequence as well as the coordinates from which the sequence is selected.

Hints:

- Return to the UCSC Genome Browser website.
- If RefSeq track is not visible, go to “Genes and Gene Predictions” section in the UCSC Genome Browser and select “Full” option in the “NCBI RefSeq” element.
- Click on the candidate gene in the RefSeq track.
- Copy the RefSeq accession ID
- <a name="_int_9dpfw2mk"></a>To design primers you can use the NCBI primer-blast website at: <https://www.ncbi.nlm.nih.gov/tools/primer-blast/>
- Paste the RefSeq ID in  “Enter accession, gi, or FASTA sequence” section. 
- Under “Exon/Intron selection” -> “Exon junction span” -> select “primer must span an exon-exon junction” or “Primer pair must be separated by at least one intron on the corresponding genomic DNA” (Bonus question: why do you think it is important that the primer spans an exon or must be separated by at least one intron?).
- Take a screenshot of this page. This screenshot is sufficient as an answer for the current question (i.e., **Q15**). 
- Press “Get Primers” button at the end of the webpage. The processing can take a while depending on how busy the server is (5 min).
- The result is a set of sequences that can be used as primers for performing cDNA qPCR experiment. If you get to the results, you can add an additional slide and place a screenshot of the result page there.


