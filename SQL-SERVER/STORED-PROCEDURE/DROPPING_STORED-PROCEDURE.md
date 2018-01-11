Dropping Single Stored Procedure
To drop a single stored procedure you use the DROP PROCEDURE or DROP PROC command as follows.

DROP PROCEDURE dbo.uspGetAddress 
GO
-- or
DROP PROC dbo.uspGetAddress 
GO
Dropping Multiple Stored Procedures
To drop multiple stored procedures with one command you specify each procedure separated by a comma as shown below.

DROP PROCEDURE dbo.uspGetAddress, dbo.uspInsertAddress, dbo.uspDeleteAddress
GO
-- or
DROP PROC dbo.uspGetAddress, dbo.uspInsertAddress, dbo.uspDeleteAddress
GO