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

### There are some ways to declare/ set a variable:

1. Declare a variable with initial value.

- Declare @myName varchar(12), 
          @amount int=123,
          @myCounter int
  print @amount
  
2. Declare w/o initial value and then SET it, including making a calculating:

- set @myCounter

  >Declare  @balance int,
  >
  > @total int
  >
  >set @balance=1000
  >
  >set @total = @balance*1.02
  >
  >print 'The total is:'+cast(@total as char)

3. If the value is related to the tables, then SELECT it:

- declare a variable with a cell of tables 
  > declare @variable varchar(12)
  >
  >select @variable=  姓名 from 學生 where 學號='S001'
