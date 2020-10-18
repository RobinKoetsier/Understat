# Understat
Repo for scraping and plotting Understat data

There is an easy way to plot expected goal timelines and shotmaps yourself. Understat.com provides data of all shots in a game and their xG value. In some easy steps we will:

[- Install Understatr and tidy data](#install-understatr-and-tidy-data)

[- Inspect and modify the data](#inspect-and-modify-the-data)

[- Plot an xG shotmap](#plot-an-xg-shotmap)

**- Plot an xG timeline**

I will assume that you have at least some knowledge with R and already have some packages installed. If not, start by searching info and tutorials about R and RStudio. 

# Install Understatr and get data

Download the Understatr package from [https://github.com/ewenme/understatr](https://github.com/ewenme/understatr) and load it along with the tidyverse

```
pacman::p_load(tidyverse, understatr)
```

Understatr has a few functions, see: 

[https://rdrr.io/github/ewenme/understatr/man/](https://rdrr.io/github/ewenme/understatr/man/) 

and 

[https://github.com/ewenme/understatr](https://github.com/ewenme/understatr)

Go to your preferred match on understat.com. The url will look like this : https://understat.com/match/14828

The number at the end is the match id. You need this number to get the shots. With this number you can run:
```
match <- get_match_shots(14828)
head(match)
```
Which will give you this:
```
# A tibble: 6 x 20
      id minute result     X     Y     xG player h_a   player_id situation season shotType match_id
   <dbl>  <dbl> <chr>  <dbl> <dbl>  <dbl> <chr>  <chr>     <dbl> <chr>      <dbl> <chr>       <dbl>
1 381911     14 Saved… 0.902 0.707 0.0362 Iago … h          2290 OpenPlay    2020 LeftFoot    14828
2 381912     23 Saved… 0.942 0.435 0.355  Santi… h          2384 SetPiece    2020 Head        14828
3 381913     25 ShotO… 0.919 0.371 0.355  Sergi… h          8122 OpenPlay    2020 RightFo…    14828
4 381914     27 Saved… 0.89  0.542 0.442  Santi… h          2384 OpenPlay    2020 LeftFoot    14828
5 381915     27 Block… 0.878 0.452 0.0999 Iago … h          2290 OpenPlay    2020 RightFo…    14828
6 381916     27 Misse… 0.853 0.34  0.0458 Fran … h          6931 OpenPlay    2020 RightFo…    14828
# … with 7 more variables: h_team <chr>, a_team <chr>, h_goals <dbl>, a_goals <dbl>, date <dttm>,
#   player_assisted <chr>, lastAction <chr>
```


# Inspect and modify the data

# Plot an xG shotmap

# Plot an xG timeline

# Make everything look prettier 
