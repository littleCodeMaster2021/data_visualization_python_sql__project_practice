# data_visualization_python_sql__project_practice documentation
Beginning Data Analysis practice project using matplotlib and seaborn and a self made plotting package and writing queries in sqlite3 

## Challenge Part1
For this project, I need to consider data from what is called “Subjective Metrics”, which are
mood, stress, rumination, and sleep tracking. In our iOS and Android apps, we ask users to rate
these four elements on a float scale of 0-4 , with 0 being negative and 4 being positive.
Every morning at 8am, we send our patients a notification to rate their mood and their sleep on
a circular scale. The five full options are Awful, Bad, Okay, Good, and Great! Awful is 0 and
Great is 4. Additionally, patients can enter these subjective measures throughout the day,
whenever they feel like it’s necessary.

Users can also rate their rumination (“Are you having trouble letting go of something that
happened today?”) with options “Not at all”, “Slightly”, “Moderately”, “Very”, “Extremely” and they
can rate their stress (“Are you stressed about something that might happen in the near future?”)
on the same scale.

The clinical purpose of these activities is to help patients track their sleep, mood, rumination,
and stress over time to see if therapy is making a difference. The provider can see this data too,
building the basis of a conversation they can have together.

Current, I need to solve the problem of not being able to visualize progress well for these four metrics
to mental health providers and their patients.

Data is provided in a CSV format with information on each of these four metrics. 

For each line, the first column represents the time the measurement was made, the second
column represents the id of the user submitting the rating, the third column is the type of rating
submitted, and the fourth column represents the value of the response.

Draw insights and assumption I made about the data...

##Challenge Part2

Write SQL for the given questions:

1. How many users completed an exercise in their first month per monthly cohort?
Assume you have two tables in our company’s database:
● 'users' table, with columns 'user_id', 'created_at'
● ‘exercises’ table, with columns 'exercise_id', 'user_id', 'exercise_completion_date'

Write a single SQL query that breaks up the users based on the month that they signed up (their
cohort month), and determines the percentage of users that have a completed exercise in their
first month for each monthly cohort (e.g., the 2018 January cohort has x% of users completing
an exercise in their first month, 2018 February cohort has x% of users completing an exercise in
their first month, etc.)

2. Which organizations have the most severe patient population?
Assume you have two tables in our company’s database:
● ‘Providers’ table that contains ‘provider_id’, ‘organization_id’, and ‘organization_name’
● ‘Phq9’ table that contains ‘patient_id’,’provider_id’, ‘score’,’datetime_created’
For context, A phq score ranges from 0-27 and anything 20 or above is considered severe.

Write a single query that finds the top five organizations that have the highest average phq9
score per patient.
