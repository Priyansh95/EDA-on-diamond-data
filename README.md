# Data Collection 
I have taken this dataset from kaggle .This classic dataset contains the prices and other attributes of almost 54,000 diamonds. It's a great dataset for beginners learning to work with data analysis and visualization. This data set has 10 columns 
## content
 columns
1. price, price in US dollars (\$326--\$18,823)

2. carat weight of the diamond (0.2--5.01)

3. cut quality of the cut (Fair, Good, Very Good, Premium, Ideal)

4. color diamond colour, from J (worst) to D (best)

5. clarity a measurement of how clear the diamond is (I1 (worst), SI2, SI1, VS2, VS1, VVS2, VVS1, IF (best))

6. x length in mm (0--10.74)

7. y width in mm (0--58.9)

8. z depth in mm (0--31.8)

9. depth total depth percentage = z / mean(x, y) = 2 * z / (x + y) (43--79)

10. table width of top of diamond relative to widest point (43--95)

 This dataframe has 53940 rows and 10 variable.
 data link - https://www.kaggle.com/datasets/shivam2503/diamonds
## Extracting relevant info about dataframe
 1. Describing the different columns : At first , I checked the details of columns of the dataset using describe() function .I found different aggregates like mean 
    count , standard deviation , mimimum and maximum values . Then i found some columns (cut ,color ,clarity ) has only object dtypes , i described them separately 
    using  pd.describe(include = 'object') 
 2. Calculation of unique values of each column : I have calculated all the unique values and their numbers  using unique() and nunique() . I found 5 Unique values in 
    cut column , 7 unique values in color column and 8 unique values in clarity column.
 3. Then ,i have taken a sample of 55% of total data using sample(frac=0.55, random_state = 99) and accessed the rest 45% using negation .
 4. Then , I have calculated Percentage of each value of cut columns 
 5. Merging and renaming of the columns of the dataframe 
## operation with duplicates 
 1. I have executed diam.isna().sum() and the output was 0 ,so there is no duplicate value in dataframe
 2. if any duplicate occurs then we can apply .drop_duplicates() to remove them
## Visulisation of the dataset 
 1. I have the distribution of the cut ,color and clarity column distribution using histogram by using seaborn and matplotlib.pyplot
 2. then , I have plotted a scatterplot taking x = carat and y = depth using seaborn scatterplot
## Filtering 
 1. Find the best diamond having cost  less than 1000$ and has best color and clarity .
         I have executed the code and found that there is only 1 matches the requirement 
 2. Find the diamond that have length(x) > 5 mm and bredth(y) > 5mm and depth(z) > 5mm
 3. Getting the groups using Groupby function 
## Creating Pivot Table
  1. Using df.pivot_tabel
 
    
  


