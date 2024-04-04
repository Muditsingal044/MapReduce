# MapReduce

Downloads Folder- (copy and paste in URL)

https://drive.google.com/drive/folders/1JGOAnuABVAmLRcw0hdccbx1djcjpMAre?usp=sharing

CMD - 

0.  mkdir mudit@2101331540068

 
1.  mkdir MapReduceTutorial
  
  
   files(SalesCountryDriver,SalesCountryReducer,SalesJan2009,SalesMapper,Manifest.txt) have pasted in (MapReduceTutorial) directory..  with help of folder


.... given in description....



2. sudo chmod -R 777 MapReduceTutorial

3. cd MapReduceTutorial

4. hadoop version 


5. export CLASSPATH="/usr/lib/hadoop-mapreduce/hadoop-mapreduce-client-core-2.6.0-cdh5.12.0.jar:/usr/lib/hadoop-mapreduce/hadoop-mapreduce-client-common-2.6.0-cdh5.12.0.jar:/usr/lib/hadoop/hadoop-common-2.6.0-cdh5.12.0.jar:~/MapReduceTutorial/SalesCountry/:/usr/lib//hadoop/lib/"



6. javac -d . SalesMapper.java SalesCountryReducer.java SalesCountryDriver.java 

7. sudo chmod -R 777 SalesCountry


8. jar cfm ProductSalePerCountry.jar Manifest.txt SalesCountry/*.class

9. hadoop fs -mkdir /inputMapReduce1 

10. hadoop fs -copyFromLocal /home/cloudera/mudit@2101331540068/MapReduceTutorial/SalesJan2009.csv /inputMapReduce1 
    NOTE - (please change the name and rollnumber)

11. hadoop jar /usr/lib/hadoop-mapreduce/hadoop-mapreduce-examples-2.6.0-cdh5.12.0.jar wordcount /inputMapReduce1 /mapreduce_output_sales1

12. hadoop fs -cat /mapreduce_output_sales1/part-r-00000
