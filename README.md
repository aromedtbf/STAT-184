The Metropolitan Transportation Authority of New York City
================

I will begin analysing the data provided from New York City's transportation authority, also known as the MTA. The following data used will include success and failure rates for each department.
In order to use this data, I had to apply through its website in order to obtain this data. The given data will be provided along with this file, and in the website. In order to make this data easier to read, there were csv files created in order to yield a viable graph and for data wrangling purposes.

New York City is one of the most populated cities in the world, and has one of the largest public transportation systems in the world as well.

Below is a comparison between the Completed and projected Trips from MTA Bus and MTA New York City Bus. Note: On 2012, Hurricane Sandy did affect service, along with other years due to suspension of service.

``` r
bustripdata <- read.csv("bustrip.csv")
bustripdata %>% 
  ggplot(aes(x=PERIOD_YEAR,y=count,color=type)) +
  stat_smooth() +
  geom_point() + 
  xlab("Year") + 
  ylab("% of Completed Trips")
```

![](README_files/figure-markdown_github/unnamed-chunk-2-1.png)

``` r
bustripdata <- read.csv("bustrip.csv")
knitr::kable(bustripdata)
```

|    X| INDICATOR\_NAME                 |  PERIOD\_YEAR|     count| type   |
|----:|:--------------------------------|-------------:|---------:|:-------|
|    1| % of Completed Trips - NYCT Bus |          2008|  99.30000| TARGET |
|    2| % of Completed Trips - NYCT Bus |          2008|  99.27833| ACTUAL |
|    3| % of Completed Trips - NYCT Bus |          2009|  99.40000| TARGET |
|    4| % of Completed Trips - NYCT Bus |          2009|  99.16417| ACTUAL |
|    5| % of Completed Trips - NYCT Bus |          2010|  99.40000| TARGET |
|    6| % of Completed Trips - NYCT Bus |          2010|  98.41750| ACTUAL |
|    7| % of Completed Trips - NYCT Bus |          2011|  99.36000| TARGET |
|    8| % of Completed Trips - NYCT Bus |          2011|  97.93667| ACTUAL |
|    9| % of Completed Trips - NYCT Bus |          2012|  99.36000| TARGET |
|   10| % of Completed Trips - NYCT Bus |          2012|  98.72667| ACTUAL |
|   11| % of Completed Trips - NYCT Bus |          2013|  99.36000| TARGET |
|   12| % of Completed Trips - NYCT Bus |          2013|  99.26583| ACTUAL |
|   13| % of Completed Trips - NYCT Bus |          2014|  99.36000| TARGET |
|   14| % of Completed Trips - NYCT Bus |          2014|  98.89083| ACTUAL |
|   15| % of Completed Trips - NYCT Bus |          2015|  99.36000| TARGET |
|   16| % of Completed Trips - NYCT Bus |          2015|  98.58333| ACTUAL |
|   17| % of Completed Trips - NYCT Bus |          2016|  99.36000| TARGET |
|   18| % of Completed Trips - NYCT Bus |          2016|  98.81667| ACTUAL |
|   19| % of Completed Trips - NYCT Bus |          2017|  99.36000| TARGET |
|   20| % of Completed Trips - NYCT Bus |          2017|  99.11625| ACTUAL |
