# MUSA_Final_Project
 
The goal of your final project is to impress your peers and your instructors by utilizing some of the tools you have learned this semester. The assignment is to communicate an engaging public policy use case of predictive modeling by showing off both your analytical skills and your ability to convert those skills into a relevant policy use case.

You are required to work in pairs (signup  HYPERLINK "https://docs.google.com/spreadsheets/d/1tT-n82UrjgB9Xt_5ZHD2qwSUdMi-6CfKeo7aiFfQv9M/edit#gid=0" here). Both team members should work on the model, but each member will present a different part of the deliverable. Each pair will receive a grade that comprises both parts of the project.

Please focus on cross-validation (random, spatial and time, where appropriate) and on goodness of fit indicators (accuracy and generalizability) that relate directly to the business process. You may have to make up the business process, but please consider social, economic etc. costs/benefits. 

I will open the project registration signup on Tuesday, 11/17 at 9am. 

Schedule

11/13 – Project introduced
11/20 – Prepare to discuss your chosen project, data, methods in lab breakout. Sharper wireframe exercise in lab.
12/4   -  Presentations in class
12/15 – Final markdown and video due

1.  Deliverable 1 (Due 11/20): Have a partner chosen, pick and project, and be prepared in lab to talk for a few minutes about the questions at the bottom of this document.

2. Deliverable 2 (Due 12/4): Team member 1 will be responsible for a 4 minute 'PechaKucha' presentation that ‘sells’ us on the idea of this fancy new planning app that you’ve designed to solve an important problem. Spend ~50% of your time on exploratory analysis and model results/validation. The expectation is that you will have preliminary model at this stage, which you will sharpen by the time the assignment is due. The other 50% should focus on questions like, What is the use case? Who is the user? How does the app put the model into the hands of a non-technical decision maker? Who is creating the app? Have you created something that is usable by the client? This is a presentation where the slides are set to change automatically, every 20 seconds. This is a requirement. Remember – sell it to us. What should come first - the model or the app? Don’t forget to constantly remind the audience about the use case to keep your solution relevant. 


3.  Deliverable 3 (12/15): 
Team member 1 will have the pechakucha uploaded on youtube with a recorded narration. Link to the video in your markdown.

Team member 2 will be responsible for a markdown write up that would allow someone to replicate your analysis (show your code blocks). Post this markdown on your Github not in a google folder. At minimum, please hit on the below components:
a. Motivate the analysis – “What is the use case; why would someone want to replicate your analysis and why would they use this approach?”
    b. Describe the data you used.
    c. Describe your exploratory analysis using maps and plots.
    d. What is the spatial or space/time process?
d. Describe your modeling approach and show how you arrived at your final model.
e. Validate your model with cross-validation and describe how your predictions are useful (accuracy vs. generalizability).
f. Provide additional maps and data visualizations to show that your model is useful.
g. Talk about how your analysis meets the use case you set out to address.
h. What could you do to make the analysis better?

I expect to see data visualizations that are of high quality. Please include codeblocks.

Project Details - Forecast Metro train delays in and around NYC (NEW): An amazing new  HYPERLINK "https://www.kaggle.com/pranavbadami/nj-transit-amtrak-nec-performance?select=2018_11.csv" dataset has popped up on Kaggle recently that list origin/destinations delays for Amtrak and NJ Transit trains. Can you predict train delays? Consider the time frame that it would be useful to have such predictions. Predicting 5 minutes out is not going to be as useful as 2-3 hours out. Consider training on a month and predicting for the next week or two. Consider time/space (train line, county etc.) cross validation. Many app use cases here.


Questions to prepare for Friday Nov 20th.

What is the use case? 
- To predict the metro train delays in and around NYC to help commuters travel reliably and efficient train scheduling.  

How could data make a difference in answering this question? Do you have a sense for the business as usual decision making?
- Data permits authorities to perform both long term and short term planning. Short-term planning can be used to handle minor modifications to daily frequency while long term handling can be used to handle seasonal variations and critical weather conditions.
Since transit network is a government undertaking the business process will mostly be non-profit making and focusing more on doing good for the society. We will separately also analyze `amtrak` data which is more of a quasi-public corporation operating as a for-profit organization.

What datasets have you identified to help you answer this question?
- The dataset consists of past train delays for the NJ train line. We plan to include census data to account for socio-economic factors. 

What kind of model would you build and what is the dependent variable?
- Linear regression model trained on the family of poisson distributions. The dependent variable is the delay (in minutes) variable. 

How will you validate this model (cross-validation & goodness of fit metrics that relate to the business process)?
- We will perform cross-validation across time (per hour) and analyze the MAE.  

How do you think that stakeholders would want to consume this data?
- Both people and the service providers will benefit from this. The analysis will help compare the performances of each of the lines/providers. This will help users make informed choices and the service providers give a better experience to the commuters.

What are the use cases for your app and what should the app do?
- The app will give probable delay estimates based on different factors like time, location, day of the week and line type. This will helps travelers plan their trip more efficiently. The same can be used by the service providers to see how their trains are performing and try to overcome factors that cause delays that may affect their revenue.    
