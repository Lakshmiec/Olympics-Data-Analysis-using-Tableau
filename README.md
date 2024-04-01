# Olympics-Data-Analysis-using-Tableau
 
**Tableau Link:** [Link](https://public.tableau.com/views/TheWinterOlympics1924-2018_17117163336280/MedalDistribution?:language=en-GB&:sid=&:display_count=n&:origin=viz_share_link)

## Introduction

The Winter Olympics, held every four years, stand as a testament to human athleticism, endurance, and sportsmanship amidst the icy challenges of winter sports. But beyond the excitement, lies a treasure trove of data waiting to be explored. This analysis delves into Winter Olympics data from 1924 to 2018, aiming to uncover fascinating trends and answer intriguing questions. We'll utilize the power of the Tableau visualization tool to uncover the story hidden within the numbers, exploring everything from the evolution of participating nations to the rise of winter sports popularity and also exploring how the number of events has transformed over time, witness the rise of dominant winter sports, and potentially even track the evolution of gender participation in these prestigious games.

## Dataset

**Data Origin:** The dataset used in this analysis is the Winter Olympics (1924 - 2018) dataset sourced from Kaggle. [Winter Olympics Dataset]([Link](https://www.kaggle.com/datasets/leminhnguyen/winter-olympics-1924-2018?select=olympic_events.csv)

**Dataset Contents:** We are exploring two complementary datasets chronicling the Winter Olympics from 1924 to 2018:

1. **Olympic_events Dataset:** This dataset acts as a high-level overview, providing details like event names, locations, and total participants for each Olympic event.

2. **Events_medals Dataset:** This dataset dives deeper, revealing the countries that have claimed Olympic glory by winning medals and the number of medals awarded.

I chose this dataset because the Winter Olympics is a global phenomenon, bringing together athletes from around the world. These datasets allow us to delve into which countries have consistently dominated the games, how medal distribution has shifted over time, and potentially identify rising stars in the Winter Olympic landscape. This dataset spans almost a century, offering a unique opportunity to analyze the evolution of the Winter Olympics.

## Features

The datasets contain the following features:

### Olympic_events Dataset

| Feature Name  | Description                          | Data Type   |
|---------------|--------------------------------------|-------------|
| event_country | The country in which the event took place | Qualitative |
| event_year    | The year the event took place       | Quantitative|
| n_participants| Number of athletes at the event      | Quantitative|
| n_countries  | Number of countries participated    | Quantitative|
| n_medals      | Number of medals given out          | Quantitative|

### Events_medals Dataset

| Feature Name  | Description                          | Data Type   |
|---------------|--------------------------------------|-------------|
| event_year    | The year the event took place       | Quantitative|
| country       | The country that won at least 1 medal | Qualitative, Nominal |
| gold          | Number of gold medals won by the country | Qualitative, Ordinal |
| silver        | Number of silver medals won by the country | Quantitative |
| bronze        | Number of bronze medals won by the country | Quantitative |
| total         | Number of total medals won by the country | Quantitative |

## Purpose of Visualization

The purpose of these given visualizations is to uncover valuable insights into medal distributions, participation dynamics, and the impact of hosting the Winter Olympics on participating countries. They are described in detail below.

### Medal Distribution by Category for Each Country in the Winter Olympics using Stacked Chart

This visualization aims to provide a comprehensive overview of how medals are distributed among different categories (gold, silver, bronze) for each participating country.

### Participation Count in Hosted Countries During the Winter Olympics using Geographical Map

This visualization aims to visualize the participation count in countries that have hosted the Winter Olympics, providing insights into the impact of hosting on participant numbers.

### Comparison of Disciplines and Medals Over Time in the Winter Olympics using Line Chart

This visualization aims to visualize and compare the trends of the number of disciplines competed and the number of medals awarded over different editions of the Winter Olympics. And analyze the overall growth and development of the Winter Olympics in terms of both participation and recognition of achievements across various sports disciplines.

Some of the queries we aim to address include:

- Which countries tend to dominate in specific medal categories?
- Which hosted country has the most participation count in the Winter Olympics?
- Is there a correlation between the number of disciplines and the number of medals awarded?

## Visualization

### Stacked Chart showing Medal Distribution by Category for Each Country in the Winter Olympics

![Figure 1.1](Path_to_image_file)

#### Visual Encoding used in the Stacked Chart in Figure 1.1

| Data         | Data Type    | Encoding   | Description                                    |
|--------------|--------------|------------|------------------------------------------------|
| Total Medals | Quantitative | Bar height | The height of the bar represents the total number of medals won in that category. |
| Medal category | Qualitative | Hue        | The color of the bar represents the medal category (Gold: Yellow, Silver: Grey, Bronze: Brown). |
| Country      | Qualitative  | Text label on X-axis | Text labels on the x-axis identify the country (United States) |

**Insights & Findings:** 

The chart shows that Norway has emerged as the most successful nation in the history of the Winter Olympic Games, accumulating a remarkable total of 368 medals since the inaugural event in 1924. These medals consist of 132 gold, 125 silver, and 111 bronze. It is particularly noteworthy that Norway achieved this impressive feat despite its relatively small population of just over five million inhabitants. In terms of overall medal count, the United States holds the second position, having secured 105 gold, 112 silver, and 88 bronze medals.

### Geographical Map showing participation count in hosted countries during the Winter Olympics

![Figure 1.2](Path_to_image_file)

#### Visual Encoding used in the Geo Map in Figure 1.2

| Data         | Data Type    | Encoding   | Description                                    |
|--------------|--------------|------------|------------------------------------------------|
| Country      | Categorical  | Color      | The color distinguishes different hosted countries with their participation count. |

**Insights & Findings:**

Among the countries that have hosted the Winter Olympics, the United States has the highest participation count, with 4387 participants. This might be due to the country's historical performance in Winter Olympic sports or government funding for athlete training programs. On the other hand, Germany has the lowest participation count among the hosted countries, with only 669 participants. These numbers reflect the varying levels of involvement and representation of countries when they host the Winter Olympics.

### Line Chart for Comparison of Disciplines and Medals Over Time in the Winter Olympics

![Figure 1.3](Path_to_image_file)

#### Visual Encoding used in the Line plot in Figure 1.3

| Data                | Data Type    | Encoding   | Description                                    |
|---------------------|--------------|------------|------------------------------------------------|
| Number of Disciplines| Quantitative | Line Position(Y axis) | The height of the blue line on the Y-axis represents the number of disciplines offered in that particular Winter Olympics year. |
| Total Medals        | Quantitative | Line Position(Y axis) | The height of the orange line on the Y-axis represents the total number of medals awarded in that particular Winter Olympics year. |
| Event Year          | Quantitative | Position(X-axis) | Each tick mark along the X-axis represents a specific year of the Winter Olympics. The years increase from left to right. |
| Text labels         | Nominal      | Color      | The blue line represents the number of disciplines and the brown line represents the total medals awarded. |

**Insights & Findings:**

The graph shows an upward trend in both the number of disciplines and medals awarded over time. This indicated that the Winter Olympics have grown in complexity and scale over the years, potentially offering more opportunities for athletes to compete and win medals.

## Query Answers

**Query 1:** Which countries tend to dominate in specific medal categories? [Figure 1.1]

The graph in Figure 1.1 shows that Norway has won most of the medals (Gold, Silver, Bronze). Followed by the United States.

**Query 2:** Which hosted country has the most participation count in the Winter Olympics? [Figure 1.2]

Figure 1.2 shows that the United States has the most participation count (4387) in the Winter Olympics.

**Query 3:** Is there a correlation between the number of disciplines and the number of medals awarded? [Figure 1.3]

Yes, based on the graph provided in Figure 1.3, there appears to be a correlation between the number of disciplines and the number of medals awarded in the Winter Olympics. The overall upward trend in both the number of disciplines and medals suggests a positive relationship between these variables. As the number of disciplines increases over time, more medals are likely awarded to accommodate the growing number of events and athletes participating in the Winter Olympics.
