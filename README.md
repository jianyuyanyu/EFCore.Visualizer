![EFCore.Visualizer](doc/IconMedium.png "EFCore.Visualizer")

# Entity Framework Core Query Plan Visualizer

View Entity Framework Core query plan directly inside Visual Studio.

[![Visual Studio Marketplace Version](https://img.shields.io/visual-studio-marketplace/v/GiorgiDalakishvili.EFCoreVisualizer?style=for-the-badge&logo=visualstudio&label=Download%20Now&color=purple)](https://marketplace.visualstudio.com/items?itemName=GiorgiDalakishvili.EFCoreVisualizer)
[![Visual Studio Marketplace Downloads](https://img.shields.io/visual-studio-marketplace/d/GiorgiDalakishvili.EFCoreVisualizer?style=for-the-badge)](https://marketplace.visualstudio.com/items?itemName=GiorgiDalakishvili.EFCoreVisualizer)
[![Visual Studio Marketplace Rating](https://img.shields.io/visual-studio-marketplace/r/GiorgiDalakishvili.EFCoreVisualizer?style=for-the-badge)](https://marketplace.visualstudio.com/items?itemName=GiorgiDalakishvili.EFCoreVisualizer&ssr=false#review-details)


## Introduction

With the Entity Framework Core query plan debugger visualizer, you can view the query plan of your queries directly inside Visual Studio. Currently, the visualizer supports SQL Server, PostgreSQL, SQLite, MySQL and Oracle.

> [!IMPORTANT] 
> The visualizer requires **Visual Studio Version 17.9.0 ([Released on February 13th, 2024](https://devblogs.microsoft.com/visualstudio/visual-studio-2022-17-9-now-available/)) or newer** and supports **EF Core 7 or newer**.

### Visual Studio Toolbox - EFCore.Visualizer Extension for Visual Studio

[![Visual Studio Toolbox - EFCore.Visualizer Extension for Visual Studio](https://img.youtube.com/vi/0z5320LK9LI/0.jpg)](https://www.youtube.com/watch?v=0z5320LK9LI)

## Usage

After installing the [extension from the marketplace](https://marketplace.visualstudio.com/items?itemName=GiorgiDalakishvili.EFCoreVisualizer), a new debugger visualizer will be added to Visual Studio. When debugging, hover over your queries and there will be an option to view the query plan (Here we show the actual query plan which means it forces query execution ):

![VariableVisualizer](doc/VariableVisualizer.png)

Click on 'Query Plan Visualizer' and the query plan will be displayed for your query.

### SQL Server:

![Sql Server Plan](doc/SqlServerDarkMode.png)

![Sql Server Plan](doc/SqlServerLightMode.png)

### PostgreSQL:

![PostgreSQL Plan](doc/PostgreSQLPlan2.png)

![PostgreSQL Plan](doc/PostgreSQLPlan1.png)

### MySQL:

![MySQL Plan](doc/MySqlLightMode.png)

![MySQL Plan](doc/MySqlDarkMode.png)

### SQLite:

![SQLite Plan](doc/SQLitePlan.png)

### Oracle:

The query plan includes Actual IO stats, Outline data, Projections, and Predicates.

![Oracle Plan](doc/OraclePlan1.png)
![Oracle Plan](doc/OraclePlan2.png)

## Known Issues:

 - If query plan extraction takes more than 5 seconds, you will get [Evaluation timed out error](https://github.com/Giorgi/EFCore.Visualizer/issues/25)
 - If your project uses Application Insights, you might get [Cannot evaluate expression since the function evaluation requires all threads to run.](https://github.com/Giorgi/EFCore.Visualizer/issues/28) when viewing query plan. **Workaround** - disable Application Insights when running your project with a debugger attached.

## Credits

This extension uses [pev2](https://github.com/dalibo/pev2/), [html-query-plan](https://github.com/JustinPealing/html-query-plan) and 
[Treeflex](https://dumptyd.github.io/treeflex/) to display query plans.
