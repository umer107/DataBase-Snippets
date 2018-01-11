USE [Hell]
GO
/****** Object:  StoredProcedure [dbo].[usp_SelectedIdBasedData]    Script Date: 1/11/2018 8:07:46 AM ******/
SET ANSI_NULLS ON
GO
SET QUOTED_IDENTIFIER ON
GO
CREATE PROCEDURE [dbo].[usp_SelectedIdBasedData]
@Id  int
As 


Select * from Hell..[Department] where DeptID = @Id

