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
