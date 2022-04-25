# DBAnalytics_ver02

Code Runs Tests on Database (DB) Appending speeds for various DB and Binary Blob Sizes and types.

To RUN: 
Open project on Eclipse.
Run in order InitializeDB > PopulateDB > DataAnlysis. Each process will print out a message indicating completion (ex: "Database Initialized", Database Populated"). I have automated the process so that 100 files of each of the 18 types of DBs (varying row lengths, blob types, and blob sizes) are initialized, populated and analyzed. This process takes some hours to complete. For a quicker test of the code check out dolphin-acoustics-vip/DBAnalytics_ver01.

Caution: Please do not run PopulateDB twice. You must first initialize the database through InitializeDB then repopulate it through PopulatedDB. Not doing so will produce an unclean database which will obscure data analysis.

Note: You will find that some databases (large ones ex: 10,000 records with 10 kByte Blobs) take a few minutes (~3 min) to populate, but the message indicates that it took less (ex: 00:01:20.875). The total Write Time (WT) is accurate, but the program goes back to update the table with calculations of specific write times, which results in twice the time of computing.
