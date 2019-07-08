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
- Declare @myName varchar(12), 
          @amount int=123,
          @myCounter int
  print @amount
- set @myCounter

  >Declare  @balance int,
         @total int
set @balance=1000

set @total = @balance*1.02

print @total

print 'The total is:'+cast(@total as char)
