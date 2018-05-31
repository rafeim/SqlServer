CREATE DATABASE [AdminDB]
GO


USE [AdminDB]
GO 

CREATE SCHEMA [AlwaysOn]
GO 

SET ANSI_NULLS ON
GO

SET QUOTED_IDENTIFIER ON
GO

CREATE TABLE [AlwaysOn].[JobSync](
	[ID] [int] IDENTITY(1,1) NOT NULL,
	[JobName] [varchar](100) NULL,
	[PrimaryReplica] [varchar](100) NULL,
	[SecondaryReplica] [varchar](100) NULL,
	[DateModified] [datetime] NULL,
	[Type] [char](7) NULL
) ON [PRIMARY]
GO

ALTER TABLE [AlwaysOn].[JobSync] ADD  DEFAULT (getdate()) FOR [DateModified]
GO

