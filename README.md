## SQL-Queries-for-TPC-H
Public Repository containing SQL Queries for the TPC-H Benchmark.<br><br>

### Files containing the SQL query text and their metadata
For a given scenario and scale factor, packs of 1000 queries are generated as `.csv` files ready to be executed with jMeter (for automatically collecting the query completion/success and the query duration) in PostgreSQL, Oracle, or Microsoft SQL Server.<br>
Separated files (`.xlsx`) provide the query's metadata (e.g., number of joins, predicates in WHERE, GROUP BY attributes, etc.) for more granular analyses of query performance (e.g., assessing the association between query completion or query duration and the query parameters in various physical setups).

### Supported SQL dialects
Currently: PostgreSQL, Oracle, and MS-SQL Server (.csv files prepared for jMeter). <br>
In progress: Apache Spark (separate text file for each query).

### Database size (scale factors)
Each query set (in a .csv file) contains 1000 queries for one of the following scale factors: 0.01GB, 1GB, 2GB, 5GB, 10GB, 50GB, 100GB, 200GB, 1000GB, 2000GB 

### Query structure and parameters
For the query structure and the main vocabulary (used for defining the scenarios for query generation), see section [_query_template_and_parameters](https://github.com/marinfotache/SQL-Queries-for-TPC-H/tree/main/_query_template_and_parameters)

### Main scenarios for query generation
Each query set is generated following a specific scenario which controls the query complexity.<br>
For details, see section [_scenarios_for_query_generation](https://github.com/marinfotache/SQL-Queries-for-TPC-H/tree/main/_scenarios_for_query_generation)

### Resources:
  * [TPC-H Benchmark specification:](https://www.tpc.org/TPC_Documents_Current_Versions/pdf/TPC-H_v3.0.1.pdf)
  * [jMeter home page:](https://jmeter.apache.org)

  
### Other papers using the previous and the current versions of the query generator:
* Fotache, M., Munteanu, A., Strîmbei, C., Hrubaru, I. (2023). _Framework for the Assessment of Data Masking Performance Penalties in SQL Database Servers. Case Study: Oracle_, IEEE Access (eISSN: 2169-3536), Vol.11, pp. 18520-18541, [DOI: 10.1109/ACCESS.2023.3247486](https://ieeexplore.ieee.org/document/10049552)
* Fotache, M. Cluci, M. -I. (2021). _Big Data Performance in Private Clouds. Some Initial Findings on Apache Spark Clusters Deployed in OpenStack_, Proc. of the 20th RoEduNet Conference: Networking in Education and Research (RoEduNet), 2021, pp. 1-6, [DOI: 10.1109/RoEduNet54112.2021.9638296](https://ieeexplore.ieee.org/document/9638296)
* Fotache, M., Cluci, M.I.,  Greavu-Șerban, V. (2020). _Low cost big data solutions: The case of Apache Spark on beowulf clusters_, Proc. of the 5th International Conference on Internet of Things, Big Data and Security (IoTBDS 2020), May 2020, ISBN: 978-989758426-8, pp. 327-334, SciTePress, Setubal, Portugal [link](https://www.scitepress.org/Papers/2020/94079/pdf/index.html)
* Fotache, M., Hrubaru, I. (2016). _Performance Analysis of Two Big Data Technologies on a Cloud Distributed Architecture. Results for Non-Aggregate Queries on Medium-Sized Data_, Scientific Annals of Economics and Business, vol. 63 (SI), 2016, pp. 21-50,  [DOI: 10.1515/saeb-2016-0134](http://saeb.feaa.uaic.ro/index.php/saeb/article/view/91/35) 


### Acknowledgement:
Physical resources for deploying the query generator of this repository were provided by the Competitiveness Operational Program Romania, under project SMIS 124759 - RaaS-IS (Research as a Service Iasi).
  
