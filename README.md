# lokaritgerd

echo "# lokaritgerd" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin git@github.com:svafar/lokaritgerd.git
git push -u origin main

Abstract
Diagnosis of a thoracic aortic aneurysm (TAA) is challenging because it is often asymptomatic. While TAA is not intrinsically lethal, enlarged arteries will often lead to an aortic rupture which carries a 90% mortality rate. Because detection is very coincidental, the condition will often remain latent until revealed by a devastating outcome. Although TAAs often correlate with Marfan and Ehler-Danlos syndrome, specific mutations are linked with familial recurrence and shed light on a hereditary aspect of the condition. One such is a mismatch mutation on the linker domain of the SMAD3 of the TGFβ signaling pathway. This mutation changes amino acid 226 from tyrosine to serine, possibly causing the linker domain to gain a new phosphorylation site at that location. This research aims to find the molecular and cellular biology behind the disease manifestation of the SMAD3 mutation that could shed light on the condition. It includes experiments involving protein-protein interactions, nuclear transfections conducted on HEK line cells and endothelial cells, and a 3D structure analysis of the SMAD3 mutation protein.

1	Background

1.1	Blood vessel structure and angiogenesis
The first functional organ to form in an embryo is the heart. It begins with precursor cells, which migrate and specify into fixed cell types as the heart develops. The progenitor cells that formulate the heart originate from epiblast cells residing along either side of the primitive streak of the embryo. These two strips of cells migrate toward each other through the primitive streak forming the cardiogenic mesoderm where the heart tube takes shape. The cardiogenic mesoderm splits into two regions: the first and second heart fields. The two cardiac tubes come together, fusing into one over a small distance where they run parallel. Here is when the heart starts taking shape, and the cells differentiate into the following specializations: cardiomyocytes that make up the heart musculature; the interior layer of the endocardium; the epicardium of which the blood vessels that supply the heart stem; the endocardial cushions of the valves; and the pacemaker cells and Purkinje fibers that regulate the heartbeat. (Gilbert Barresi Michael J. F., 2018) 
 
Figure 1: Development of the heart and cell lineages (Embryology | Radiology Key, n.d.)
The heart does not begin to pump blood until there is a functional vasculature to circulate the blood flow. Blood vessels of the circulatory system develop independently from the heart and link up with it in their development. Blood vessels form via two differing processes: vasculogenesis and angiogenesis. In vasculogenesis, new blood vessels form independently from the lateral plate mesoderm. Ensuing the formation of a vascular network by vasculogenesis, it gets further remodeled into a network of veins and arteries via angiogenesis. The vascular endothelial growth factor VEGF-A, often secreted by a newly forming organ needing increased blood supply, will induce a growth cone to spout out from the vasculature. When vascular endothelial cells get signaled by VEGF-A, they turn into so-called tip cells that respond by migrating towards the increasing VEGF-A gradient. These migrating tip cells express the Notch ligand D114, which blocks adjacent endothelial cells from responding to VEGF-A, so each growth cone has only one tip cell. Those surrounding cells become the stalk cells that do not migrate but follow the tip cell by growing and dividing in its wake (Gilbert Barresi Michael J. F., 2018). Angiopoietin signaling recruits pericytes and smooth muscle cells to cover the endothelial cells to solidify and stabilize these newly formed blood vessels (Valdimarsdottir, 2004). 
 
Figure 2: Angiogenetic sprouting via VEGF stimulation (Benazzi et al., 2014)
Though the role of TGFβ in vascular development is not entirely understood, evidence shows it inhibits angiogenesis. TGFβ-signaling halts EC migration and reduces proliferation. TGFβ also signals mesenchymal cells towards specifying as either SMCs or Pericytes, solidifying the structure of formed blood vessels. However, other findings show TGFβ to have a stimulating effect on angiogenesis, and there are indications that the different results are controlled in part by activation thresholds. (Valdimarsdottir, 2004)

1.2	The TGFβ intracellular pathway
Thirty-three proteins make up the TGFβ superfamily in humans, divided into the TGFβ/activin subfamily and the bone morphogenic protein (BMP) subfamily. They regulate various biological functions in both embryonic development and the immune regulation and tissue repair of the adult body. Among the developmental processes that TGFβ signaling regulates are cellular specification, proliferation, ECM production, and apoptosis. The proteins primarily work through paracrine and juxtracrine signaling and sometimes autocrine. They act as ligands that bind to a set of TGFβ-receptors (TGFβRI and TGFβRII) on the cell surface (Alberts, 2014). There are seven types of TGFβRI receptors, also known as activin receptor-like kinases (ALKs), and five types of TGFβRII. Despite the numerous possibilities of TGFβ-receptor and TGFβ ligand combinations, there appear to be only two intracellular pathways downstream from this host of ligands and receptors (ten Dijke & Arthur, 2007). Both these pathways cause the phosphorylation of receptor-activated SMADs (R-SMADs). TGFβ/actin ligands are upstream signals for the phosphorylation of R-SMADs 2 and 3, and BMP ligands are upstream signals for R-SMADs 1, 5, and 8. The ligand first binds to the type II receptor, which phosphorylates a type I receptor (Kamato et al., 2013). R-SMADs are attached to an anchoring protein called SARA in the cytosol at the SxS region at the C-terminus of the protein. It is then the type I receptor that, as a serine/threonine kinase, phosphorylates and activates an R-SMAD. This phosphorylation of R-SMADs facilitates heteromeric complex formation, which in turn binds to SMAD4 (co-SMAD). SMADs 6 and 7 (I-SMADs) inhibit the activations of R-SMADs by competitively binding to co-SMAD (Kamato et al., 2013). When two R-SMADs and a co-SMAD have made up a trimer, they become a transcription factor (TF) that travels into the nucleus. The genes regulated by the TF and its functionality vary depending on a complex set of factors set by lineage and cell state (Alberts, Johnson). Although TGFβ gene signaling is a complicated process only partially understood, we have ample evidence for it driving transcription of ECM proteins such as fibronectin, collagen, and proteoglycans, and multiple other signaling pathways. (Kamato et al., 2013) 
 
Figure 3: The TGFβ pathway (TGF Beta Signaling Pathway | Thermo Fisher Scientific - IS, n.d.)


1.3	SMAD domain regions and phosphorylation
SMAD2/3 and SMAD4 proteins are similar in structure, and each has three classified structural regions. They are the mad-homology 1 (MH1) domain at the N-terminus, the C-terminus (MH2) domain, and a linker region sitting between them. The nuclear localization signals (NLS) mediating the protein's transport to the nucleus are located MH1 domain. Meanwhile, SMAD4 also has a nuclear export signal (NES) in the NH1 domain. The NH1 domain in SMAD2 is dissimilar from that in SMAD3. It carries two additional sequence structures that adversely affect its adherence to DNA. (Kamato et al., 2013)

The linker region of SMAD3 has four known sites of phosphorylation. They are at thr179, ser204, ser208, and ser213, see figure 1. Phosphorylation at these sites significantly affects protein stability, activity, and the nuclear transportation of SMAD3 as a TF. The phosphorylation performed by TGFβ-receptors on the SxS region at the c-terminus of SMAD2/3 proteins is required to make heterodimers and complexes that bind to co-SMAD. Many other serine/threonine kinases are also known to phosphorylate residues on the linker region. These include downstream signaling kinases and also so-called "cross-talk" with different signaling pathways, which include but are not limited to: mitogen-activated protein kinases (MAPK), the Jun N-terminal kinase (Jnk), the p38 kinase, the PIP3 kinase, tyrosine kinase Scr, cyclin dependant kinases (CDKs) and rho-associated protein kinase (ROCK). Research indicates phosphorylation at these linker sites has a vital role in TGFβ signaling. linker-phosphorylation variants resulting from ranging kinase activity show notable modifications of TGFβ signaling outputs. (Kamato et al., 2013)

 
Figure 4. SMAD3 colored by domains: MH1 yellow, linker region blue, MH2 orange. Source: (Kamato et al., 2013)

1.4	The TGFβ ECM regulation
The bioavailability of TGFβ as a cytokine ligand is heavily regulated by proteins of the extracellular membrane (ECM). This is reflected in research done on cardiovascular disorders such as Marfan syndrome-terminal kinase  (MFS), Loeys-Dietz syndrome (LDS), and pre-eclampsia. 
…..
….
(ten Dijke & Arthur, 2007)

1.5	TAA and TGFβ
The formulation of the proximal aorta originates from cells of both the second heart field and the cardiac neural crest. These two developmental lineages have specific differences integrated regarding their TGFβ signaling capacity. This difference in origin could be why  (Lindsay & Dietz, 2011)

2	Aim of the Project
2.1	Útskýrir rannsóknarefnið
2.2	Setur rannsóknarefnið í samhengi við tíðaranda, aðrar rannsóknir, hugmyndir
2.3	Útskýrir rannsóknaspurningu
2.4	Hvaðan kemur þetta og afhverju aka. Sagan
2.5	Fyrri rannsóknir
2.6	Fyrri umræður og vandamál
2.7	Niðurstaða
3	Methods and materials

3.1	Cell cultures 
Two human cell lines were used in the research within this paper, HUVEC endothelial cells originating from vascular tissue of an umbilical cord and HEK-293T, a cell lineage from an embryonic kidney that shows epithelial morphology. The Cells were kept under sterile conditions and incubated at 37°C with CO2 levels maintained at 5.2%. For the growth medium, the HUVEC cells were grown in PeproGrow with MacroV added in the lab, and the HEK-293T cells were kept in DMEM with 10% fetal bovine serum added medium in the lab. Splitting, seeding, and transfecting of cells were performed within 50-80% confluency.

3.2	Plasmid extraction and Purification
The plasmid was stored in glycerol stock of E.coli at -80°C. LP + Ampicillin medium was created and autoclaved in preparation for the amplification. A pipette tip dipped into the frozen glycerol stock bacteria was transferred into 100 ml of LP + Amp medium, sealed with aluminum foil, placed in an incubator at 37°C, and shaken at 250 rpm overnight. 
Bacteria culture was transferred to 50 ml Falcon tubes, centrifuged at 4°C 14000rpm for 30 min. The supernatant was discarded, and the pellet at the bottom of the Falcon tube was resuspended in RES buffer 8 ml. Next, 8 ml of lysis buffer was added, and the Falcon tube was inverted five times. Next, 12 ml of EQU buffer was applied onto the column rim while wetting the entire filter and allowing it to drain into the Falcon tube to be discarded. Then 8 ml of NEU buffer was added to the suspension and immediately inverted until all blue color was entirely gone. The lysate mixture was then applied to the column. The listed protocol called for a wash of 5 ml EQU buffer. However, the wash buffer was utilized in that step instead. Next, the filter was removed and discarded, and the column was washed with 8 ml of the wash buffer. After draining, a new Falcon tube was placed under a column, and 5 ml of ELU buffer was used to elute. Then 3.5 ml of isopropanol was run through. The mixture was moved to a 15 ml falcon tube and frozen overnight. After thawing mixture was centrifuged at 4°C and 4000 xg rpm for 30 minutes, and the supernatant was discarded. Next, 2 ml of room temperature 70% EtOH was added onto the pellet and centrifuged at room temperature at 4000 xg for 5 minutes. The supernatant was again discarded, and the pellet was allowed to dry out to completion before being resuspended in TE buffer and transferred to 1.5 ml Eppendorf vials. Concentration was measured with nanodrop and more added TE-buffer until all plasmid vials were standardized to be ca. 750 ng/µl (± 50 ng/µl from repeat checking) each.

3.3	Transfection 
Transfection to all cell cultures regarding immunofluorescence and immunoprecipitation was performed via PCDNA3 plasmid vector utilizing FuGENE® HD as the transfection reagent. Transfections were done on six-well plates and in twelve-well chamber slides.
 For the six-well plates, the cells were seeded into the wells with 2 ml of their respective medium and allowed to culture until 50%-80% confluency. Then the following was added together in an Eppendorf vial: 198 µl of Optimem medium; 2 µl of respective DNA via PCDNA3 vector; followed by 6 µl of transfection reagent. This mixture was allowed to sit for 15 min before adding it into a single well. 
For the twelve-well chamber slides, in the case of the Huvec cells, glycerine was added to welles and alowed to make an adherant layer to bottom beroe removing excess after 1 hour befor seeding with 200 µl of medium. However, the HEK-293T were seeded straight onto the slides with 200 µl of medium. The following was added together in an Eppendorf vial: 198 µl of Optimem medium; 2 µl of respective DNA via PCDNA3 vector; followed by 6 µl of transfection reagent. Then, this mixture was allowed to sit for 15 min before 30 µl of this mixture was added into six wells, half of a chamber slide. 
Cells were then incubated at 37°C and 5.2% CO2 overnight, after which all liquid from the cells was removed and discarded, and new medium was added and incubated again overnight. 

3.4	Cell stimulation
For each plasmid, two wells were seeded. Following transfection, one well was given a starvation medium with 10 ng/ml of TGF-β added, while the other received a starvation medium without any TGF-β. The starvation medium for the HEK-293T cell lineage was DMEM with 0.3% FBA. For the HUVEC cells, the starvation medium was 50% PeproGrow + MacroV, and 50% stripped DMEM. Cells were incubated for 1.5 hours in cases for preparation of immunofluorescence on the Huvec cells, and four hours for preparation of immunofluorescence on the HEK-293T cells, and 30 minutes in cases for immunoprecipitation. 

3.5	Harvesting cells for immunoprecipitation
After cell stimulation, the well plate was placed on ice and medium removed, and the wells were washed with 1.5 ml of PBS. Next, 500 ml of Ludwig lysis buffer was added to each well, after which the plate was placed on a shaker for 20 minutes. Next, each well was scraped with a cell scraper. All but 50 µl of lysate in the wells was extracted and placed in 1.5 ml Eppendorf vials which were kept separate in 0.5 ml Eppendorf vial as a sample of total lysate and placed in a -20°C freezer. Into the 1.5 ml vials with 450 ml of the lysate already in was added 25 µl of suspended PrA Sepharose beads, and this mixture was centrifuged at 14000 rpm for 10 minutes, and the float collected into a new vail and 0.5 µl α-Flag antibody added while the vial containing a Sepharose pellet was discarded. The samples were, at this point, placed on a shaker at 4°C and allowed to sit there overnight. Next, 30 µl of suspended PrA sepharose beads are added to the samples, put on a shaker for 30 minutes before centrifuging for 10 minutes at 14000 rpm, and discarded the supernatant. Into each vial with Sepharose pellet, 40 µl of Lamelli buffer is added and heated for 10 minutes at 95°C before being 35 µl loaded into respective wells on a 10% SDS-PAGE gel along with a ladder in a separate well. The total lysate samples were thawed, and 50 µl of Lamelli buffer and a ladder were added to each sample vial and loaded on its own 10% SDS-PAGE gel.

3.6	Harvesting cells for western blot
Proteins were extracted from cells by first removing from incubation and placing six-well plates on ice and washing them with PBS. Next, 300 µl of Ludwig-lysis buffer is placed per well, and incubated for 20 min on a shaker, after which the bottoms of the wells were scraped thoroughly. The lysate was then transferred to Eppendorph vials and samples heated at 95°C for 5-10 minutes.

3.7	SDS-page
First, a running buffer was created from (vantar innihald). Gels of 10% viscosity were used in these experiments. To make the gels 1.5 mm casting glass was selected and cleaned with 70% Ethanol and lined up in clamps. Next, the separating gel was created in a Falcon tube, (innihaldslýsing), this mixture was pipetted into the 1.5 mm space between glasses up to about 2/3 point. 1 ml of MilliQ H2O was added on top to remove bubbles and given approximately 30 min to set. Next, the stacking gel mixture is prepared, (innihaldslýsing). The water layer on top of the separating gel is poured off before pipetting the stacking gel mixture to the top. Then, a 10 well sample comb was placed in the gel before allowing it to set completely. After setting the gels and glass casing are removed from clamps and placed well side towards the inside into a running module which is then placed gel box along with running buffer, making sure the buffer surface extends over the wells on the gel and fills them, and the lid placed making sure that the running module and electrodes on the lid align correctly. The samples are loaded to their respective wells as well as a ladder to an outermost well. The power supply is turned on and set to 95 Volts for approx. 50 min for the proteins to stack, then it is set to 120 Volts and allowed to run until the blue color band almost reaches to the bottom. Then power is shut off and the gel still in the glass casing was removed from the running module. At this point, gels are ready for transfer or can be stored in a 4°C fridge wrapped in a wet paper towel and bagged for transfer later. 

3.8	Transfer
Transfer buffer was made by (innihaldslýsing). The gel is removed from the glass casing, and the stacking part is cut off and discarded. A transfer cassette is laid open and assembled, beginning on the cathode side. First thick sponge with large pores is wetted with transfer buffer and then a thinner and more compact sponge is wetted the same way and placed thereafter. Three sheets of filter paper are wetted with the running buffer and placed in succession and then the gel. Care is taken to orient the gel correctly and mark on which side the ladder is placed. Next, a membrane that has been soaking in methanol for a minute is placed on the gel. Next, the same process as before the gel was placed is performed in reverse order, ending with the thicker looser sponge on top. The cassette is closed and placed in a transfer box, taking care to orient the cassete correctly in accordance with the electrodes on the lid. Transfer buffer is added to the box until it goes over the contents of the cassette and the lid is correctly placed on the box. The bac was placed in a 4°C fridge with the cords protruding out the closed door and connected to a power supply with the settings of 24 mA, and the transfer was run overnight. The next day, the cassette is opened, and the gel is discarded. 

 
Figure 5: Example of blotting sandwich in a transfer cassette. (Politz et al., 2022)

3.9	Blocking and antibody staining
The blocking solution that was used was comprised of 5% bovine serum album (BSA) in Tris buffer saline with 0.1% Tween (TBS-T). Each membrane was placed in a clean case and 7-10 ml of blocking solution is added taking care to keep track of which side is the transfer side. Were placed on a shaker for 50 min at room temperature after which the blocking solution is recollected for future use. After blocking, the primary antibodies (see Table 1) are added to the case with the membrane and can either be left overnight at 4°C or for 3-4 hours at room temperature. After that, the primary antibody solution was recollected, and the membrane was washed three times with TBS-T for 15 min each time. Post washing, the membranes were incubated with the secondary antibody (see Table 2) for 1 hour at room temperature, after which the antibody mixture was recollected, and the membrane is washed three times with TBS-T for 15 min each wash again. After this process, membranes were ready for scanning and imaging using an Odyssey CLX machine.
Table 1: Primary antibodies for blotting
Antibody	Serum species	2° ab species	Company	Catalog #	Dilution
					
					


Table 2: Secondary antibodies for blotting
Species	Serum species	Company	Catalog #	Wavelength	Dilution
α-					
α-					

3.10	Immunofluorescence staining
Immunofluorescence staining was conducted on both Huvec and HEK-293T cell lines. The cells were cultured, transfected, and stimulated in twelve-well chamber slides whereupon they were fixed to the slides. To fix the cells, the medium was removed, and then the chambers were washed with 100 µl of PBS. Then, 100 µl of paraformaldehyde (PFA) was added to each chamber and ad the slide was allowed to incubate for 10 min at room temperature. The PFA was removed and discarded, and each chamber was washed with 100 µl PBS three times successively, with the last wash sitting in each chamber for 5 min. Next, to permeabilize the cells for staining, 0.1% Triton-X in PBS was added to each well and incubated at room temperature for eight minutes. Again, each chamber was washed with 100 µl PBS three times successively, with the last wash sitting in each chamber for 5 min. After removing the PBS, 300µl of 4% goat serum in PBS was added to each well and incubated overnight at room temperature. The next day, Primary antibodies diluted in 4% goat serum in PBS are added (see Table 3 and Figure 2) and allowed to incubate for two hours at room temperature. Next, each chamber is washed with 0.05% Tween in PBS (PBS-T) three times in succession. Next, 100 µl of a dilution of secondary antibodies in 4% goat serum in PBS is added to each well (see Table 4 and Figure 3) and incubated for 2 hours at room temperature or 4°C overnight. Once the secondary antibodies were added care was taken to minimize direct light exposure to the slides by keeping them in closed lid boxes. After incubation chambers were washed three times with PBS-T. Next the chambers were emptied of liquid and the rubber chamber seeperator romoved off the slide and it was ser to dry completely. The mounting media used had DAPI nuclear staining already mixed in it. A small number of mounting media was applid to the surface with the exposed cells and a class cover blaced down gently on the slide before allowing to dry. Once the slides were dry they were ready for imaging which was performed with an Olympus Fv1200 confocal microscope.

Table 3: Primary antibodies for IF
Antibody	Serum species	2° ab species	Company	Catalog #	Dilution
					
					


Table 4: Secondary antibodies for IF
Species	Serum species	Company	Catalog #	Wavelength	Dilution
α-					
α-					




HUVEC	-	+ TGFβ	+BMP9	-	+ TGFβ	+BMP9
Elastin
TSP1	

	

	

	

	

	


FLAG
(not present)	

	

	

	

	

	


	pcDNA3	SMAD3 WT


HUVEC	-	+ TGFβ	+BMP9			
Elastin
TSP1	

	

	

	
GFP
	
2°ab ctrl.
	


FLAG
(not present)	

	

	

	

	

	


	SMAD3 mutant	


HEK-293T	-	+ TGFβ	+BMP9	-	+ TGFβ	+BMP9
ID1
PAI1	

	

	

	

	

	


FLAG	

	

	

	

	

	


	pcDNA3	SMAD3 WT


HEK-293T	-	+ TGFβ	+BMP9			
ID1
PAI1	

	

	

	
GFP
	
2°ab ctrl.
	


FLAG	

	

	

	

	

	


	SMAD3 mutant	

Hvaða aðferðarfræði ertu að fara að nota og afhverju?
4	Results
4.1	Overview explanation

4.2	Immunoprecipitation

	 
~66 kDa	
~42 kDa	

~23 kDa	
Figure 6: Lysate HEK-293T cells FLAG and Actin 07.03.22
 
Figure 7:





	 
~66 kDa	
Actin 42 kDa	
~23 kDa	
Figure 8
 
Figure 9









	 
~66 kDa	
Actin 42 kDa	
~23 kDa	


 









	 
~66 kDa	
Actin 42 kDa	
~23 kDa	



 
4.3	Immunofluorescence staining

4.3.1	Chamberslide images of HEK-293T cells after stimulation

	No stimulation	TGFβ stimulation	BMP9 stimulation
EV	 	 	 
WT	 	 	 
Y226S	 	 	 
Figure 10: Chamber slide images of HEK-293T cells after stimulation
	2°ab ctrl.	GFP	GFP fl.
Cntrl	 	 	 
Figure 11: Chamber slide images of controls  
4.3.2	Confocal images
PAI1	No stimulation	TGFβ stimulation	BMP9 stimulation
EV	 	 	 
WT	 	 	 
Y226S	 	 	 
Figure 12: HEK-293T cells stained with PAI1 primary antibody and mouse secondary antibody
ID1	No stimulation	TGFβ stimulation	BMP9 stimulation
EV	 	 	 
WT	 	 	 
Y226S	 	 	 
Figure 13: HEK-293T cells stained with ID1 primary antibody and rabbit secondary antibody
FLAG	No stimulation	TGFβ stimulation	BMP9 stimulation
EV	 	 	 
WT	 	 	 
Y226S	 	 	 
Figure 14: HEK-293T cells stained with Flag primary antibody and mouse secondary antibody with DAPI nucleus coloring 
Elastin	No stimulation	TGFβ stimulation	BMP9 stimulation
EV	 	 	 
WT	 	 	 
Y226S	 	 	 
Figure 15: HUVEC cells stained with Elastin primary antibody and rabbit secondary antibody
TSP1	No stimulation	TGFβ stimulation	BMP9 stimulation
EV	 	 	 
WT	 	 	 
Y226S	 	 	 
Figure 16: HUVEC cells stained with TSP1 primary antibody and mouse secondary antibody


Alphafold
 
Figure 17: SMAD3 WT brúnt og SMAD3 Y226S mutant ljósblátt borið saman

 
Figure 18: SMAD3 WT
 
Figure 19: SMAD3 Y226S mutant

 
 
4.4	Útskýra hvaða skref eru tekin
4.5	Útskýra hvernig hún er gerð
4.6	Útskýra hvernig það tengist aðferðarfræðinni
4.7	Niðurstaða
5	Discussion
5.1	Eitthvað sem hefði mátt gear betur 
5.2	Önnur aðferðarfræði sem hefði getað gefið aðrar niðurstöður?
5.3	HVersu marktækar eru niðurstöðurnar þínar í samhengi hlutanna?
5.4	Hversu marktækar eru þessar rannsóknaraðferðir?
6	Conclusion
6.1	Hver var niðurstaðan
6.2	Hvað lærðir þú
6.3	Hverjar voru takmarkanirnar og mögulegar framhaldsrannsóknir



References

Alberts, B. (2014). Molecular biology of the cell (6th ed.). CRC Press.
Benazzi, C., Al-Dissi, A., Chau, C. H., Figg, W. D., Sarli, G., Oliveira, J. T. de & Gärtner, F. (2014). Angiogenesis in Spontaneous Tumors and Implications for Comparative Tumor Biology. The Scientific World Journal, 2014, 919570. https://doi.org/10.1155/2014/919570
Embryology | Radiology Key. (n.d.). Retrieved May 4, 2022, from https://radiologykey.com/embryology/#Fig2
Gilbert Barresi Michael J. F., S. F. (2018). Developmental biology.
Kamato, D., Burch, M. L., Piva, T. J., Rezaei, H. B., Rostam, M. A., Xu, S., Zheng, W., Little, P. J. & Osman, N. (2013). Transforming growth factor-β signalling: role and consequences of Smad linker region phosphorylation. Cellular Signalling, 25(10), 2017–2024. https://doi.org/10.1016/J.CELLSIG.2013.06.001
Lindsay, M. E. & Dietz, H. C. (2011). Lessons on the pathogenesis of aneurysm from heritable conditions. Nature, 473(7347), 308–316. https://doi.org/10.1038/NATURE10145
Politz, S., Wpi & Advisor, P. (2022). Nematomucin Antigen Expression Identification using Anti-Peptide Antibodies.
ten Dijke, P. & Arthur, H. M. (2007). Extracellular control of TGFbeta signalling in vascular development and disease. Nature Reviews. Molecular Cell Biology, 8(11), 857–869. https://doi.org/10.1038/NRM2262
TGF Beta Signaling Pathway | Thermo Fisher Scientific - IS. (n.d.). Retrieved May 4, 2022, from https://www.thermofisher.com/is/en/home/life-science/antibodies/antibodies-learning-center/antibodies-resource-library/cell-signaling-pathways/tgf-beta-pathway.html
Valdimarsdottir, G. (2004). Comprehensive Summaries of Uppsala Dissertations from the Faculty of Medicine 1357 TGFß Signal Transduction in Endothelial Cells [Uppsala University]. https://www.diva-portal.org/smash/get/diva2:164704/FULLTEXT01.pdf
 
