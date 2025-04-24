# -JOINS-PRACTICE

*COMPANY: CODTECH IT SOLUTIONS

*NAME: RAYINERI HARISH

INTERN ID: COD73117

"DOMAIN: SQL

*DURATION: 4 WEEEKS

MENTOR: NEELA SANTOSH

In this task, I explored and implemented various SQL join operations to meaningfully combine data from multiple tables using pgAdmin 4, a powerful web-based interface for PostgreSQL database management. The objective was to understand how different types of joins—INNER JOIN, LEFT JOIN, RIGHT JOIN, and FULL OUTER JOIN—can be used to analyze data by merging it from two related tables.

🗃️ Tables Used
To demonstrate join operations, I created two tables in pgAdmin 4:

Employees – containing employee ID, name, and department ID.

Departments – containing department ID and department name.

These tables were chosen because they share a common key: DeptID. This key enables us to link employees to their respective departments.

🔨 Table Creation and Data Insertion
Using the Query Tool in pgAdmin 4, I executed SQL scripts to create the tables and insert sample data. The Employees table includes a few employees assigned to departments, while one employee has a NULL department, simulating real-world cases where data might be missing or incomplete. Similarly, the Departments table contains department entries, including one department not linked to any employee.

🔍 Join Operations and Output Analysis
INNER JOIN:
This join returned only the records that had matching department IDs in both tables. It effectively filters out employees with no department and departments with no employees. It’s useful for generating precise reports where only valid, matched records are relevant.

LEFT JOIN (or LEFT OUTER JOIN):
This query returned all employees, including those who do not belong to any department. For such unmatched records, the department fields returned NULL. This type of join is valuable when we want to retain all records from the left table (in this case, Employees) for audits or completeness.

RIGHT JOIN (or RIGHT OUTER JOIN):
This returned all departments, including those not linked to any employees. It ensured no department data was left out even if there were no employees assigned. This join is often used for organizational mapping or resource allocation.

FULL OUTER JOIN:
This join combined the results of both LEFT and RIGHT joins. It included all employees and all departments, showing NULL where matches were absent on either side. This provides the most comprehensive overview, useful for identifying data mismatches or incomplete entries.


#OUTPUT
#FULLOUTERJOIN
"empid","name","deptname"
1,"Alice","HR"
2,"Bob","IT"

#INNERJOIN
"empid","name","deptname"
1,"Alice","HR"
2,"Bob","IT"

#RIGHTJOIN
"empid","name","deptname"
1,"Alice","HR"
2,"Bob","IT"
NULL,NULL,"Marketing"

#LEFTJOIN
"empid","name","deptname"
1,"Alice","HR"
2,"Bob","IT"
3,"Charlie",NULL
4,"David",NULL
