# India-Census-2011

##-INTRODUCTION

•Census is nothing but a process of collecting, compiling, analyzing, evaluating, publishing and disseminating statistical data regarding the population.

•It is a reflection of truth and facts as they exist in a country about its people, their diversity of habitation, religion, culture, language, education, health and socio-economic status.

•The word ‘Census’ is derived from the Latin word ‘Censere’ meaning ‘to assess or to rate’.

•It covers demographic, social and economic data and are provided as of a particular date. Census is useful for formulation of development policies and plans and demarcating constituencies for elections.

•The Census of India has been conducted 15 times, As of 2011. It has been conducted every 10 years, beginning in 1871.

This repository consists of the following :
README.txt (this file)
Dataset : "india-districts-census-2011.csv"
Code PDF

Q1. Create a geographic map of states with low literacy rates.
Step 1. Group all the rows of the same state together

Step 2. Iterate through each group and calculate the total population and total literate population for that particular state.

Step 3. Literacy rate = (total literate population / total population) * 100

Step 4. Store the results for each state

Step 5. Plot the results in a geographic map of India (a) Getting coordinates (b) Creating a map (c) Using Shapefiles for drawing states (d) Creating a dataframe mapping shapes to literacy rates and state names (e) Using data to color areas

Q2. Find out most similar districts in Bihar and Tamil Nadu. Similarity can be based on any of the columns from the data.
Step 1 : Create dataframes of Bihar districts and TN districts

Step 2 : Calculate similarity matrix

To measure the similarity between two instances we can use the Euclidean distance measure. Similarity score is the inverse of Euclidean distance. Larger Euclidean distance corresponds to smaller similarity score and vice-versa.

However on observing the data we notice that the first three features are not numbers and also that the remaining features vary over a large range. In order to account for these we do the following:

• To find the euclidean distance we compute sum of squared differences of the attribute values for each column (between each row of Bihar districts and Tamil Nadu districts).

• Then, we compute the square root of the total sum computed above and inverse it. Resultant obtained is the similarity score.

• If features vary over a large range then the largest component will dominate the calculation of the similarity score. In order to avoid this we normalize the numerical attributes so that they fall between 0 and 1.

Step 3 : Plot the matrix using seaborn heatmap

Q3. How does the mobile penetration vary in regions (districts or states) with high or low agricultural workers?
Step 1 : Iterate through each group and calculate total agri workers and total households with mobiles

Step 2 : Create a dataframe holding state name, households_with_mobile and agri_workers

Step 3 : Plot statewise distribution

