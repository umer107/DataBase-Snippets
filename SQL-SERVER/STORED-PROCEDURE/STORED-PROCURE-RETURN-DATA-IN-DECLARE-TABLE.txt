USE [Hell]
GO
/****** Object:  StoredProcedure [dbo].[usp_SelectedDataFromDeclareVariable]    Script Date: 1/11/2018 8:10:12 AM ******/
SET ANSI_NULLS ON
GO
SET QUOTED_IDENTIFIER ON
GO
ALTER PROCEDURE [dbo].[usp_SelectedDataFromDeclareVariable]
@Id  int 
As
Declare @ReturnTable table (DepartmentId int , DepartmentDescription varchar(max))

Insert into @ReturnTable
Select DeptID , DeptName from Department



Select * from @ReturnTable
