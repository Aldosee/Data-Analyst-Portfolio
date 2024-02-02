--Gender and Age Group per Region based on COVID cases-- 
SELECT RegionRes, AgeGroup, Sex, COUNT(sex) AS TotalSex
FROM [dbo].['DOH COVID Data Drop_ 20231107_CaseInfo]
WHERE RegionRes IS NOT NULL 
GROUP BY Sex, RegionRes, AgeGroup
ORDER BY RegionRes, AgeGroup;

--Number Health Status per Region-- 
SELECT RegionRes, HealthStatus, COUNT(HealthStatus) AS TotalStatus
FROM [dbo].['DOH COVID Data Drop_ 20231107_CaseInfo]
GROUP BY HealthStatus, RegionRes
HAVING RegionRes IS NOT NULL 
ORDER BY RegionRes;

--Grand Total based on symptoms per Region--
SELECT
    DISTINCT(region),  
    SUM(ISNULL(CONVERT(INT, conf_asym), 0)) AS Total_conf_asym,
    SUM(ISNULL(CONVERT(INT, conf_crit), 0)) AS Total_conf_crit,
    SUM(ISNULL(CONVERT(INT, conf_mild), 0)) AS Total_conf_mild,
    SUM(ISNULL(CONVERT(INT, conf_mod), 0)) AS Total_conf_mod,
    SUM(ISNULL(CONVERT(INT, conf_severe), 0)) AS Total_conf_severe,
    SUM(ISNULL(CONVERT(INT, conf_asym), 0) +
        ISNULL(CONVERT(INT, conf_crit), 0) +
        ISNULL(CONVERT(INT, conf_mild), 0) +
        ISNULL(CONVERT(INT, conf_mod), 0) +
        ISNULL(CONVERT(INT, conf_severe), 0)) AS Grand_TotalCasesPerRegion
FROM [dbo].[DOH COVID_ 20231107 - 05 DOH Data Collect - Daily Report]
GROUP BY region, cfname;


--Confirmed cases in the region per symptoms-- 
SELECT
    region,
    SUM(ISNULL(CONVERT(INT, conf_asym), 0)) AS Total_conf_asym,
    SUM(ISNULL(CONVERT(INT, conf_crit), 0)) AS Total_conf_crit,
    SUM(ISNULL(CONVERT(INT, conf_mild), 0)) AS Total_conf_mild,
    SUM(ISNULL(CONVERT(INT, conf_mod), 0)) AS Total_conf_mod,
    SUM(ISNULL(CONVERT(INT, conf_severe), 0)) AS Total_conf_severe
FROM [dbo].[DOH COVID_ 20231107 - 05 DOH Data Collect - Daily Report]
GROUP BY region;

