CREATE TABLE Employee (
e_id INTEGER PRIMARY KEY,
e_name TEXT NOT NULL,
dep_id INTEGER NOT NULL,
rank INTEGER NOT NULL,
 salary FLOAT NOT NULL
);
insert into Employee values (1001, 'Sara Jalal', 
'23', '1'
, 
'200000');
insert into Employee values (1002, 'Srijan
Nazia', '24', '2'
, 
'150000');
insert into Employee values (1003, 'Jack Halter', 
'28', '4'
, 
'70000');
insert into Employee values (1004, 'Tom 
Cruise', '89', '3'
, 
'85000');
insert into Employee values (1005, 'Ranbir 
Sing', '76', '5'
, 
'65000');
CREATE TABLE Department (
 
e_id INTEGER PRIMARY KEY,
dep_id INTEGER NOT NULL,
 dep_name TEXT NOT NULL,
 FOREIGN KEY (e_id)
 REFERENCES Employee (e_id) 
);
insert into Department values (1001, 23, 
'Executive Office');
insert into Department values (1002, 24, 
'Accounting');
insert into Department values (1003, 28, 
'Finance');
insert into Department values (1004, 89, 'HR');
insert into Department values (1005, 76, 'Sales');
CREATE TABLE Positions (
 
e_id INTEGER PRIMARY KEY,
rank INTEGER NOT NULL,
p_title TEXT NOT NULL,
 FOREIGN KEY (e_id)
 REFERENCES Employee (e_id) 
);
insert into Positions values (1001, 1, 'CEO');
insert into Positions values (1002, 2, 'CFO');
insert into Positions values (1004, 3, 
'Dep_Head');
insert into Positions values (1003, 4, 'Manager');
insert into Positions values (1005, 5, 
'Supervisor');
