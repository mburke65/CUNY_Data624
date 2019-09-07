2.1 Use the help function to explore what the series gold, woolyrnq and gas represent.
Use autoplot() to plot each of these in separate plots.
What is the frequency of each series? Hint: apply the frequency() function.
Use which.max() to spot the outlier in the gold series. Which observation was it?

3. Download some monthly Australian retail data from the book website. These represent retail sales in various categories for different Australian states, and are stored in a MS-Excel file.
You can read the data into R with the following script:
retaildata <- readxl::read_excel("retail.xlsx", skip=1)
The second argument (skip=1) is required because the Excel sheet has two header rows.
Select one of the time series as follows (but replace the column name with your own chosen column):
myts <- ts(retaildata[,"A3349873A"],
  frequency=12, start=c(1982,4))
Explore your chosen retail time series using the following functions:
autoplot(), ggseasonplot(), ggsubseriesplot(), gglagplot(), ggAcf()
Can you spot any seasonality, cyclicity and trend? What do you learn about the series?
