# Data_Wrangling

### Need to have:
- Pandas
- Numpy
- Matplotlib for the graphs
- Statisticts module

### Prerequisites:
- Data Wrangling techniques
- Unit testing 
- Functional programming(apply, map, reduce)

For example, to get modify every column in a data frame (to get a percentage in this case), instead of writing:

    for column in df:
      column = column/10*100

use:

    def get_percentage(score):
      score/10*100

df.apply(get_percentage, axis = 1)


### Instruction:
#### The data contains the personality scores for the recruits and the department they applied for.

1. Read in the dataset personality_scores.csv in this repo. Examine the data frame for duplicates (based on ID), and drop any duplicates that exist. Assert that the new data frame is the length of the unique entries of the original data frame.

2. Write functions that will:
    (1) convert the answer on each of the personality test questions to a number, as set out in scoring, and 
        (2) calculate total scores for each of the subscales (conscientiousness, emotional stability, openness to new experience, agreeableness, extraversion). As you are doing this, first create unit tests that will test that the functions work as they should.

3. Create a function/functions that takes in subscale total, and for each subscale, creates a new column called “{subscale_name}_interpretation” (e.g., conscientiousness_interpretation) and applies the labels “low”, “medium”, or “high” according to a person’s score on that subscale. Cut-off scores corresponding to the low, medium and high groups can be found in scoring.md. Again, write a unit test before creating this function that tests whether the generate_score_interpretation function works.

4. Read in the data in departments.csv and merge this data frame with the personality score data frame, keeping all applicants within the department data frame. Assert that the newly created merged data frame has the same amount of rows as the department data frame, and the expected number of columns.

5. Create histograms of personality scores by department. You may need to clean some of the department names.

