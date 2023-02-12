# notes

## SQL query

```SQL
    SELECT DISTINCT T.name
    FROM Instructor AS T, Instructor AS S
    WHERE T.Salary > S.Salary AND 
    S.dept_name = 'Comp_Sci';
```

Another example could be:
A **query** to select all instructor names which have string 'dar' in their name

```SQL
    SELECT name FROM instructor WHERE name LIKE '%dar%'
    -- this %<string>% helps to specify the string
    -- which would be a part of the users  name
```

### it is not same as matching a string with "%" in it like 100%

```sql
LIKE '100%' escape'\'
```

## WHERE clause

```sql
-- WHERE has a range operation 
SELECT name from instructor WHERE salary between 90000 AND 100000
-- It also has a tuple comaprision support
SELECT name,course_id FROM instructor,teaches WHERE (instructor.ID, dept_name) = (teaches.ID, 'Biology');
```
