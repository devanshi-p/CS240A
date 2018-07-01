We have developed and tested our code in IBM DB2 Express Edition on Windows machine.

The submission folder contains separate directories for KNN and NB classifiers. The data for each classifier has been included inside the folder but the absolute path of the dataset needs to be updated in the load sql script file. The submission folder also contains a python utils file that was used to generate facts for Deal.

The test accuracy is stored in the table named "Combined_results". This table can be viewed to get the accuracy of the classifier.


+++++++++++++++++++++++++++ Naive Bayes ++++++++++++++++++++++++++++

Use the following command to first create a database and then execute the scripts:
CREATE DATABASE NB1

Order of execution of scripts
--------------------------------------------------------------------
1. load_banking.sql or load_mushroom.sql
2. verticalize.sql
3. attnumeric.sql
4. partition.sql
5. nb.sql
6. nbtest.sql

For scripts 2,4,5 use following command:
db2 -td~ -vf PATH\NB\nb.sql

For scripts 1,3,6 use following command:
db2 -tvmf PATH\NB\nbtest.sql


++++++++++++++++++++++++++++++ KNN ++++++++++++++++++++++++++++++++

Use the following command to first create a database and then execute the scripts:
CREATE DATABASE KNN

Order of execution of scripts
-------------------------------------------------------------------
1. load.sql
2. verticalize.sql
3. knn.sql

For scripts 2,3 use following command:
db2 -td~ -vf PATH\KNN\db2\knn.sql

For scripts 1 use following command:
db2 -tvmf PATH\KNN\db2\load.sql

