## Go 

- define batches.
- batches is the unit of execution
- some commands need to be a uniqlo batch, such as create view...
- /*...*/ Go can not be included in notes.

## View

- create view viewName as select * from tableName where...

## Variables

- @Local variables
- @@Global Variables

#### There are some ways to declare/ set a variable:

- Declare a variable with initial value.
```
          Declare @myName varchar(12), 
                    @amount int=123,
                    @myCounter int
          print @amount
  ```
- Declare w/o initial value and then SET it, including making a calculating:

    - set @myCounter
    
```
   Declare  @balance int,
   
   @total int
   
   set @balance=1000
  
   set @total = @balance*1.02
   
   print 'The total is:'+cast(@total as char)
```
- If the value is related to the tables, then SELECT it:

    - declare a variable with a cell of tables
    
 ```
    declare @variable varchar(12)
   
    select @variable=  姓名 from 學生 where 學號='S001'
 ```
   - these two command have the same result
 ```
Declare @total int
select @total=sum(學分) from 課程
set @total= (select sum(學分) from 課程)
print ('總學分:'+ cast(@total as char))
 ```

- variable as table
 ```
declare @students table(
學號 char(12),
姓名 char(12)
)
insert @students select 學號,姓名 from 學生 where 性別='女'    ---insert + table + select condition
select * from @students   ---print the table
 ```
 
 ## System Function, = Global Variables
 
 - @@IDENTITY: return the last number of identity column, if not=> null
 
 - @@ROWCOUNT: return that how many rows are effected
 
 - @@ERROR: return the number of error message, if not=> 0
 
 - @@SERVERNAME
 
 
 
 
