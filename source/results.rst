Results
================================================================================

folders
--------------------------------------------------------------------------------

Basically, there are 4 folders, including **0-shells**, **1-data**, **2-results**, **3-reports**, and **4-logs**.
Their introduction is as following tables(same as the table in **Storage** section, 600 genome with 100x data):

.. csv-table::
   :file: tables/storage.tsv
   :delim: tab
   :header-rows: 1
   :widths: 15, 10, 75


Scaffold file
--------------------------------------------------------------------------------

After filling the gaps, run_pbjelly output all the sequences in the file named 'jelly.out.fasta' under the file folder '2-results'.


.. _GapInfo:

Gap informations
--------------------------------------------------------------------------------

Besides, for the detailed process information for each gap, you can refer the file 'gap_fill_status.txt' also under the file folder '2-results'.

.. _Reports:

Reports
--------------------------------------------------------------------------------

We also generated a html report for run_pbjelly, which include contig N50 value, distribution of gap lengths, and et al. And the report files were placed under the file folder '3-reports' (comming soon). A simple statistics were generated under the file folder '3-reports', such as:

.. image:: images/stat.png
