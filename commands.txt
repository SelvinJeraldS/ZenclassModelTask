create database ZenclassModel;
use ZenClassModel;
create table Student(student_id int primary key,student_name varchar(30),stu_qualification varchar(30) ,mentor_id int,course_id int, foreign key(course_id) references courses(course_id),foreign key(mentor_id) references mentor(mentor_id));
create table batch(batch_id int primary Key,batch_name varchar(30)); 
create table task ( task_id int primary key ,student_id int ,foreign key (student_id) references Student(student_id), batch_id int,foreign key(batch_id) references batch(batch_id));
create table mentor(mentor_id int primary key,mentor_name varchar(30));
create table courses(course_id int primary key ,Course_name varchar(30)); 

drop database ZenClassModel;
drop table Student;
desc Student;
