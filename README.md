# Football Scouting using Machine Learning with PySpark 
- Based on Transfermarkt Player Values & APIFootball.com Player Stats

This repo contains the files to replicate a way of doing real football scouting: collecting all the transfermarkt player values and the player statistics of APIfootball.com.

![url](https://images.supersport.com/media/34vlqwkk/la-liga_2324_seasonstart_11082023_sup_1200.png?width=2048&quality=90&format=webp)

The methodology is the following: 

1. I built a web-scrapping script to extract transfermarkt player values for the main football leagues, and its second division leagues.
   
2. After that, I used APIFootball.com Football API, through RapidAPI, to extract the current season stats for every player and save them within a .csv. This API also contains an internal rating.

3. We fit an a linear regression using PySpark (we could have used scikit-learn or any other ML library, but this is a university exercise to run it on several servers).

4. Once we get that rating based on current season stats, we compare it with the historical rating from APIFootball.com. We calculate the difference to determine if based on stats, the player is currently over or undervalued.
  
5. After that, we order by the descending order by player value to find good players that are currently overperforming and are cheap in the market.

BAM! I recommend you to refer to the PDF on MDA (Modern Data Architectures) I uploaded. It is much better explained.
