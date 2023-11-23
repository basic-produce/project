[Main portfolio](https://thong-pm.github.io/)

<iframe title="Business Forecast Tracking" width="1000" height="500" src="https://app.powerbi.com/view?r=eyJrIjoiYzFkM2YzMTQtMjhhOS00NGE0LTgzMzEtYTBlMTBmNWY3Nzk0IiwidCI6Ijk0YzBmYWUxLWY5MDEtNDMwZi05ZTkyLWJiMGZkNzMxZTlmNCIsImMiOjEwfQ%3D%3D" frameborder="0" allowFullScreen="true"></iframe>

## Context
I have worked for an e-commerce company, where cash flow forecasting was an essential part of the operation. The company's main market was American, and products were sold via Amazon. Needless to say, the competition was a real deal and to be able to make financial and operational decisions based on future trends and changes patterns of data, which were aggregated and analyzed to predict was a must-do. 

In my role, I involved in both maintaining the monthly rolling cash flow forecasting and evaluating the accuracy of the forecast. Evaluating the accuracy of the forecast was crucial because it proved the monthly rolling cash flow forecasting I produced each month was legit and reliable in making the right decisions.

### Resource:
pbix file: [pbix file](https://github.com/thong-pm/Data_Port/blob/45b2e9193cb5df68c06d621bad574048690db11f/PowerBI/1.%20Cashflow%20forecast%20tracking/Business%20Forecast%20Tracking.pbix)

mySQL file: [Query file](https://github.com/thong-pm/Data_Port/blob/main/PowerBI/Forecast%20tracking/foreast_track_query.sql)

live version: [PowerBI embedded publish link](https://app.powerbi.com/view?r=eyJrIjoiYzFkM2YzMTQtMjhhOS00NGE0LTgzMzEtYTBlMTBmNWY3Nzk0IiwidCI6Ijk0YzBmYWUxLWY5MDEtNDMwZi05ZTkyLWJiMGZkNzMxZTlmNCIsImMiOjEwfQ%3D%3D)

Visisualization of rolling forecasting and forecast tracking combined, we called the report Forecast Tracking

***Disclaimer: The data was censored or edited to protect my previous company's privacy.***

![Overview Tab](assets/Overview_tab.png)

Below is the basic database relationship, in this case, it's a simple star schema meanwhile in reality, there can be a lot more data involved due to the business demand. 

![Database Diagram](assets/database_diagram.png)

## SQL Query
"Data should be transformed as far upstream as possible, and as far downstream as necessary."

I extracted and transformed the data using mySQL. Full mySQL query can be found in this link: [Full Query](https://github.com/thong-pm/Data_Port/blob/main/PowerBI/Forecast%20tracking/foreast_track_query.sql). Mostly try to join the revenue columns from actual and forecasting tables, redefine some attributes with CASE function and format the date time data type.
## Visualization

### Line Column Chart
The main visualization of the chart is the line column chart. The columns represents revenue has been gathered. While the lines are the forecast versions, usually 3 or 4 latest months.

![Line And Column](assets/line_and_column_chart.png)

The lines can be toggled on and off using the slicer below, which is the same colors of the lines. You can try it yourself. [Link](https://app.powerbi.com/view?r=eyJrIjoiYzFkM2YzMTQtMjhhOS00NGE0LTgzMzEtYTBlMTBmNWY3Nzk0IiwidCI6Ijk0YzBmYWUxLWY5MDEtNDMwZi05ZTkyLWJiMGZkNzMxZTlmNCIsImMiOjEwfQ%3D%3D)

Other slicers can also be applied:

- category/sku
- months
- country
- sales team

### Score cards:

![Score Cards](assets/score_cards.png)

The month of the version is June therefore, the month-on-month comparison would be between June and May. In this case, there was a reduction of nearly 10% of the total revenue forecasted in June compared to May, which is significant, and an ad-hoc meeting was appointed with the main person in charge of the forecast for cross-checking. 

And for the actual revenue of June versus the previous version. Lag 1 was compared the total of actual revenue of June with the forecasted couterpart in May forecast version, lag 2 compared with April, and so on. The further the lag was, the accuracy started to drop aggressively.

## Conclusion
Although it may vary on businesses, these metircs more or less are the a requirement in Forecast Tracking.

The columns and lines combined with the element can be toggled on and off helps in the data transformation aspect, only 1 csv file was extracted in the process. No need to build too many sets of data or separate visualizations, in fact, I can always add more month versions (more lines) and give people the choices whether to view that month or not.
