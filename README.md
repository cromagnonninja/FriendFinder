# FriendFinder
Find Mutual Friends using Hadoop MapReduce

### HADOOP ASSIGNMENT 
### MUTUAL FRIENDS FINDER (GROUP 9)
##### Submitted to: Pravin Srivastava Sir, Research Scholar, Systems Lab, IIIT Allahabad
By: Bhanu Bhandari (IEC2016027) and Harshit Srivastava (IEC2016065), Group 9 

The procedure followed for obtaining the output text file which gives mutual friends is as follows: 
1. Used a facebook scraper to obtain data of our own friend list as well as friends of all our friends with some data manipulation afterwards so as to make the data usable for MapReduce operations. 
2. This data was then transferred to hdfs by using hadoop commands. 
3. Created the Hadoop MapReduce “MutualFriend.java” file which takes input as the 2nd-degree extended friendlist with many rows containing friend information and IDs and generates output as the IDs having common names. Later on, this Java file was compiled into a “jar” binary file to be used by Hadoop. 
4. The mapper maps friends of a particular ID (basically generating a key value pair of the friendlist), and the reducer reduces this list into a list of common friends between two people on the basis of their IDs (as observed in the outputs). The reducer gives the output file in the format 
“Friend1, Friend2 <space> MutualFriend1, MutualFriend2, MutualFriend3,..” as obtained in the file output1.txt. 
5. Then, after this process takes place, the output is currently located inside HDFS. This has to be removed from there by using Hadoop commands. 
6. The final output is copied out from HDFS and thus the output has been obtained. 
