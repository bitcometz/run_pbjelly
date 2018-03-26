run_pbjelly - a faster pbjelly
================================================================================


run_pbjelly is a toolkit to do the gapcloser with PacBio or ONT long reads. Basically, it is the same as the published PBJelly. The main difference between them is that run_pbjelly firstly filtered out reads that are determined to have little relationship with the gap region by MECAT. It has been reported that MECAT is 10 more times faster than Blasr which is employed by the PBJelly.

Another bright spot in our pipeline is that you can just finish all the tasks by running a single job whereas you have to manually deliver the task each time and you also need to check that each task has been completed with the original PBJelly pipeline. And we also replaced the blasr1.3 with blarsr5.3 in PBJelly.


.. raw:: html 
   
    <font color="red">Performance </font> of run_pbjelly on ~600M genome comparing to the original PBJelly as the tables, 
run_pbjelly achieve **better** results but **~10 times faster** !!! Because in this case, only **~93%** of the reads were first filtered by mecat.

.. _FeatureTable:

.. csv-table::
   :file: tables/performance.tsv
   :delim: tab
   :header-rows: 1
   :widths: 15, 10, 75

Another tested on also ~731M genome with 100x PacBio data based on the same 20 cpu:

.. _FeatureTable:

.. csv-table::
   :file: tables/performance2.tsv
   :delim: tab
   :header-rows: 1
   :widths: 15, 10, 75
 
