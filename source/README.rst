run_pbjelly - a faster pbjelly
================================================================================


run_pbjelly is a toolkit to do the gapcloser with PacBio or ONT long reads. Basically, it is the same as the published PBJelly. The main difference between them is that run_pbjelly firstly filtered out reads that are determined to have little relationship with the gap region by MECAT. It has been reported that MECAT is 10 more times faster than Blasr which is employed by the PBJelly.

Another bright spot in our pipeline is that you can just finish all the tasks by running a single job whereas you have to manually deliver the task each time and you also need to check that each task has been completed with the original PBJelly pipeline.

