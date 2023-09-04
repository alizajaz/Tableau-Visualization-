# Tableau-Visualization-
STEPWISE PROCESS TO DOWNLOAD TABLEAU 2023
1. Download tableau(https://www.tableau.com/products/public/download)
2. Fill up the form(first name, last name,email,country,state)
3. Download ( MAC or Window)
4. Double-click on the application and click agree
5. After downloading, You can type (Type here to search in the window)

   TABLEAU CAN NOT DIRECTLY CONNECT TO THE DATABASE, WE HAVE TO USE EXCEL
   STEPWISE PROCESS:
    **A.**
1. RUN THIS
       Select SUM(new_cases) as total_cases, SUM(cast(new_deaths as int)) as total_deaths, SUM(cast(new_deaths as int))/SUM(New_Cases)*100 as DeathPercentage
        From PortfolioProject..CovidDeaths$
      --Where location like '%states%'
        where continent is not null 
      --Group By date
      order by 1,2
(note: HIT ON top LEFT (RESULT) CTRL SHIFT C )
    It's copy the data and header
2. Go to excel
   Insert or paste the copied file from the upper query(RESULTS)
   save Excel file in TableauTable1.xlsx

   **B.**
   RUN THIS
Select location, SUM(cast(new_deaths as int)) as TotalDeathCount
From PortfolioProject..CovidDeaths$
--Where location like '%states%'
Where continent is null 
and location not in ('World', 'European Union', 'International')
Group by location
order by TotalDeathCount desc

CTRL+SHIFT+C(IT will copy with the header, then save in Excel and save as TableuTable2.xlsx)

**C.**
REPEAT LIKE A AND B
Select Location, Population, MAX(total_cases) as HighestInfectionCount,  Max((total_cases/population))*100 as PercentPopulationInfected
From PortfolioProject..CovidDeaths$
--Where location like '%states%'
Group by Location, Population
order by PercentPopulationInfected desc
**(NOTE:if there is null replace ALL to 0)**

**D.**
REPEAT LIKE A,B AND C
Select Location, Population,date, MAX(total_cases) as HighestInfectionCount,  Max((total_cases/population))*100 as PercentPopulationInfected
From PortfolioProject..CovidDeaths$
--Where location like '%states%'
Group by Location, Population, date
order by PercentPopulationInfected desc
**(NOTE:if there is null replace ALL to 0 AND CHANGE DATE TO SHORT DATE(HOME MENU) )**

We have 4 Excel data , now we can visualize into Tableau.
GO to Tableau>Microsoft excel>TableauTable1.xlsx>sheet1(Go to worksheet)>go to sheet 2 (click +sign below)>click new data Source>microsoft excel>TableauTable2.xlsx>
go to sheet 3(click +sign below)>click new data Source>microsoft excel>TableauTable3.xlsx>
go to sheet 4 (click +sign below)>click new data Source>microsoft excel>TableauTable4.xlsx

