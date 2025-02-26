jMetrik
=======


jMetrik is a free and open source computer program for psychometric analysis. It is a pure Java application that features a user-friendly interface, integrated database, and a variety of statistical procedures and charts. The interface is intuitive and easy to learn. It also scales to the experience of the user. New users can quickly learn to implement psychometric procedures though point-and-click menus. Experienced users can take advantage of the jMetrik command structure and write command files for executing an analysis.

jMetrik’s embedded database increases productivity by providing a common data format for all of its methods. There is no need to reformat or reshape data for each procedure. The database is the primary mechanism for data management. There is virtually no limit to the sample size or number of tables that can be stored in the database. Users are only limited by the amount of storage on their computer. After importing data into jMetrik, users can create subsets of data by selecting examinees or variables. Users can also create new tables by saving the results of an analysis in the database for further processing.



The compiled jMetrik application can be downloaded from <a href="http://www.ItemAnalysis.com">http://www.ItemAnalysis.com</a>.

jMetrik involves a variety of dependencies including Apache Derby, Apache Commons Math, jFreeChart, and the psychometrics library.

Building (Updated: 2022-11-03)
========  
Here are the steps for how to build jMetrik 1.4 successfully.  

First you need to install Maven & JDK 8:  
[https://maven.apache.org/install.html](https://maven.apache.org/install.html)  
[https://bell-sw.com/pages/downloads/#downloads](https://bell-sw.com/pages/downloads/#downloads)

Open your terminal, build a directory then cd into it, enter the commands below:

git clone https://github.com/chenshinfeng/jmetrik.git  
git clone https://github.com/chenshinfeng/psychometrics.git

cd psychometrics  
git checkout 58216c4  
mvn clean install -Dfile.encoding=UTF-8 -Dproject.build.sourceEncoding=UTF-8

cd ../jmetrik  
git checkout 3b20326  
mvn clean package -Dfile.encoding=UTF-8 -Dproject.build.sourceEncoding=UTF-8

Run:  
java -jar target/jmetrik-4.1.1-jar-with-dependencies.jar
