# Twitter Analytics -Dashboard

### Dashboard Link : https://app.powerbi.com/view?r=eyJrIjoiMTE2NGM3YzUtZjk3Zi00YjhiLWFkMmUtZDZmNDk2NjIzYWExIiwidCI6IjM0YmQ4YmVkLTJhYzEtNDFhZS05ZjA4LTRlMGEzZjExNzA2YyJ9

## About Dashboard

The Twitter Analytics Dashboard is an interactive web application designed to provide comprehensive insights into Twitter data. Utilizing advanced data visualization techniques, this project enables users to track, analyze, and visualize various Twitter metrics, including tweet frequency, engagement, sentiment analysis, and user demographics. Built using Power Query Editor, Dashboard, the dashboard offers an intuitive interface for exploring real-time and historical data, making it an invaluable tool for social media analysts and marketers


### Steps followed 

- Step 1 : Load data into Power BI Desktop, dataset is a csv file.
- Step 2 : Open power query editor & in view tab under Data preview section, check "column distribution", "column quality" & "column profile" options.
- Step 3 : Also since by default, profile will be opened only for 1000 rows so you need to select "column profiling based on entire dataset".
- Step 4 : In the report view, under the view tab, theme was selected.
- Step 5 : Since the data contains date and time, thus in order to represent the data in a useful form, the date and times were separated which made data esy to understand for future use. 
- Step 6 : Various visual filters were added for averaging the count and separe the quarters named "WithAppOpen", "WithoutAppOpen", "MediaViews" & "engagement".
- Step 7 : Dual axis chart visuals were added to the canvas, one representing MediaViews and mediaEngagements
           Using visual level filter from the filters pane, basic filtering was used & null values were unselected for consideration into average calculation.
           
           Although, by default, while calculating average, blank values are ignored.
- Step 8 : A bar chart was also added to the report design area to represent the countsreply, retweets and likes. 
- Step 9 : Drill down was added to represent the clicks for each tweet.

In our dataset, Some parameters were assigned value 0, representing those parameters are not applicable for some users.

All these values have been ignored while calculating average rating for each of the parameters mentioned above.

- Step 10 : Calculated column was created in which, users data was aversged.

for creating new column following DAX expression was written;
     
       EngagementWithoutAppOpen = CALCULATE(AVERAGE([engagement rate]), FILTER('SocialMedia (1)', [app opens] = 0))

![snap1](https://github.com/user-attachments/assets/81522f20-e5ef-415b-8a5d-ccdc7d76468a)

        EngagementWithAppOpen = CALCULATE(AVERAGE([engagement rate]), FILTER('SocialMedia (1)', [app opens] = 1))

![snap2](https://github.com/user-attachments/assets/6e821601-70be-4c66-a948-17907329bb16) 

# Snapshot of Dashboard (Power BI Service)

![dashboard](https://github.com/user-attachments/assets/a5355ff2-28f1-4277-8418-a1379dc78009)
