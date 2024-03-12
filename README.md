#run first mysql dockerfile
#docker docker build -t mysql-8.0-ubuntu .
#docker run -d --name mysql-container -p 3306:3306 mysql-8.0-ubuntu
#docker inspect container id (to check mysql container id on this command)
#mysql -h container ip -u root -p 12345 (we can go to the inside the mysql on use this command ) and 
(create thise databases copy past only this database tables)

mariadb 
create database studentapp;
use studentapp;
CREATE TABLE if not exists students(student_id INT NOT NULL AUTO_INCREMENT,
	student_name VARCHAR(100) NOT NULL,
    student_addr VARCHAR(100) NOT NULL,
	student_age VARCHAR(3) NOT NULL,
	student_qual VARCHAR(20) NOT NULL,
	student_percent VARCHAR(10) NOT NULL,
	student_year_passed VARCHAR(10) NOT NULL,
	PRIMARY KEY (student_id)
);



Then build backend dockerfile 
#docker build  -t ajju90/backend-file .
#docker run -d -p 8080:8080 ajju90/backend-file
Then changes context.xml file after run dockerfile context.xml past inside the mysql container ip address

Then build frontend dockerfile 
#docker build  -t ajju90/frontend-file .
#docker run -d -p 80:80 ajju90/frontend-file
you can go to index.html file after build the dockerfile and copy backend ip or URL in index.html file this file only readirect the page 
