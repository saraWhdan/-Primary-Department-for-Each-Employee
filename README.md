# -Primary-Department-for-Each-Employee

Problem Link:
(https://leetcode.com/problems/primary-department-for-each-employee/description/?envType=study-plan-v2&envId=top-sql-50)
## Solution

```sql
SELECT e.employee_id,e.department_id
FROM Employee e
inner join (select employee_id,count(*) department_count
from Employee
group by employee_id) c
on c.employee_id=e.employee_id
WHERE c.department_count=1 OR e.primary_flag='y'

```

