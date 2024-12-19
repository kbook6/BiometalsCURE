# BiometalsCURE
Side research on heme and hemoglobin related genetic disorders as a part of the Biochemistry II Laboratory capstone project. This project was also my capstone for the international program designation.
Below is the write-up requirement for the international program designation. 
--------------------------------------------------------------------------------------------------------------------------------------------------
**Heme and Hemoglobin Related Genetic Disorders** 
**IP Capstone Project | Katherine Book | Fall 2024**

**Introduction** 

The purpose of the International Plan capstone is to incorporate global connection within our degree program. For biochemistry students, this culminates in a portion of the CHEM 4582 Biochemistry Lab II semester project. For my project, I aimed to tie my study abroad experiences to the classes I have taken, and present that part as an addition to my team’s final project. I first studied abroad with the Georgia Tech BEST Lyon Program at CPE University in the summer of 2022. I then spent the following fall in Barcelona with the Georgia Tech Barcelona Fall Program. I also volunteered for a week in Chone, Ecuador, at the Regeneration Field Institute. These experiences influenced me to focus on two geographic regions: Europe and South America.  
The final project in biochemistry lab II was the Course-Based Undergraduate Research Experience, a project in which teams worked with stakeholders from a research lab on campus. I was a part of the Biometals CURE with Dr. Amit Reddi and Dr. Ryan Allen. Our goal was to determine if zinc and gallium protoporphyrins effectively mimic heme binding to human serum albumin, myoglobin, and hemoglobin. Since heme is involved in lots of hereditary diseases, I decided to take a bioinformatics approach to make a global connection. I did a similar project in Genomics and Applied Bioinformatics, in which I looked at sickle cell disease variants within the 1000 Genomes Project. Thus, after consulting with Dr. Allen, I decided to analyze more hereditary diseases that were related to heme or hemoglobin.  

**Background Information** 

The 1000 Genomes Project is an open-source database containing genetic information. It offers several phases of samples. I used Phase 3 GRCh38, which came out in 2017 and contained sample genetic information on 2504 individuals. I focused on three hereditary diseases: sickle cell disease, beta thalassemia, and hereditary hemochromatosis. 
Sickle cell disease, also known as sickle cell anemia, is a condition in which red blood cell formation is abnormal and results in a sickle-shape due to a malformed hemoglobin protein. This is caused by variant 334, a mutation in the HBB gene on chromosome 11. Sickle cell disease is known to cause pain, stroke, lung disease, and a variety of other conditions. I analyzed sickle cell anemia in my Genomics and Applied Bioinformatics course (BIOS 4150), and thus it served as a sort of reference variant in this study to ensure the experiment was running correctly.  
The second disease analyzed was beta thalassemia, which is a disease also caused by a malformed hemoglobin protein, in this case due to malformed or missing beta subunits. It also is caused by a variant on the HBB gene, identified as rs33971634. Beta thalassemia can cause anemia, stunted growth, and other possible long-term effects due to iron overload.  
The final disease I analyzed was hereditary hemochromatosis, a disease in which iron builds up in the body over time. Two variants contribute to two forms of hemochromatosis: rs1800562, which accounts for around 85% of all hereditary hemochromatosis cases; and rs1799945, which causes a milder case of the disease. Both variants are found in the HFE gene on chromosome 6. This disease can lead to heart problems, liver cancer, and other conditions, but can also go undetected. It is also common within people of European ancestry, which made it more related to this project.  

**Methodology**

I used Jupyter Notebook to extract the information from the 1000 Genomes Project. Jupyter Notebook is a web-based coding platform that we use in Genomics and Applied Bioinformatics that I decided to use for this as well since the environment needed to run the commands was already created for me to use from that class. I first extracted the population information from the 1000 Genomes Project by copying the pre-created metadata file to my folder. This file contained the sample IDs, population, super population and gender of each sample. To make the information easier to access, I copied only the sample IDs and their populations to a text file. I then extracted variant information by downloading the chromosome information from the 1000 Genomes Project as well. I downloaded chromosome 6 and chromosome 11 data and analyzed the variants according to their respective chromosomes. I then used BCFtools to view samples that contained the variant based on the variant ID (rs########) and extract it to a text file. This command is a common bioinformatics tool used to analyze variant call format files. Finally, I used ChatGPT to help write Python code that would cross-reference the sample information text file with the variant information text file to count the number of samples that contained the variant in each population. After conducting this for each variant, I analyzed the information in Excel.  

**Results and Discussion**

*Sickle Cell Disease* 
I found that 859 samples out of 2504 carried the sickle cell variant, and they belonged only to American and African populations. Thus, I further analyzed only those two populations, and determined that of those 859 carriers, 96.35% were of the African superpopulation and 3.65% were of the American superpopulation.  

*Beta Thalassemia*
I found that only one sample in the GRCh38 data contained the variant for beta thalassemia. This individual belonged to the Peruvian population. Since there was only one individual, I decided not to create a graph for this disease.  

*Hereditary Hemochromatosis*
For the first variant, I determined that 61 samples carried the variant. Of these, 68.85% were of European descent, 22.95% were of American descent, 4.92% were of African descent, and 3.28% were of South Asian descent. Notably, each of the five European populations had carriers of the variant.  
336 samples were carriers of the milder second variant. 46.13% were of European descent, 20.54% were of South Asian descent, 16.96% were of American descent, 8.63% were of African descent, and 7.74% were of East Asian descent. Once again, each of the five European populations had carriers of this variant. Another notable finding was that 9 individuals of Peruvian descent carried the variant as well.  

**Conclusion and Significance**
Overall, sickle cell disease was most common in samples of African descent and did not have any carriers in the populations of interest: European or American, specifically from regions close to Ecuador. Beta thalassemia was shown to be a rare disease in this test of 2504 samples. However, it was present in an individual from Peru, which is geographically close to where I volunteered in Ecuador. On a similar note, hereditary hemochromatosis was most common in European populations, which notably contains samples from the Iberian population in Spain.  
This study is significant to the Biometals CURE for three key principles: heme regulation and iron uptake, treatments to target specific populations, and a better understanding of global populations. Anemia affects around 1 in 4 people in the world (GBD 2021 Anemia Collaborators, 2021). Research on heme regulation can help determine new treatments. Findings from this project—and future research on heme regulation—can aid in designing treatments tailored to target specific populations at greater risk for specific hereditary diseases. And, overall, as migration and globalization shift global demographics, it is important to understand how to address the diverse needs of different populations. Thus, the global significance of this study with regards to the Biometals CURE project is that the understanding the transport and regulation of heme, like that conducted within the Biometals CURE, will be beneficial for future research for treatments for these hereditary diseases.  

**Citations**

Centers for Disease Control and Prevention. (n.d.). About hereditary hemochromatosis. Centers for Disease Control and Prevention. https://www.cdc.gov/hereditary-hemochromatosis/about/index.html#:~:text=Hereditary%20hemochromatosis%20is%20most%20commonly,for%20developing%20high%20iron%20levels 

Gardner, W., Kassebaum, N., & McHugh, T. (2023, September 8). Anemia afflicts nearly 1 in 4 people worldwide, but there are practical strategies for reducing it. Institute for Health Metrics and Evaluation. https://www.healthdata.org/news-events/insights-blog/commentary/anemia-afflicts-nearly-1-4-people-worldwide-there-are 

Gardner, W. M., et al. (2021) Prevalence, years lived with disability, and trends in anaemia burden by severity and cause, 1990–2021: findings from the Global Burden of Disease Study 2021. The Lancet Haematology 10(9), e713 – e734. https://www.thelancet.com/journals/lanhae/article/PIIS2352-3026(23)00160-6/fulltext  

IGSR: The International Genome Sample Resource. 1000 Genomes | A Deep Catalog of Human Genetic Variation. (n.d.). https://www.internationalgenome.org/ 

Langer, A. L. (2000, September 28; Updated 2024, February 8). Beta-Thalassemia. In: Adam MP, Feldman J, Mirzaa GM, et al., editors. GeneReviews® [Internet]. Seattle (WA): University of Washington, Seattle; 1993-2024. Available from: https://www.ncbi.nlm.nih.gov/books/NBK1426/  

Lithi, U. J., Laird, D. W., Ghassemifar, R., Wilton, S. D., & Moheimani, N. R. (2023, December 13). Microalgae as a source of bioavailable heme. Science Direct. https://www.sciencedirect.com/science/article/pii/S221192642300396X 

National Center for Biotechnology Information (US). (1998, January 1). Anemia, sickle cell. Genes and Disease [Internet]. https://www.ncbi.nlm.nih.gov/books/NBK22238/#:~:text=SCA%20is%20an%20autosomal%20recessive,HBB)%20found%20on%20chromosome%2011p15 

NIH. (n.d.). What is sickle cell disease? National Heart Lung and Blood Institute. https://www.nhlbi.nih.gov/health/sickle-cell-disease 

RS1799945. SNPedia. (n.d.). https://www.snpedia.com/index.php/Rs1799945 

RS1800562. SNPedia. (n.d.). https://www.snpedia.com/index.php/Rs1800562 
