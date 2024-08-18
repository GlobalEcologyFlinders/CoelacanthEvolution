# Coelacanth evolution
<a href="https://doi.org/10.5281/zenodo.8054092"><img src="https://zenodo.org/badge/DOI/10.5281/zenodo.8054092.svg" alt="DOI"></a><br>
Analyses accompanying article on coelacanth evolution.<br>
<img align="right" src="www/coelacanth.png" alt="Latimeria chalumnae" width="400" style="margin-top: 20px">
<br>
<br>
Prof <a href="https://globalecologyflinders.com/people/#DIRECTOR">Corey J. A. Bradshaw</a> <br>
<a href="http://globalecologyflinders.com" target="_blank">Global Ecology</a> | <em><a href="https://globalecologyflinders.com/partuyarta-ngadluku-wardli-kuu/" target="_blank">Partuyarta Ngadluku Wardli Kuu</a></em>, <a href="http://flinders.edu.au" target="_blank">Flinders University</a>, Adelaide, Australia <br>
June 2023<br>
<a href=mailto:corey.bradshaw@flinders.edu.au>e-mail</a> <br>
<br>
article:<br>
<a href="https://www.flinders.edu.au/people/alice.clement">CLEMENT, AM</a>, <a href="https://www.uqar.ca/universite/a-propos-de-l-uqar/departements/departement-de-biologie-chimie-et-geographie/cloutier-richard">R CLOUTIER</a>, <a href="https://www.flinders.edu.au/people/mike.lee">MSY LEE</a>, <a href="https://www.benedictking.com">B KING</a>, <a href="https://scholar.google.com/citations?user=6LHmxgUAAAAJ&hl=en">O VANHAESEBROUCKE</a>, <a href="https://globalecologyflinders.com/people/#DIRECTOR">CJA BRADSHAW</a>, <a href="https://sites.google.com/site/hugodutel/home">H DUTEL</a>, <a href="https://staffportal.curtin.edu.au/staff/profile/view/kate-trinajstic-f0dcf6b1/">K TRINAJSTIC</a>, <a href="https://www.flinders.edu.au/people/john.long">JA LONG</a>. 2024. A Late Devonian coelacanth reconfigures actinistian phylogeny, disparity, and evolutionary dynamics. <em>Nature Communications</em> in press
<br>

## Abstract 
The living coelacanth <em>Latimeria</em> (Sarcopterygii: Actinistia) is an iconic so-called ‘living fossil’ within one of the most morphologically conservative vertebrate groups. We describe a new, exceptionally preserved 3-D coelacanth from the Late Devonian Gogo Formation in Western Australia. We assembled the most comprehensive analysis of the group to assess the phylogeny, evolutionary rates, and morphological disparity of all coelacanths. The new fossil fish fills a critical transitional stage in coelacanth disparity and evolution. We revealed a major shift in morphological disparity between Devonian and post-Devonian coelacanths. Since the mid-Cretaceous, discrete character changes (representing major morphological innovations) have essentially ceased, while meristic and continuous characters have continued to evolve within coelacanths. Considering a range of putative environmental drivers, tectonic activity best explains variation in the rates of coelacanth evolution.

## <a href="https://github.com/cjabradshaw/CoelacanthEvolution/tree/main/scripts">Scripts</a>
### 1. <a href="https://github.com/cjabradshaw/CoelacanthEvolution/tree/main/scripts/BRT">phylogenetics</a>
- <code><a href="https://github.com/cjabradshaw/CoelacanthEvolution/tree/main/scripts/phylogenetics/BEAST">BEAST</a></code> (Bayesian phylogenetic analysis of discrete, meristic and continuous traits; written by <a href="https://github.com/Michael-S-Y-Lee">Mike Lee</a>)
- <code><a href="https://github.com/cjabradshaw/CoelacanthEvolution/tree/main/scripts/phylogenetics/PAUP">PAUP</a></code> (parsimony analysis of discrete traits; written by <a href="https://github.com/Michael-S-Y-Lee">Mike Lee</a>)
<img align="center" src="www/coelphylogeny.png" alt="coelacanth phylogeny" width="800" style="margin-top: 20px">

### 2. <a href="https://github.com/cjabradshaw/CoelacanthEvolution/tree/main/scripts/evolrate">rates of evolution</a>
- <code><a href="https://github.com/cjabradshaw/CoelacanthEvolution/blob/main/scripts/evolrate/rates_through_time.R">rates_through_time.R</a></code> (developed by <a href="https://github.com/king-ben">Ben King</a>): R code for plotting the uncorrelated log-normal (UCLN) clock rates through time requires BEAST time treefile (concatentated, post-burnin) for input. This file contains 8000 trees and is 2 GB, and might have to be subsampled (thinned) due to memory constraints to run the script; plots in article subsampled every 5<sup>th</sup> tree. Tree file included here (<a href="https://github.com/cjabradshaw/CoelacanthEvolution/blob/main/scripts/evolrate/Coelacanths_87_268_tipsVariance_Dis_Mer_Con_uclnG_RootExp418_MC3_sumBi20%3Athinned.trees">Coelacanths_87_268_tipsVariance_Dis_Mer_Con_uclnG_RootExp418_MC3_sumBi20/thinned.trees</a>) is only the first 10 trees from this subsampled file (~ 2 MB).
- <code><a href="https://github.com/cjabradshaw/CoelacanthEvolution/blob/main/scripts/evolrate/functions.R">functions.R</a></code>: R source functions called in <code>rates_through_time.R</code>
- <code><a href="https://github.com/cjabradshaw/CoelacanthEvolution/blob/main/scripts/evolrate/epoch_clock.R">epoch_clock.R</a></code>: R code to create <em>epoch_clock</em> plot (below)
<img align="center" src="www/epoch_clock.png" alt="epoch clock" width="800" style="margin-top: 20px">

### 3. <a href="https://github.com/cjabradshaw/CoelacanthEvolution/tree/main/scripts/disparity">disparity</a>
<img align="right" src="www/fishshape.png" alt="disparity" width="80" style="margin-top: 20px">
- <code><a href="https://github.com/cjabradshaw/CoelacanthEvolution/blob/main/scripts/disparity/disparity.R">disparity.R</a></code> (developed by <a href="https://scholar.google.com/citations?user=6LHmxgUAAAAJ&hl=en">Olivia Vanhaesebroucke</a>): R code for disparity analyses and figure.

### 4. <a href="https://github.com/cjabradshaw/CoelacanthEvolution/tree/main/scripts/BRT">environmental drivers of evolution rate</a>
<img align="right" src="www/decisiontree.png" alt="decision tree" width="100" style="margin-top: 20px">
- <code><a href="https://github.com/cjabradshaw/CoelacanthEvolution/blob/main/scripts/BRT/Coelacanth%20evolR-envir%20model.R">Coelacanth evolR-envir model.R</a></code> (developed by <a href="https://github.com/cjabradshaw">Corey Bradshaw</a>): R code to reproduce the resampled boosted regression tree analysis for determining the environmental drivers of coelacanth rate of evolution.

## <a href="https://github.com/cjabradshaw/CoelacanthEvolution/tree/main/data">Data</a>
- <a href="https://morphobank.org/index.php">Morphobank</a> (morphological matrices) <a href="http://morphobank.org/permalink/?P3471">Project 3471</a> (project leader: <a href="https://www.flinders.edu.au/people/alice.clement">Alice Clement)</a>: project <a href="https://github.com/cjabradshaw/CoelacanthEvolution/tree/main/data/Morphobank">SSD files</a>
- <em><a href="https://github.com/cjabradshaw/CoelacanthEvolution/blob/main/data/Postcranial.TPS">Postcranial.TPS</a></em>, <em><a href="https://github.com/cjabradshaw/CoelacanthEvolution/blob/main/data/Jaws.TPS">Jaws.TPS</a></em>, <em><a href="https://github.com/cjabradshaw/CoelacanthEvolution/blob/main/data/Skull.TPS">Skull.TPS</a></em>: TPS files with landmarks coordinates for the three morphological disparity analyses with geometric morphometrics
- <em><a href="https://github.com/cjabradshaw/CoelacanthEvolution/blob/main/data/Matrix_corrected.nex">Matrix_corrected.nex</a></em>: Nexus file containing corrected matrix for morphological disparity analysis with discrete characters
- <em><a href="https://github.com/cjabradshaw/CoelacanthEvolution/blob/main/data/Age-habitat.xlsx">Age-habitat.xlsx</a></em>, <em><a href="https://github.com/cjabradshaw/CoelacanthEvolution/blob/main/data/Age-habitat-Jaw%20.xlsx">Age-habitat-Jaw.xlsx</a></em>, <em><a href="https://github.com/cjabradshaw/CoelacanthEvolution/blob/main/data/Age-habitats-GM-PC.xlsx">Age-habitat-GM-PC.xlsx</a></em>, <em><a href="https://github.com/cjabradshaw/CoelacanthEvolution/blob/main/data/Age-habitat-Skull.xlsx">Age-habitat-Skull.xlsx</a></em>: Excel files with the list of species and their ages for disparity analyses (figures)
- <em><a href="https://github.com/cjabradshaw/CoelacanthEvolution/blob/main/data/coelacanthDatV2.csv">coelacanthDatV2.csv</a></em> (compiled by <a href="https://www.uqar.ca/universite/a-propos-de-l-uqar/departements/departement-de-biologie-chimie-et-geographie/cloutier-richard">Richard Cloutier</a>): rate of evolution and environmental data (continental flooding area<sup>1</sup>, subduction flux<a href="http://doi.org/10.1016/j.gr.2021.05.016"><sup>2</sup></a>, atmospheric [CO<sub>2</sub>]<a href="https://doi.org/10.1126/sciadv.aat4556"><sup>3</sup></a>, sea surface temperature<a href="https://doi.org/10.1007/s12583-018-1002-2"><sup>5</sup></a>, dissolved [O<sub>2</sub>]<a href="https://doi.org/10.1007/s12583-018-1002-2"><sup>4</sup></a>

<sup>1</sup><a href="https://doi.org/10.1016/j.gr.2022.05.011">Marcilly <em>et al</em></a>. 2022 <em>Gondwana Res</em> 110:128;
<sup>2</sup><a href="http://doi.org/10.1016/j.gr.2021.05.016">Marcilly <em>et al</em></a>. 2021 <em>Gondwana Res</em> 97:176;
<sup>3</sup><a href="https://doi.org/10.1126/sciadv.aat4556">Witkowski <em>et al</em></a>. 2018 <em>Sci Adv</em> 4:3aat4556;
<sup>4</sup><a href="https://doi.org/10.1007/s12583-018-1002-2">Song <em>et al</em></a>. 2019 <em>J Earth Sci</em> 30:236
<br>

## Required <a href="https://cran.r-project.org/">R</a> libraries
<a href="https://cran.r-project.org/"><img align="right" src="www/R logo.png" alt="R logo" width="60" style="margin-top: 20px"></a>
<a href="https://cran.r-project.org/web/packages/cluster/index.html"><code>cluster</code></a>, <a href="https://www.rdocumentation.org/packages/data.table/versions/1.14.8"><code>data.table</code></a>, <a href="https://cran.r-project.org/web/packages/dismo/index.html"><code>dismo</code></a>, <a href="https://www.rdocumentation.org/packages/dispRity/versions/1.7.0"><code>dispRity</code></a>, <a href="https://cran.r-project.org/web/packages/dplyr/vignettes/dplyr.html"><code>dplyr</code></a>, <a href="https://www.rdocumentation.org/packages/gbm/versions/2.1.8.1"><code>gbm</code></a>, <a href="https://www.rdocumentation.org/packages/geoscale/versions/2.0/topics/geoscale-package"><code>geoscale</code></a>, <a href="https://ggplot2.tidyverse.org/"><code>ggplot2</code></a>, <a href="https://cran.r-project.org/web/packages/ggrepel/vignettes/ggrepel.html"><code>ggrepel</code></a>, <a href="https://bookdown.org/rdpeng/RProgDA/the-grid-package.html"><code>grid</code></a>, <a href="https://momx.github.io/Momocs/"><code>Momocs</code></a>, <a href="https://www.rdocumentation.org/packages/phylotate/versions/1.3"><code>phylotate</code></a>, <a href="https://www.rdocumentation.org/packages/phytools/versions/1.5-1"><code>phytools</code></a>, <a href="https://www.rdocumentation.org/packages/plyr/versions/1.8.8"><code>plyr</code></a>, <a href="https://readxl.tidyverse.org/"><code>readxl</code></a>, <a href="https://cran.r-project.org/web/packages/reshape2/index.html"><code>reshape2</code></a>, <a href="https://scales.r-lib.org/"><code>scales</code></a>, <a href="https://stat.ethz.ch/R-manual/R-devel/library/stats/html/00Index.html"><code>stats</code></a>, <a href="https://www.tidyverse.org"><code>tidyverse</code></a>, <a href="https://cran.r-project.org/web/packages/vegan/index.html"><code>vegan</code></a>
<br>
<img align="center" src="www/Ngamugawi wirngarri.jpg" alt="Ngamugawi wirngarri" width="400" style="margin-top: 20px">
<br>
<br>
<p><a href="https://www.flinders.edu.au"><img align="bottom-left" src="www/Flinders_University_Logo_Horizontal_RGB_Master.png" alt="Flinders University" width="140" style="margin-top: 20px"></a> &nbsp; <a href="https://globalecologyflinders.com"><img align="bottom-left" src="www/GEL Logo Kaurna New Transp.png" alt="GEL" width="75" style="margin-top: 20px"></a> &nbsp; &nbsp; <a href="https://www.uqar.ca/"><img align="bottom-left" src="www/UQARlogo.png" alt="UQAR" width="90" style="margin-top: 20px"></a> &nbsp; &nbsp; <a href="https://www.samuseum.sa.gov.au/"><img align="bottom-left" src="www/SAMlogo.png" alt="SAM" width="100" style="margin-top: 20px"></a> &nbsp; &nbsp; <a href="https://www.bristol.ac.uk"><img align="bottom-left" src="www/UBlogo.png" alt="UB" width="80" style="margin-top: 20px"></a> &nbsp; &nbsp; &nbsp; <a href="https://www.naturalis.nl/en"><img align="bottom-left" src="www/NBClogo.png" alt="NCU" width="50" style="margin-top: 20px"></a> &nbsp; &nbsp; &nbsp; <a href="https://www.curtin.edu.au/"><img align="bottom-left" src="www/CUlogo.png" alt="CU" width="40" style="margin-top: 20px"></a> &nbsp; &nbsp; &nbsp; <a href="https://www.eva.mpg.de/index/"><img align="bottom-left" src="www/maxplancklogo.png" alt="Max Planck" width="80" style="margin-top: 20px"></a></p>
