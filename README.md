# project

I have worked for an e-commerce company, where cash flow forecasting was an essential part of the operation. The company's main market was American, and products were sold via Amazon. Needless to say, the competition was a real deal and to be able to make financial and operational decisions based on patterns of data, which were aggregated and analyzed to predict future trends and changes was a must-do. 

In my role, I took part in both maintaining the monthly rolling cash flow forecasting and also evaluating the accuracy of the forecast. Evaluating the accuracy of the forecast was crucial because it proved the monthly rolling cash flow forecasting I produced each month was legit and reliable in making the right decisions.

Rolling forecasting and forecast tracking combined, I called the report forecast tracking; PowerBI embedded publish link.

Disclaimer: The data was censored or edited to protect my previous company's privacy.

Image
Image


Below is the basic database relationship, although, in reality, there is a lot more data involved due to the business demand. 

The data to feed into powerBI report was queried and exported as csv file to feed into PowerBI, however, more direct connection between PowerBI and company’s database was under the setting up process.

Full mySQL query can be found on this link. Mostly try to join the revenue columns from actual and forecasting tables, redefine some attributes with CASE and format the date time data type.
Link
Main visualization of the chart is the line column chart. Which column represents revenue in reality has gathered. While the lines are the version of forecast, usually 3 or 4 latest months.

The lines can be toggled on and off using the slicer below, which is the same colors of the lines. Try it yourself. Link

Other slicer can be applied 

category/sku
months
country
sales team




Score cards:

The month of the version is June therefore, month-on-month comparison would be between June and May. In this case there was a reduction of nearly 10% of total revenue forecasted in June compared to May, which is significant, and an ad-hoc meeting was appointed with the main person in charge of forecast version June for cross-checking. 

And for the actual revenue of June vs the previous version of forecast. Lag 1 was compared to revenue forecasted for June to May, lag 2 is April and so on. The further the lag was, the accuracy started to drop aggressively.  



This is the basics forecast tracking that is required in my business, although it varies on business will require more or less features. 

The column and lines combined with the element can be toggled on and off helps in the integrating data aspect, I don’t really need to build too many sets of data or seperated visualizations, in fact I can always add more versions (more lines) and give people the choices whether to view that month or not.
