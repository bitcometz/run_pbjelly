run_pbjelly - a faster pbjelly
================================================================================


run_pbjelly is a toolkit to do the gapcloser with PacBio or ONT long reads. Basically, it is the same as the published PBJelly. The main difference between them is that run_pbjelly firstly filtered out reads that are determined to have little relationship with the gap region by MECAT. It has been reported that MECAT is 10 more times faster than Blasr which is employed by the PBJelly.

Just as shown in the above figure, we first use MECAT to do the alignment for all the raw reads and after that we can know the most possible locations of genome for those reads. Usually, only ~10% reads are mapped around gap regions(around 2kbp) and it waste a lot of time for PBJelly to do the alignment for the rest of reads with Blasr since those far away gap region reads were not used to do the local assembly and filled the gaps. So, we can speed up the PBJelly by first removing those reads. Besides, we found that the original PBJelly rudely collected reads to do the local assembly and doing this uasually gives poor results. So, with our approach, it will get better contig N50 value.
