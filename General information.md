# XLII-Congreso-SEG

Genome annotation improvement by analysing the gene KaKs ratio: A practical case with the genome of Acinetobacter baumannii

The current availability of complete genome sequences has allowed numerous comparative studies to be carried out to better understand the genome of a species. 
These studies are highly dependent on the quality of the used genome assembly, so sequence errors cause poor gene prediction (1). For this reason, new tools 
and methods have emerged to search for new coding regions and thus be able to complete the genome annotation. An example of this is AnaABlast, developed by our
group, an algorithm that discovers small and complex hidden coding sequences (2). We have already shown that the Nonsynonymous / Synonymous Substitution ratio 
(KaKs ratio) could effectively measure evolutionary pressure in other bacteria such as Helicobacter pylori (3). In this work, we propose using AnABlast and the
KaKs ratio to detect regions poorly annotated by current gene finders and discover new possible protein-coding regions. For this study, we use Acinetobacter baumannii, 
an opportunistic bacterium that causes nosocomial infections with high mortality and morbidity (4), because it presents many sequenced strains allowing large-scale
evolutionary analysis. We have carried out a proof of concept with the ATCC 17978 strain, used as a reference of this species, to validate this approach. It presents two 
genome versions sequenced with different NGS tools, the most current version being the most reliable. We performed a comparative analysis between both versions, and
we identified more than 200 genes that showed a wrong annotation in the first genome version of the ATCC 17978 strain. After the estimation of modifications, the 
evolutionary selection for each gene has been calculated using almost 2200 strains. We found that the KaKs ratio usually improved when the most current version gene 
is used as a reference. Furthermore, we discovered some regions which could be new coding genes using our gene predictor. It is a preliminary result, so we must implement
an even more detailed comparative analysis. All these preliminary results propose that this type of analysis could be helpful to validate and correct genetic predictions.

![imagen](https://user-images.githubusercontent.com/84905997/119867469-368bfc80-bf1e-11eb-92ba-ce301775c401.png)


Figure 1. We have already shown that the Nonsynonymous/Synonymous Substitution ratio (KaKs ratio) could effectively measure evolutionary pressure in other bacteria 
such as Helicobacter pylori. Distribution of the Ka/Ks ratio in all the protein-coding genes from the pangenome, where different groups are highlighted (different colors) 
and genes that encode for uncharacterized proteins (asterisks). Black dots represent the median of the distribution

![imagen](https://user-images.githubusercontent.com/84905997/119866979-ad74c580-bf1d-11eb-815a-3f47c5fa2f3d.png)


Figure 2. Proof of concept. A different annotation is observed when comparing the region 40211-47135 in both versions of the ATCC 17978 strain. 
The previous version has two different genes, whereas the new version has only one. The evolutionary comparison with 2200 strains indicates a better 
result when the most current version of the region is used as a reference since the KaKs ratio is lower. The sequence-level comparison shows changes 
that cause a frameshift in the previous version. (a) AnABlast profile highlighting protein-coding regions in the annotated czA gene in the ATCC 17978 
strain genome. (b) Official annotation of region 40211-47135 in both versions of the ATCC 17978 strain genome and KaKs ratio values. (c) Local alignment 
of the C-terminal region between the czA_previous_1 and cza_new gene. We used different colours according to the degree of similarity at the amino acid. 

![imagen](https://user-images.githubusercontent.com/84905997/119867316-0ba1a880-bf1e-11eb-82fc-a8927c0adcd9.png)

Figure 3. Estimation of evolutionary selection in differentially annotated genes. The changes in the KaKs ratio, depending on the version of the gene used as a reference, 
are represented with lines of a different colour (green bars when the ratio improves and red bars when the ratio does not improve). The KaKs ratio improved mostly when the 
most current version gene is used as a reference. The dashed black line represents the kaks ratio of 1.

1.	Meader S, Hillier LW, Locke D, Ponting CP, Lunter G. Genome assembly quality: assessment and improvement using the neutral indel model. Genome Res. 2010 May;20(5):675–84. https://doi.org/10.1101/gr.096966.109.
2.	Jimenez J, Duncan CD, Gallardo M, Mata J, Perez-Pulido AJ. AnABlast: a new in silico strategy for the genome-wide search of novel genes and fossil regions. DNA Res. 2015 Dec;22(6):439-49. doi: 10.1093/dnares/dsv025. Epub 2015 Oct 21. PMID: 26494834; PMCID: PMC4675712.
3.	Rubio A, Pérez-Pulido AJ. Protein-Coding Genes of Helicobacter pylori Predominantly Present Purifying Selection though Many Membrane Proteins Suffer from Selection Pressure: A Proposal to Analyze Bacterial Pangenomes. Genes (Basel). 2021 Mar 6;12(3):377. doi: 10.3390/genes12030377. PMID: 33800844; PMCID: PMC7998743.
4.	Antunes LC, Visca P, Towner KJ. Acinetobacter baumannii: evolution of a global pathogen. Pathog Dis. 2014 Aug;71(3):292-301. doi: 10.1111/2049-632X.12125. Epub 2014 Jan 27. PMID: 24376225.
