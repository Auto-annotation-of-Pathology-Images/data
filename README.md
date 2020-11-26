- vignettes: from Dr. Coley
- vignettes_new: vignettes from FFPE PostRep 001.svs level 1, (11000,16000) on top left, 1028*1028
- vignettes_new_level_0: same as vignettes_new but on level 0, 4112*4112
- normal proximal and distal tubular segments_HE_001: vignettes from MultiStain normal proximal and distal tubular segments/HE_001, 3000*3000
- HE_001_rotated: rotate 90 anti-clock to match the angle of tubules in vignettes_new (updated)
- FFPE PostRep 001: annotate biopsy on top. take out all glom and arteries. full annotation on two selected patches 13600_18000_0 and 20000_14800_0
- FFPE PostRep 002 - 010: annotated slide vignettes

train: 001, 004, 005, 006, 008, 010, all other multistain
validation: 003, 009, HE_001 (tubule_HE_001)
test: 002, 007
* for slide 003-010, tubule/tubules are copied and divided into distal_tubule and proximal_tubule
```
ds          label          
test        arteriole           38
            artery              10
            distal_tubule       10
            glomerulus          57
            glomerulus_gs        3
            medulla              2
            proximal_tubule     10
            tubule              20
            tubules              4
train       arteriole           23
            artery              49
            distal_tubule      126
            glomerulus         157
            glomerulus_gs        6
            proximal_tubule    150
            tubule              47
            tubules             62
validation  arteriole           25
            artery              18
            distal_tubule       81
            glomerulus          81
            glomerulus_gs        4
            proximal_tubule     79
            tubule              20
            tubules             44
```
readme for vignettes_1117
- vignettes: working folder for collage generator
  - combine vignettes_new_level_0, HE_001_rotated, FFPE PostRep 001 and multistain
  - train/val split 0.8/0.2
    - glomerulus: 32/9
    - artery: 18/5
    - proximal_tubule: 125/32
    - distal_tubule: 84/22
  - exclude some incompleted tubules and glom
- patch_annotation:
  - original patch of slide and tubules masks
  - HE_001 from multistain and 11000_16000_0 from FFPE PostRep 001.svs
  - 13600_18000_0 and 20000_14800_0 from FFPE PostRep 001.svs. Full annotation for multiple labels. Attache a labelmap.txt.
- other archived data transfered to data repo
