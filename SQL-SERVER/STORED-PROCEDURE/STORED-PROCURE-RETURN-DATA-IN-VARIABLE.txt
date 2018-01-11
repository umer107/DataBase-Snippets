USE [Hell]
GO
/****** Object:  StoredProcedure [dbo].[usp_GetDataThroughDeclareVariable]    Script Date: 1/11/2018 8:08:42 AM ******/
SET ANSI_NULLS ON
GO
SET QUOTED_IDENTIFIER ON
GO
ALTER PROCEDURE [dbo].[usp_GetDataThroughDeclareVariable]
As
--Intialize Variable
Declare @TotalCount int
Select @TotalCount = Count(*) from Hell..[Department]
--Return Variable
Select @TotalCount
