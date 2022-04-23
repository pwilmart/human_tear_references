# human_tear_references

### Review of Human Tear Quantitative Proteomics References

Please see `References_20220420.xlsx` in this repository.

## Preface

This blog-like post is not a review of human tears or tear collection methods. Nor is it a proper review of quantitative proteomics methods. It is **my personal assessment** of the quantitative proteomics methods used in these publications. Specifically the study design, choice of quantitative proteomics method (as it relates to the tear proteome), analytical measurement platforms, data analysis methods, and statistical analysis of the data. My expertise lies in the middle parts of proteomics experiments (data acquisition, data processing, statistical analyses, data summarization, and communication of results). Those are my areas of interest in these 80 papers. These papers may make significant contributions to our knowledge of tears that are outside my areas of interest and will be beyond the scope of my assessment. My apologies to the authors of these papers if I fail to mention important aspects of your work.

## Background

I have been involved in a project comparing human tear proteins to look for changes in relative tear abundances associated with different biological groups. We have been doing methods development to prepare for the larger numbers of subjects in the clinical sample set. We are using TMT labeling of tear samples collected with Schirmer's strips.

This are kind of an old school comparative proteomics experiments. Tears are a biological fluid that can be collected non-invasively (is anything really non-invasive?) that has potential to reflect corneal health and lacrimal gland health. The study design seems simple on paper. Collect tears in some standardized way from patients with a condition of interest and from appropriately matched healthy subjects. Some kind of proteomics methods will be used to compare the relative abundances of proteins or peptides (depending on analysis method). This is a type of study that we have been trying to do in proteomics for more than two decades.

## Quantitative Proteomics History

We are all aware of how much mass spectrometers have improved over the years. They are the show pieces of proteomics and, as such, receive much attention. Every aspect of the instruments have gotten better (except the prices): they are more sensitive, faster scanning, have high resolutions, amazing mass accuracies, better stability, and sophisticated data acquisition systems. The chromatography methods (liquid and gas phase) have also seen dramatic improvements in sensitivity and performance while retaining their **classic reliability**. Sample processing steps, which are critical in studies where larger and larger sample cohorts are needed to study human biology, are constantly improving. More automated sample processing solutions are offered every year.

What we do today bears little resemblance to the "gold standard" methods of past proteomics eras (classic proteomics? proteomics priors?). Nearly three decades is a long time in a fast moving technological field like proteomics. Many fundamentally different methods to compare and contrast proteomes have come and gone over the years. I will mention a few of the quantitative proteomics methods that I have seen come and go over the years (and that have been used for human tears).

#### SELDI

In the early 2000s, whole protein profiling was marketed as a way to classify healthy versus disease conditions. [SELDI-TOF](https://www.nature.com/articles/nmeth0505-393) was a commercial platform for proteome profiling. I like to think of [Seer's nanoparticles](https://seer.bio/) as SELDI beads. SELDI did not have any reliable way to figure out what proteins were making samples different, so it was of limited utility to find biomarkers or gain mechanistic insights into disease.

#### 2D-PAGE

Another oldie but goody from the early days of proteomics was [2D-PAGE](https://en.wikipedia.org/wiki/Two-dimensional_gel_electrophoresis). Despite having very high protein resolving power, its success was **spotty** at best. Ha-ha. 2D gels resolve proteins by isoelectric point in the x-axis and by molecular weight in the y-axis. With Coomassie or silver staining, you have a satisfying visual representation of your proteome. It goes downhill from there. There is limited amount of protein that can be loaded and that gives about 2 order of magnitude dynamic range for visual stains and maybe another decade with fluorescence stains. The protocol is difficult to perform and the gel-to-gel reproducibility is poor. Quantitation involved image analysis software that has to warp gel coordinates to try and match spots across gels based on nearby spot landmarks. The method evolved into [DIGE](https://en.wikipedia.org/wiki/Difference_gel_electrophoresis) where proteins were labeled with multiplexed dyes. While that helped in aligning gels, the ability to pick visible spots for digestion and identification was harder. 2D-PAGE ended up all show and no go. Many precious samples were sacrificed to the 2D-PAGE gods and took their biological secrets to the biohazard container in the sky.

#### 1D-PAGE

1D-PAGE is an established way to separate and visualize proteins. In-gel digestion works well and is mass spec compatible. There are several ways to use 1D-PAGE in proteomics: you can excise individual bands, excise entire lanes (usually after a short run in), or cut lanes into multiple pieces (like multiple fractions). These methods work okay but are more difficult to automate for larger study designs. Use of 1D-PAGE has been declining as the years go by.

#### Labeling

In solution digestion methods and liquid chromatography separations are the norm now. Initially, methods relied on stable isotope labeling for quantitative measurements. There have been many labels with limited multiplexing capability developed over the years: iCAT, SILAC, dimethyl, iTRAQ, and others. The limited number of label masses was always a challenge for biological studies where larger replicate numbers are needed. iTRAQ (like iCAT) was a little too ahead of its time. It could have used more channels (initially 4 but later increased to 8) and instruments to generate the reporter ions were not very fast or sensitive when the tags were first released. Tandem mass tags (TMT) are one of the few labeling methods able to add sufficient channels to remain in use. TMT started with six channels and is currently up to 18 channels. Methods to use multiple TMT kits in studies have also been developed.

#### Label-Free

The need to run many samples led to label-free methods. These methods typically digest each sample and run the peptides in a single reverse-phase LC run (single shot). Matching m/z values and retention times (RT) across runs is an important requirement, so high mass accuracy/resolution instruments and stable chromatography set ups are critical. Mass spectrometry peaks at defined m/z and RT are called MS1 "features". The areas or peak heights of the features can be summed to estimate the relative protein abundances. This sounds simple enough on paper but can be hard to pull off. A less powerful variation of label-free analyses uses spectral counting to compare the protein abundances. This is computationally more straightforward because it is basically a byproduct of identifying peptides and inferring proteins. MS1 feature methods suffer from missing data because the instruments cannot sample every eluting peptide in the limited LC times. Spectral counting suffers from poor statistical power when count values are small.

#### Current Methods

The current hot quantitative proteomics methods are DIA (the new kid on the block) and TMT with newer kits and acquisition methods. DIA methodologies are under active development. Great improvements have been made and DIA gets closer to what single shot label free experiments were supposed to be able to deliver. Being able to quantify signals across all runs for almost anything you can fragment and identify eliminates most missing data. The dynamic range limitations of single shot proteomics are a more fundamental challenge that does not seem to be discussed as much.

TMT has been around since 2003 (yes, that date is correct). The instrumental requirements to generate reporter ions (not possible on low resolution ion traps due to low m/z cutoffs) that hindered iTRAQ also affected early use of TMT. Eventually Orbitraps could do TMT (the reagents are also from Thermo) and use of TMT grew. Early experiments with iTRAQ and TMT used reporter ion intensities from MS2 scans. Measurement accuracy issues were discovered and it took a few years to develop new types of instrument configurations and data acquisition modes to (mostly) overcome these issues. There are sill more improvements to TMT experiments underway (FAIMS and real time search, to mention a couple) and the method is still growing.  

## Literature Search

I used a few different search strings in PubMed to find human tear proteomics studies. `Human tear` (tear and tear [to rip something] are both biological terms...) was used in combination with `protein*` or `proteom*` and/or in combination with `mass spec*`. It is hard to specify all of the keywords for comprehensive literature searches. Commonly used terms for the same things change over time. Clinical investigators describe analytical methods differently that do analytical scientists.

These searches produce a lot of matches. I was not interested in really old work (late 1990s up through early 2000s) because I knew first hand what methods we had back then. There are many PubMed matches that have little to do with what you want. You have to look at titles, author lists, and abstracts to see if papers are potentially useful. PubMed lets you checkmark papers in a session so you can download a file with the results. A half day later, I had 60 papers to begin with. During the course of reading those papers and the papers they cited, I added another 20 papers to the list.

This search is not 100% comprehensive. There are always more things to try. Google Scholar tracks citations of papers. Another way to find other related work is to pick a few likely high impact papers and see who has cited those studies. The list ranged from 1998 to 2022 publication dates. There are papers using most quantitative methods mentioned above on a wide range of analytical platforms. There are different tear collection methods being evaluated, different proteomics methods being evaluated, etc. It is a good sampling of work to see how quantitative proteomics has matured and how some methods have aged.

## Information Extraction

I constructed an Excel spreadsheet (`References_20220420.xlsx`) to tabulate a variety of extracted information from the 80 published studies. The sheet is in the GitHub repository with this README. There are things like the author lists, the title, journal details, PubMed link, and several fields populated while reading each paper. Around 30 to 45 minutes was spent reading each paper and summarizing details. You cannot tell much about a study design from the abstract. In nearly all of the studies, for example, the number of subjects that tears were collected from (usually stated in the abstract) was not the number of biological replicates used in the proteomics study (those numbers might be found at the end of the Introduction, in the Methods, or in the Results). I did not make any attempt to summarize study conclusions. The papers mostly had different study goals, so direct comparisons of results did not make much sense.

## Common Issues   

#### Sensitivity and Pooling

Early quantitative methods could not accommodate large numbers of samples. Older instruments and LC methods were much less sensitive. The amount of protein required per sample was often a challenge with tears where volume of tears collected might be rather small (especially for dry eye diseases). This often led to sample pooling to get more protein per pooled sample and/or to reduce the number of biological subjects to something that the proteomics methods could handle. For example, if you had 10 subjects in each of 4 biological groups and you were doing a 4-channel iTRAQ experiment, pooling samples from each group might seem logical. Pooling turns your quantitative study into a qualitative study. Information about biological variability is lost in the chemical averaging (mixing samples).

#### Matching Proteome to Quant Method

When you are first characterizing a bio fluid like human tears, little is known about the composition (the proteins present and their relative abundances). That makes it hard to match the nature of your sample to an appropriate proteomics method. Many of the 80 studies I looked at used proteomics methods that were not very good choices for human tears. Tear is a wide dynamic range proteome (maybe there is a better term). It has several highly abundant tear-specific proteins produced by the lacrimal gland. There are also lower abundance proteins that come from glandular secretion leakage and cellular proteins of various origins that come from the cornea and surfaces of the eye lids. I am not a tear expert and I will not waste your time by reading my poor summary of human tears.

#### Secreted Bio Fluids

There are some proteomics basics with bio fluids. Secreted proteins have sequences in FASTA files that include the N-terminal signal peptide. Those residues are removed from the actual proteins. The first tryptic peptide of the actual protein will not match the theoretical digest peptides from the FASTA sequence. There are also endogenous proteases in bio fluids and some proteins may be processed into mature/active forms. You need to specify semi-tryptic searches to identify peptides in bio fluids. This was not done in any of the 80 papers.

#### Relative Abundance Dynamic Range

When you have samples with low abundance proteins that will be hard to detect, you need a sensitive platform, you have to load more total digest, or you have load more digest and use fractionation. The MudPIT concept has been around since the late 1990s. The chromatography systems have limited dynamic range, the instrument scans have limited dynamic range, the instrument has limited duty factor, etc. Fractionating your samples helps overcome these limitations and increase the proteomics depth. Detecting a few tens to a few hundred tear proteins is insufficient for proteome profiling. Many early quantitative proteomics methods were incompatible with fractionation.

#### Stimulated Tears

Have you ever chopped an onion? Your eyes respond to dry environments and irritation through reflex tearing (stimulated tearing). The composition of basal tears versus reflex tears are not the same. Most proteomics protocols run the same total amount of something (micrograms proteins, amount of peptide digest, etc.). If you have some highly abundant tear proteins increased during reflex tearing and your subjects have some degree of reflex tearing, that will push all of the other proteins in tears down in relative abundance. You have to correctly normalize data taking this into account to compare samples and not get false changes. This is a challenging problem that was seldom mentioned in the papers I read.

#### Inconsistent Proteins of Interest

There were small numbers of proteins listed as important candidates across the studies. However, there was little consensus on those proteins. If tears can serve as a source of biomarkers for monitoring eye health, sources of bacteria and irritation (like contact lenses) should elicit some sort of general response (increased anti-microbial proteins, increased immunoglobulins, changes in markers of inflammation, etc.). Some of the proteins of interest should be present in multiple studies. That was not really the case.

## Disclaimers

Out of the 80 papers, I have one flagged as good (for tear proteome characterization and not for good quantitative study design). However, I believe these are all good faith papers where the best techniques that the authors could employ were used to study tears to the best of their abilities **at that time**. Most of these papers are not by big name labs that specialized in proteomics. Quantitative proteomics methods have always been (and continue to be) very challenging. Most of the early methods mentioned above had some utility (at least for some types of samples) but were beyond the proteomics expertise of most labs, except for the labs that developed those methods.

These papers all met the bar for publication **at that time**. Like so many things, the bar keeps changing. Many of these studies might not meet the standards for publication by today's standards. We have better instruments and methods that can process more biological replicates. What gets over today's bar are papers where the methods are considered reasonable **by today's standards**. It might be wise to not sit on data for too long, or your window for publication may close. At some point, methods will have improved so much that it really makes more sense to repeat experiments with better methods.

## What are the Lessons?

You have to be pretty old and have been hanging out in the lab for way too long to be able to pass judgement on papers from more than 10 years ago (let alone 20+ years ago). It may be difficult for younger proteomics researchers to get a sense of the back stories and contexts for older proteomics work. This is a time to go talk to the "old" folks (or post something on Twitter) to get some perspective. A bigger problem is how non-proteomics experts (like clinical ophthalmologists) might perceive this tear literature. How do those folks know that many of these papers may not be that useful to read or cite? This has always been a challenge for the scientific record and the problem seems to be growing as the number of publications increase and the barriers to access scientific studies decrease.

Human tears are not one of the systems that has had much focus from the "big name" labs over the years. Serum has been, and continues to be, the major focus of biomarker work. However, I think tears are probably representative of much proteomics work that has been published over the years. A lot of proteomics work happens in smaller labs with non-experts trying to use proteomics in their studies. Proteomics studies are more variable and difficult to optimize compared to genomic studies, but we are making advances. We need to figure out better ways to communicate to a broader audience how to do quantitative proteomics experiments. We need less focus on cutting edge proof of principle papers and more focus on the important concepts like study designs, proper replicate numbers, matching methods to samples, quality control, sanity checks, etc.

---

Thanks for reading! </br>
Phil Wilmarth, OHSU </br>
April 20, 2022    
