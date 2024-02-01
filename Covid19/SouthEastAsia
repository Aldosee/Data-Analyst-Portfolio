--Update the "Lao Peoples Democratic Republic" to "Laos" in the Global table and vaccination--
UPDATE ['vaccination-data$']
SET country = 'Laos'
WHERE country  LIKE  '%Lao People%'; 

--Cases vs Death--
SELECT country, SUM(CONVERT(INT, New_cases)) AS Total_New_Cases, SUM(CONVERT(INT,New_deaths)) AS Total_New_Deaths
FROM ['WHO-COVID-19-global-data$']
GROUP BY country
HAVING country IN ('Cambodia', 'Malaysia', 'Philippines', 'Viet Nam', 'Indonesia', 'Thailand', 'Singapore', 'Timor-Leste', 'Laos', 'Myanmar', 'Brunei Darussalam');

--East Asia Total Vaccination (Include the date) and Total 1 Dose--
SELECT country, TOTAL_VACCINATIONS, persons_vaccinated_1plus_dose
FROM ['vaccination-data$']
WHERE COUNTRY IN ('Cambodia', 'Malaysia', 'Philippines', 'Viet Nam', 'Indonesia', 'Thailand', 'Singapore', 'Timor-Leste', 'Laos', 'Myanmar', 'Brunei Darussalam');

--Get the vaccines used--
SELECT country, COMPANY_NAME
FROM ['vaccination-metadata$']
INNER JOIN ['vaccination-data$'] ON dbo.['vaccination-metadata$'].ISO3 = dbo.['vaccination-data$'].ISO3
WHERE COUNTRY IN ('Cambodia', 'Malaysia', 'Philippines', 'Viet Nam', 'Indonesia', 'Thailand', 'Singapore', 'Timor-Leste', 'Laos', 'Myanmar', 'Brunei Darussalam')
ORDER BY country;

--Calculate the Case Fatality Ratio. Based on World Health Organization calculation--

#CASE WHEN ... END AS Infection_Percentage_Rate: This conditional expression calculates the infection percentage rate.
##It checks if the total new cases are zero, and if so, sets the Infection_Percentage_Rate to 0. Otherwise, it performs the calculation (SUM(CONVERT(INT, New_deaths)) * 100.0) / NULLIF(SUM(CONVERT(INT, 
New_cases)), 0). 
###This calculation computes the percentage of new deaths relative to new cases, handling the potential divide-by-zero error by using NULLIF to set the divisor to NULL if it is zero. The CASE statement ensures that the division is only performed when there are non-zero new cases to avoid a divide-by-zero error.

SELECT country, SUM(CONVERT(INT, New_cases)) AS Total_New_Cases, SUM(CONVERT(INT,New_deaths)) AS Total_New_Deaths, 
  CASE
    WHEN SUM(CONVERT(INT, New_cases)) = 0 THEN 0
    ELSE (SUM(CONVERT(INT, New_deaths)) * 100.0) / NULLIF(SUM(CONVERT(INT, New_cases)), 0)
  END AS Case_Fatality_Ration
FROM ['WHO-COVID-19-global-data$'] 
GROUP BY country 
HAVING country IN ('Cambodia', 'Malaysia', 'Philippines', 'Viet Nam', 'Indonesia', 'Thailand', 'Singapore', 'Timor-Leste', 'Laos', 'Myanmar', 'Brunei Darussalam');
