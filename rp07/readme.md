RNA-Puzzle 07
-----------------------------------------------------------------------------

This is an intertwined dimer formed by an exchange of substrate helices. Since not all groups provided models of dimers, I (@mmagnus) focused on getting at least the chain A in order to be able to compare models to the solution. It might not be what you exactly want dear user. The models only with chain A inside are stored in `models_only_with_chain_A` with calculated rmsds and infs ([1]).

Solution sequence vs target sequence:

```
> 7_0_soluton_4r4v_rpr A:1-185
GCGCUGUGUCGCAAUCUGCGAAGGGCGUCGUCGGCCCAAGCGGUAGUAAGCAGGGAACUCACCUCCAAUGAAACACAUUGUCGUAGCAGUUGACUACUGUUAUGUGAUUGGUAGAGGCUAAGUGACGGUAUUGGCGUAAGCCAAUACCGCAGCACAGCACAAGCCCGCUUGCGAGAUUACAGCGC

> 7_Adamiak_1_rpr A:1-185
GCGCUGUGUCGCAAUCUGCGAAGGGCGUCGUCGGCCCAAGCGGUAGUAAGCAGGGAACUCACCUCCAAUGAAACACAUUGUCGUAGCAGUUGACUACUGUUAUGUGAUUGGUAGAGGCUAAGUGACGGUAUUGGCGUAAGCCAAUACCGCAGCACAGCACAAGCCCGCUUGCGAGAUUACAGCGC
```

Manual manipulations:

- Ding.. long list of atoms at the beggning

Problem with `7_Das_7_rpr.pdb`

```
HEADER Generated with rna-pdb-tools
HEADER ver v0.99-14-gca9e840-dirty 
HEADER https://github.com/mmagnus/rna-pdb-tools 
HEADER Thu May 18 18:48:13 2017
REMARK 000 Missing atoms:
REMARK 000  + P A <Residue A het=  resseq=156 icode= > residue # 156
REMARK 000  + OP1 A <Residue A het=  resseq=156 icode= > residue # 156
REMARK 000  + OP2 A <Residue A het=  resseq=156 icode= > residue # 156
REMARK 000  + O5' A <Residue A het=  resseq=156 icode= > residue # 156
```

Rmsd of the A chain:

    rna_calc_rmsd.py -t 7_0_soluton_4r4v_rpr.pdb --target_selection 'A:1-185' --model_selection 'A:1-185' *.pdb
    rmsd_calc_rmsd_to_target
    --------------------------------------------------------------------------------
    method: all-atom-built-in
    # of models: 52
    7_0_soluton_4r4v_rpr.pdb 0.0 3956
    7_Adamiak_1_rpr.pdb 29.04 3956
    7_Adamiak_2_rpr.pdb 28.83 3956
    7_Adamiak_3_rpr.pdb 30.74 3956
    7_Adamiak_4_rpr.pdb 30.01 3956
    7_Adamiak_5_rpr.pdb 28.39 3956
    7_Bujnicki_1_rpr.pdb 42.52 3956
    7_Bujnicki_2_rpr.pdb 60.63 3956
    7_Bujnicki_3_rpr.pdb 26.14 3956
    7_Bujnicki_4_rpr.pdb 24.89 3956
    7_Bujnicki_5_rpr.pdb 24.89 3956
    7_Bujnicki_6_rpr.pdb 26.15 3956
    7_Bujnicki_7_rpr.pdb 26.93 3956
    7_Chen_1_rpr.pdb 28.28 3956
    7_Chen_2_rpr.pdb 34.36 3956
    7_Chen_3_rpr.pdb 29.75 3956
    7_Chen_4_rpr.pdb 27.75 3956
    7_Chen_5_rpr.pdb 23.23 3956
    7_Chen_6_rpr.pdb 29.07 3956
    7_Chen_7_rpr.pdb 29.12 3956
    7_Chen_8_rpr.pdb 29.93 3956
    7_Chen_9_rpr.pdb 33.37 3956
    7_Chen_10_rpr.pdb 31.55 3956
    7_Das_1_rpr.pdb 20.58 3956
    7_Das_2_rpr.pdb 23.56 3956
    7_Das_3_rpr.pdb 24.57 3956
    7_Das_4_rpr.pdb 25.39 3956
    7_Das_5_rpr.pdb 24.6 3956
    7_Das_6_rpr.pdb 25.16 3956
    7_Das_8_rpr.pdb 26.8 3956
    7_Ding_1_rpr.pdb 29.27 3956
    7_Ding_2_rpr.pdb 32.76 3956
    7_Ding_3_rpr.pdb 31.81 3956
    7_Ding_4_rpr.pdb 31.95 3956
    7_Ding_5_rpr.pdb 29.79 3956
    7_Ding_6_rpr.pdb 29.3 3956
    7_Ding_7_rpr.pdb 29.97 3956
    7_Ding_8_rpr.pdb 27.24 3956
    7_Ding_9_rpr.pdb 26.8 3956
    7_Ding_10_rpr.pdb 36.56 3956
    7_Dokholyan_1_rpr.pdb 30.19 3956
    7_Dokholyan_2_rpr.pdb 36.92 3956
    7_Major_1_rpr.pdb 29.01 3956
    7_Major_2_rpr.pdb 28.18 3956
    7_Major_3_rpr.pdb 26.91 3956
    7_Major_4_rpr.pdb 27.64 3956
    7_Major_5_rpr.pdb 28.53 3956
    7_Major_6_rpr.pdb 27.7 3956
    7_Major_7_rpr.pdb 28.53 3956
    7_Major_8_rpr.pdb 27.41 3956
    7_Major_9_rpr.pdb 27.37 3956
    7_Major_10_rpr.pdb 31.61 3956
    # of atoms used: 3956
    csv was created!  rmsds.csv

-------------------------------------------------------------------------------

[1] 

	rna_calc_rmsd.py -t 7_0_soluton_4r4v_rpr_only_A.pdb *.pdb
	rna_calc_inf.py -t 7_0_soluton_4r4v_rpr_only_A.pdb *.pdb
