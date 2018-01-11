USE [Hell]
GO
/****** Object:  StoredProcedure [dbo].[usp_selectdemoData]    Script Date: 1/11/2018 8:05:41 AM ******/
SET ANSI_NULLS ON
GO
SET QUOTED_IDENTIFIER ON
GO


CREATE PROCEDURE [dbo].[usp_selectdemoData]
As

Select * from Hell..[Department];
