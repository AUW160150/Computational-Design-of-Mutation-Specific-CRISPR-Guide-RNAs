# Computational-Design-of-Mutation-Specific-CRISPR-Guide-RNAs
##

CRISPR Guide RNA Candidates for TERT Promoter Mutation Targeting
================================================================

Research Question: Can CRISPR guide RNAs be computationally designed to selectively target TERT promoter regions containing cancer-specific mutations (C228T or C250T) with at least 3-fold higher cutting efficiency compared to normal TERT promoter sequences?

Target Sequences:
- Wild-type: CCGCGCGGACCCCGCCCCGTCCCGACCCCTCCCGGGTCCCCGGCCCAGCCCCCTCCGGGCCCTCCCAGCCCCTCCCCTTCC
- C228T:     CCGCGCGGACCCCGCCCCGTCCCGACCCTTCCCGGGTCCCCGGCCCAGCCCCCTCCGGGCCCTCCCAGCCCCTCCCCTTCC
- C250T:     CCGCGCGGACCCCGCCCCGTCCCGACCCCTCCCGGGTCCCCGGCCCAGCCTCCTCCGGGCCCTCCCAGCCCCTCCCCTTCC

Mutation Sites:
- C228T: Position 29 (C→T) - Creates ETS binding motif
- C250T: Position 51 (C→T) - Creates ETS binding motif

High-Priority Guide RNA Candidates:
===================================

GUIDE 1 - C228T Targeting
Guide RNA: GCCCCGTCCCGACCCCTCCC
PAM: CGG
Position: 14-33 (spans C228T mutation at position 29)
Target: C228T mutation
Priority: HIGH - directly spans C228T site

GUIDE 2 - C228T Targeting  
Guide RNA: CCCCGTCCCGACCCCTCCCG
PAM: GGG
Position: 15-34 (spans C228T mutation at position 29)
Target: C228T mutation
Priority: HIGH - directly spans C228T site

GUIDE 3 - C228T Targeting
Guide RNA: CCGACCCCTCCCGGGTCCCC
PAM: CGG
Position: 22-41 (spans C228T mutation at position 29)
Target: C228T mutation (also near C250T)
Priority: HIGH - spans C228T, may have activity against both

GUIDE 4 - C250T Targeting
Guide RNA: TCCCCGGCCCAGCCCCCTCC
PAM: CGG
Position: 37-56 (spans C250T mutation at position 51)
Target: C250T mutation
Priority: HIGH - directly spans C250T site

GUIDE 5 - C250T Targeting
Guide RNA: CCCCGGCCCAGCCCCCTCCG
PAM: GGG
Position: 38-57 (spans C250T mutation at position 51)
Target: C250T mutation
Priority: HIGH - directly spans C250T site

Computational Analysis Required:
===============================

For EACH guide RNA, test against ALL THREE sequences:
1. Wild-type TERT promoter
2. C228T mutant TERT promoter  
3. C250T mutant TERT promoter

Metrics to Calculate:
- On-target efficiency score (use CRISPRscan or similar)
- Off-target potential (use COSMID or Cas-OFFinder)
- GC content of guide RNA
- Presence of problematic sequences (poly-T, etc.)

Selectivity Calculations:
- C228T selectivity = (C228T cutting score) / (Wild-type cutting score)
- C250T selectivity = (C250T cutting score) / (Wild-type cutting score)

Success Criteria:
- Selectivity ratio ≥ 3.0 for target mutation
- High on-target score for mutant sequence (>0.5)
- Low off-target potential (<3 predicted sites)
- Suitable guide RNA properties (40-80% GC, no poly-T)

Recommended Tools:
=================
1. CHOPCHOP (https://chopchop.cbu.uib.no/)
   - Upload the three FASTA files
   - Design guides for each sequence
   - Compare efficiency scores

2. Benchling CRISPR Design Tool
   - Import sequences
   - Generate guide RNAs
   - Analyze activity predictions

3. CRISPRscan (for activity prediction)
   - Score each guide against each target sequence
   - Calculate selectivity ratios

4. Cas-OFFinder (for off-target analysis)
   - Check genome-wide off-target potential
   - Ensure specificity

Next Steps:
===========
1. Upload the three FASTA files to your chosen CRISPR design tool
2. Generate comprehensive guide RNA designs for each sequence
3. Create a spreadsheet with efficiency scores for each guide on each target
4. Calculate selectivity ratios for each guide
5. Rank guides by selectivity and activity
6. Select top 3-5 candidates for experimental validation
7. Design experiments to test in vitro cutting efficiency
8. Validate selectivity experimentally

Expected Outcome:
================
If successful, you should identify 2-5 guide RNAs that show:
- ≥3-fold selectivity for mutant vs wild-type sequences
- High cutting efficiency on target mutations
- Low off-target potential
- Suitable properties for experimental use

This would support your hypothesis that CRISPR guide RNAs can selectively target cancer-specific TERT promoter mutations.
