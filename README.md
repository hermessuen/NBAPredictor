# NBAPredictor

Used Machine Learning to predict whether or not the home team in a NBA game would win based on game statistics. Used features and NBA data that was posted here:

https://www.kaggle.com/nathanlauga/nba-games/

I also examined a NBA betting odds for a series of games from 2013-2019 to determine how accurate the Vegas prediction was. It was found that betting odds were about 68% accurate in determining whether or not the home team won a particular game. 

I then trained a model to predict whether a home team would win a game based on field goal percentages, assists, and rebounds. I did feature scaling to ensure that they were all within acceptable ranges. I engineered “new” features, mostly through comparing the Away Team and Home Team statistics (dividing, or creating flags when the Home Team stats were much better than the Away Team stats). These newly “engineered” features ended up greatly reducing performance of the model so they were scrapped.

Several models were trained, and what performed the best was an SVM with Gaussian Kernels. Finally, RAPM (https://www.nbastuffer.com/analytics101/regularized-adjusted-plus-minus-rapm/)  statistics for each team were calculated for each team, and this was included in the final model which had an accuracy of 85% (5-fold cross-validation accuracy). However, several limitations of this model should be noted. The first is that it would not really be feasible to use it for sports betting purposes because we would not be able to know game stats such as number of rebounds or assists until after the game is included. Second, the RAPM stats were used based on a teams performance for that year. Old predictions would have more data on RAPM, while new stats (games in the start of a season) would not.  Link to GitHub repo: https://github.com/hermessuen/NBAPredictor
