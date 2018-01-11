Overview
When you first create your stored procedures it may work as planned, but how to do you modify an existing stored procedure.  In this topic we look at the ALTER PROCEDURE command and it is used.

Explanation
Modifying or ALTERing a stored procedure is pretty simple.  Once a stored procedure has been created it is stored within one of the system tables in the database that is was created in.  When you modify a stored procedure the entry that was originally made in the system table is replaced by this new code.  Also, SQL Server will recompile the stored procedure the next time it is run, so your users are using the new logic.  The command to modify an existing stored procedure is ALTER PROCEDURE or ALTER PROC.

Modifying an Existing Stored Procedure
Let's say we have the following existing stored procedure:  This allows us to do an exact match on the City.

CREATE PROCEDURE dbo.uspGetAddress @City nvarchar(30)
AS
SELECT * 
FROM Person.Address
WHERE City = @City
GO
Let's say we want to change this to do a LIKE instead of an equals.

To change the stored procedure and save the updated code you would use the ALTER PROCEDURE command as follows.

ALTER PROCEDURE dbo.uspGetAddress @City nvarchar(30)
AS
SELECT * 
FROM Person.Address
WHERE City LIKE @City + '%'
GO