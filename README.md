# Uppala-spark-wordcount

## About Me and the Objective of the Project  
I am Saikumar from Hyderabad,India. 
I have completed my undergraduation from Vignan Engineering College, Hyderabad in Electronics Department, 2015.
I have worked in Infosys as Systems Engineer for 17 months as Linux Admnistrator.
The objective of the project is to find the word count in a file using spark.

## Dataset:
It is the data from shakepeare's Measure of Measure book. It is the The Tragedy of Hamlet, Prince of Denmark

http://shakespeare.mit.edu/hamlet/hamlet.2.1.html

## Commands used:
val inputFile = val inputFile = sc.textFile("C:/44517/Uppala-spark-wordcount/plays.txt")  
Commad to load shakespeare.txt data

val counts = inputFile.flatMap(line => line.split(" ")).map(word => (word,1)).reduceByKey(_ + _);  
command to count words with space deliminator

counts.saveAsTextFile("C:/44517/Uppala-spark-wordcount/output")  
Command to save the results in Output.txt

## Result

| Word    | Count|
|---------|------|
| and     | 24   |
| the     | 20   |
| his     | 23   |
| i       | 23   |
| Lord    | 19   |
| my      | 22   |
| of      | 21   |
| polonius| 20   |
| to      | 17   |
| you     | 17   |


By seeing the reults we can say that "and" is the most repeating word in this article than the other words.  
## Screenshot of results graph
![capture](https://user-images.githubusercontent.com/31738776/48322457-45736380-e5ed-11e8-9ccc-fce82956571c.PNG)
