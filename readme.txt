--create database called HELLOWORLD_INSTALL_TEST
--create SQL (not windows) user with credentials that can access it 
--modify connection string in web.config file here for this connection string HELLOWORLD_INSTALL_TESTEntities to have user credentials server and db name
--run script below

CREATE TABLE [dbo].[tbl_colours](
	[unique_id] [int] IDENTITY(1,1) NOT NULL,
	[colour] [varchar](1000) NULL,
PRIMARY KEY CLUSTERED 
(
	[unique_id] ASC
)WITH (PAD_INDEX = OFF, STATISTICS_NORECOMPUTE = OFF, IGNORE_DUP_KEY = OFF, ALLOW_ROW_LOCKS = ON, ALLOW_PAGE_LOCKS = ON) ON [PRIMARY]
) ON [PRIMARY]
GO


insert into tbl_colours
select 'red'
union 
select 'orange'
union 
select 'yellow'
union 
select 'green'
union 
select 'blue'
union 
select 'indigo'
union 
select 'violet'
