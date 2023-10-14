# Simulation-of-Regional-Airport
## Goal of The Project
This is to simulate a regional airport database management. This employs normalization, primary keys, foreign keys, and join queries to ensure data consistency. 

### Important to know- I am using mySQL 8.0

## Tables 
1. Aircraft
2. Airport
3. CityState
4. Employee
5. Employee Position
6. Flight
7. Passenger
8. Position

### 1. Aircraft 
This describes the aircraft that the airport uses. The primary key is the ID. It has the following variables
1. ID - int
2. Manufacturer - varchar
3. icaoCode - varchar
4. model - varchar
5. engineClass - enum
6. numEngine - int
7. numSeat - int

### 2.  Airport
This table describes the different airports that the flights go out to or come in from. It has the FAA as the primary key. This table employs a foreign key as well. 
It has: 
1. faa - char
2. icao - char
3. cityServed - char

### 3. CityState 
This table has a list of all the cities and states that flights can go in and out from. The zipcode is the primary key. It has: 
1. city - varchar
2. state - char
3. zipCode - char

### 4. Employee 
This table describes the employee and some of their information. It uses the ID as the primary key. The variables are: 
1.  ID - int
2.  furstName - varchar
3.  lastName - varchar
4.  address - varchar
5.  zipCode - char
6.  phone - char
7.  email - varchar

### 5. EmployeePosition
This table has the IDs for the employee's jobs. The variables are: 
1. employeeID- int
2. positionId - int

### 6. Flight 
This table describes the flights that are leaving one place and landing in another. There are foreign keys and primary keys in this table. 
It has: 
1. ID - int      
2. origin - char
3. destination - char
4. aircraft - int 
5. departure - timestamp 
6. arrival - timestamp


### 7. Passenger 
This table has information pertaining to some passengers who fly in the region
1. ID -int
2. firstName - varchar                   
3. lastName - varchar                   
4. address - varchar                   
5. city - varchar                   
6. state - char                    
7. zipCode - char                   
8. phone - char                      
9. email - varchar

### 8. Position
This table relates to the employee position tables. This one has the descriptive names for the job titles. It has: 
1. ID int
2. description - varchar
3. hourly - decimal


## Entity-Relationship Diagram 
With databases, it is important to have an entity-relations diagram. Here is the ER diagram for this database: 

![Images](/Images/ERDiagram.PNG)
