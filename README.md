# Graph-Data-Mining-for-Fraud-Detection
__Objectives__  <br> <br> 
● To identify or detect suspicious fraud rings and events using graph visualization and help prevent future frauds <br>
● To verify customer identities and identify potential fraud profiles as well as profiles at risk of falling for fraudulent schemes <br>
● To learn, use and implement graph data science technology of Neo4j <br>
● To use __Neo4j GDS ( Graph Data Science )__ library to detect and label two types of fraudsters - First party fraudsters and Money Mules <br>
● To use graph mining technology and techniques for achieving fraud detection on a mobile transactions data <br> 

__Scope__ <br> <br>
To reach out goal of 100% accuracy in fraud detection, we did end up creating a system that can, with enough time and data, get very close to that goal. As with any such project, there is some room for improvement here.The very nature of this project allows for multiple algorithms to be integrated together as modules and their results can be combined to increase the accuracy of the final result.This model can further be improved with the addition of more algorithms into it. <br>
However, the output of these algorithms needs to be in the same format as the others. Once that condition is satisfied, the modules are easy to add as done in the code. This provides a great degree of modularity and versatility to the project. <br><br>


## Implementation 👨‍🎓
Synthetic identity fraud and first party fraud can be identified by performing entity link analysis
to detect identities linked to other identities via shared PII. There are three types of __Personally
Identifiable Information (PII)__ in the dataset - SSN, Email and Phone Number.<br> 

__Steps for Finding First-Party Fraud:__
1. Identify clients that share identifiers and create a new relationship between clients that share identifiers
2. Identify clusters of clients sharing PII using a community detection algorithm (Weakly Connected Components)
3. Find similar clients within the clusters using pairwise similarity algorithms (Node Similarity)
4. Calculate and assign fraud score to clients using centrality algorithms (Degree Centrality)
5. Use computed fraud scores to label clients as potential First-Party Fraudsters

__Steps for Finding Second-Party Fraud:__
1. Use WCC (community detection) to identify networks of clients who are connected to first party fraudsters
2. Use PageRank (centrality) to score clients based on their influence in terms of the amount of money transferred to/from fraudsters
3. Assign risk score (secondPartyFraudScore) to these clients
4. Find 2nd - Party Fraudsters using the risk score.

## Neo4j 💹
Neo4j is the world's leading open source Graph Database which is developed using Java technology. It is highly scalable and schema free (NoSQL). Notable features  Neo4j include some of the following mentioned ones −

__1. Data model (flexible schema) −__ Neo4j follows a data model named native property graph model. Here, the graph contains nodes (entities) and these nodes are connected with each other (depicted by relationships). Nodes and relationships store data in key-value pairs known as properties. There is no need to follow a fixed schema. You can add or remove properties as per requirement. It also provides schema constraints.

__2. ACID properties -__ Neo4j supports full ACID (Atomicity, Consistency, Isolation, and Durability) rules.

__3. Scalability and reliability −__ You can scale the database by increasing the number of reads/writes, and the volume without affecting the query processing speed and data integrity. Neo4j also provides support for replication for data safety and reliability.

__4. Cypher Query Language −__ Neo4j provides a powerful declarative query language known as Cypher. It uses ASCII-art for depicting graphs. Cypher is easy to learn and can be used to create and retrieve relations between data without using complex queries like Joins.
