NBA like-player Recommender Engine

Modeled after Nathan Carabello's model from: https://nathancarabello.medium.com/nba-scouting-recommendation-engines-with-k-nearest-neighbors-knn-8eb0238a53d9

Using dataset from Kaggle

Download the files from these two links. I only use the cbb21 and all_seasons files for the model
NBA player data: https://www.kaggle.com/datasets/andrewsundberg/college-basketball-dataset
College team ranking data: https://www.kaggle.com/datasets/justinas/nba-players-data

You can motify the specs to base model off of, currently set to use: age,	draft_round,	draft_number,	gp,	net_rating, and college ranking

Upon completion of this mini project, I have found the findings to be quite underwhelming and largley incorrect. The data used is bias to a high degree and relies on patterned similarites instead of a sophistocated analysis of similarites between players (the analysis lacked weighted data and a robust dataset). I believe this to be the case because of the lack of variables used, I rely on age (of draft), draft round, draft number, games played (of the draft year), net rating (which I assume is also based on the year drafted), and ranking of college attended (as of 2021). The college ranking column was also irrelevant to a certain degree because if the college/university was not in the data set or the player did not attend school, the entry was -1, leaving many -1s in the dataset. The data was normalized and equally weighted when fit for the model before performing the kNN search. 

For future analysis, it would be best to use a more robust dataset that contained position/skill targeted variables; players in the roles of shooting guards will have more shots outside the arc and a higher 3-pt attempt ratio than posts for example. In addition to this, I would suggest using a single season (or a small range of seasons) instead of a data set containing players over the last few decades to get a more accurate comparison. This model also chose the draft year performance of a player, which has not always been the most telling of a players career performance, like Dirk his rookie season. Or the alternative, players pop off their rookie year and enter a slow decline. The best age range to experiment with would be mid to late 20s. 

