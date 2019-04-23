# Green_Happy_Challenge
Wells Fargo 2018 challenge on MindSumo.com
Goal: Minimize individual carbon footprint without reducing quality of life, based on the following data:
- "surveys" from 1000 individuals on more than 30 activities and their importance
- Consumption "data" on the individuals over these ~30 activities
- Sparse data on the sources used by the individuals
- units of pollution for ~10 fuel sources over the ~30 activities

I was so excited about this challenge to start, but after 30 days with more and more time spent each day after getting no where, I began to hate myself. However, I learned a lot of valuable lessons throughout the challenge: a lot about data, approaching datasets, and biased approaches based on expertise. The worst thing about this challenge was the messiness and incompleteness of the data. I spent countless hours making algorithms to score each individual and impute missing data; when the reality was that about 80% of the individuals/activites (~3000) did not have energy sources available. It turned out in the end, that Wells Fargo made up the data, and was only looking for Green Engineering ideas and suggestions, leaving us Data Scientists frustrated with the lack of any sort of correlations in this randomized survey & consumption data.

My approach:
- The 'Data_Mining' jupyter notebook (python) file takes the original data set and breaks it into multiple csv files, prepared for analysis.
- The 'Unsupervised' notebook then reads these digested files and does some further wrangling to produce metrics such as total individual carbon footprint. I attempted a few more exploratory analyses including some unsupervised clustering algorithms. 
- The 'Individual' notebook includes a class that grabs all the data for each individual. This can be used by an individual to see their carbon footprint broken down by activity, as well as recommended energy source changes and the corresponding impacts on carbon footprint.

How I could've improved:
Normality tests showed me that this data was made up, no matter how I sliced it. What I learned is that I should have run these tests before getting so deep into applying my repertoire of machine learning algorithms (supervised and unsupervised) to the data. Crunched for time left on the challenge, which I was balancing with my senior year coursework, I ended up with a sloppy solution.
I wanted to include all the data munging and results I had, even though they did not help me answer the most important aspects of the solution. If I had paid more attention to the spec, which had noted that the data may or may not be real, and stopped trying to rely on what I was best at, I could have spent a lot more time thinking about the problem from a Green Engineering perspective and crafted a more elegant solution.

What I learned:
- Disect the question, brainstorm solutions, and talk to outsiders about your intuitions before diving into code.
- In data science, diving into a data munging, hypothesis testing, and analysis, without proper planning, is typically the biggest waste of time imaginable.
- Especially for the intermediate data wrangler, where we are capable of figuring code to do anything we want, you will lose hours upon hours in black holes of organizing the data how you envisioned; only to realize there was either:
  a) an easier way to do it; or worse
  b) it was totally pointless in the scope of the taks/ big picture.
