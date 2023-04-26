# data-pre-processing

The main aim is to construct a Credit Risk Model that measures probability of “default” for every personal account. Here the main objective is to pre-process the data so that further predictions can be made by applying certain data model in the later stage. 

A detailed report is added with all the changes that were made to the original data set where I described what each column of the new data set represents.

Following instructions were followed:

1. You’ve been given is a sample from a larger data set that belongs to an affiliate bank based in the United States. Therefore, all the values are in dollars, so youneed to provide their euro equivalents.
2. The loan information is stored in the CSV file called loan data, which you can download from the resources.
3. Then every categorical variable must be quantified. So, we need to change any text columns into numbers based on the information they contain. For some, like the issue date on each loan, the transformation is extremely straightforward, since we can split the accounts by months. For example, if all the data is related to a single year only, there is no need to deal with whole date. Rather we can just retain the month information.
4. Similarly for other columns, we only care if they provide positive or negative connotations. So, we'll be turning them into dummy variables that hold either zero or one. Furthermore, when we're measuring credit worthiness, we need to be extremely risk averse and distrustful of any unavailable data. That's why the consensus in the field is that missing information suggests foul play because loan applications are self reported to elaborate since candidates fill out their loan applications manually. There is an incentive to withhold information which can lower their chances of getting a loan. Of course, we prefer to give out loans to applicants who can repay them so that the information isn't available will just assume the worst. However, what is worst varies from one column to the next.
5. The management team has provided us the casting directions for the data set. They are not in the favour of deleting any missing data. Instead, they prefer to fill the missing data by using minimum, maximum or some other value depending upon the context. Obviously, you can discard the columns which do not play any significant role or you can also delete those columns which are highly co-related or can replace each other.

Here are some of the suggested steps:

1. Import the required packages/libraries
2. Check if there is any problem of missing data. Do some statistical checks to analyze the given features
3. Split the dataset into numeric and non-numeric sub-sets. Make sure that both newly created data sets have proper headers for understanding.
4. Start with non-numeric data pre-processing
Some of the tasks you can do is:
  - There are different types of loan-status: You can categorize these status into good or bad and can assign some 0,1 values
  - Analyze the “term” column: Analyze and assign some values .
  - Analyze the relationship between grade and sub-grade column. Are these columns related? If yes, what should be the next step in terms of pre-processing? Can we assign some values to these columns instead of textual information?
  - Work on “verification status” column.
  - Analyze the “url” column and think about its significance and next step.
  - Analyze the “state address” column. Check how many number of entries are there for each state. Is there any problem of missing data? The other thing we can implement here is to assign values to these states based on their location into four regions as per this document https://www2.census.gov/geo/pdfs/mapsdata/maps/reference/us_regdiv.pdf and can replace the missing entries by 0.
5. Analyze and work on numeric data columns: Some of the things which you can do:
  - Fill the missing values of Funded amount, Loaned Amount, Interest Rate, Total Payment, Installment, interest rate with some fillers like min, max, average depending upon the context.
  - Convert the currency USD to Euro wherever applicable in the data set
  - Sort and store the new refined data set.
