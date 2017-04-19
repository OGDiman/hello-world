# hello-world

Test commit changes

CREATE TABLE [dbo].[cc_details_ref] (
    [id]             INT             IDENTITY (1, 1) NOT NULL,
    [detail_name]    VARCHAR (100)   NOT NULL,
    [interface_type] VARCHAR (30)    NOT NULL,
    [detail_type]    VARCHAR (30)    DEFAULT ('char') NOT NULL,
    [created]        DATETIME        NOT NULL,
    [display]        NVARCHAR (255)  NOT NULL,
    [description]    NVARCHAR (1024) NULL,
    [author]         NVARCHAR (255)  NULL,
    [actual]         NUMERIC (1)     DEFAULT ((1)) NULL,
    [archival]       NUMERIC (1)     DEFAULT ((0)) NOT NULL,
    PRIMARY KEY CLUSTERED ([id] ASC)
);

CREATE TABLE [dbo].[cc_details_ref_values] (
    [Id]             INT           IDENTITY (1, 1) NOT NULL,
    [detail_name]    VARCHAR (100) NOT NULL,
    [value]          VARCHAR (100) NOT NULL,
    [display_value]  VARCHAR (100) NOT NULL,
    [interface_type] VARCHAR (30)  DEFAULT ('operator') NOT NULL
);
