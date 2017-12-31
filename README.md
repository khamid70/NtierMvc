# NtierMvc - Applying N-Tier over ASP.NET MVC solution

## Executive Summary

This tutorial aims to mix three main architecture styles through one complete but simple VS 2013 ASP.NET MVC web solution with C# class libraries. These architecture styles are the Model-View-Controller MVC Presentation Pattern, the N-Tiers Deployment Architecture Pattern, and the Repository Pattern plus many inline applied design patterns, such as Separation of Concerns SOC and Don’t Repeat Yourself DRY.

## Sample Business Case Problem Tutorial

This tutorial solves a business case for a fictional company called NtierMvc asks you to build a solution with the following business requirements:

* Perform Create, Update, Delete and Retrieve Employees Data.
* The Employees input fields are Id, Name, Age, HiringDate, and GrossSalary
* Apply TAX deduction Business Rule, which states that “Employees with Age less than 30 years old shall get their salary deducted by 50%, Employees with Age less than 40 years old shall get their salary deducted by 40%, Employees with Age less than 50 years old shall get their salary deducted by 30%, Employees with Age less than 60 years old shall get their salary deducted by 20%, and Employees 60 years old and above shall get their GrossSalay without deduction”.
* When viewing Employees data, you should show the a NetSalary based on the previous Business Rule.

## The Proposed Solution for the Business Case Problem

The proposed solution in this tutorial is to build simple web solution that apply 3-Tier Deployment Architecture with User Interface Layer built through ASP.NET MVC framework, a Business Logic Layer that applies the TAX deduction Business Rule, and a Data Access Layer that applies Repository Pattern for exchanging data with a SQL Server Database called NtierMvcDB. 

The proposed solution shall contain five projects and one SQL Server database as follows:
1.	SQL Server Database called NtierMvcDB as a data source for the project. This database shall contain a table named Employees.
2.	ASP.NET MVC web project named NtierMvc for the User Interface Layer.
3.	Class library named NtierMvc.BusinessLogic for the Business Logic Layer.
4.	Class library named NtierMvc.DataAccess for the Data Access Layer, the Repository.
5.	Class library named NtierMvc.Common as a cross-cutting helper component.
6.	Class library named NtierMvc.Model as a Data Contract Entity Model component.
