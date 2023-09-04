# Tableau-Visualization-
STEPWISE PROCESS TO DOWNLOAD TABLEAU 2023
1. Download tableau(https://www.tableau.com/products/public/download)
2. Fill up the form(first name, last name,email,country,state)
3. Download ( MAC or Window)
4. Double-click on the application and click agree
5. After downloading, You can type (Type here to search in the window)

   TABLEAU CAN NOT DIRECTLY CONNECT TO THE DATABASE, WE HAVE TO USE EXCEL
   STEPWISE PROCESS:
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
   

