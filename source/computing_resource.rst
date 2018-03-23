Computing Resource
================================================================================

Mecat
--------------------------------------------------------------------------------

We suggest 5Gb memory and 16 cpu for mecat alignment.

PBJelly
--------------------------------------------------------------------------------

The size of memory depends on the file size of the fastq. Usually 15Gb fastq input requires 20Gb for blasr alignment.
Since run_pbjelly have filtered most of reads, ~80%, we recommend 2Gb memory and 20 cpu for blasr alignment and 16 cpu for the local assembly in PBJelly.

You can easily change these settings in the config.cfg file.

Storage
--------------------------------------------------------------------------------

For a genome ~600Mb size with 100x PacBio, the storage for each folder is:

.. csv-table::
   :file: tables/storage.tsv
   :delim: tab
   :header-rows: 1
   :widths: 15, 10, 75

To save you storage, you can nohup the shell 'nohup_rm.sh' after you finished runpbjelly.

