
#### - Scraping Data From Understat : Get xG data from understat website as pandas dataframe by entering match id(from understat) , x and y locations of shots also included
#### -  9 xG Lollipop : Using xG data from understat, create a xG timeline for both teams in a lollipop style
#### - 11 - Bar,Shots(On target %) : Bar charts to show shots by each team and on target %
#### - 16 xGOT Table, create a table to show xGOT and goals scored
#### - 22 Show timeline on when Arsenal have scored thier goals this season
#### - 26 Create Pizza Plots using MPL soccer 


# Football Data Analytics
Collection of my football data analytics work that I showcase on twitter
Most of the code and concepts that I have learned in this field has been from the amazing resources provided by the analytics community


## Contents

<details open="open">
  <summary>Table of Contents</summary>
  <ol>
    <li><a href="#introduction"> ➤ Introduction</a></li>
    <li><a href="#folder-structure"> ➤ Folder Structure</a></li>
    <li><a href="#workflow"> ➤ Workflow</a></li>
    <li>
      <a href="#projects"> ➤ Projects</a>
      <ul>
        <li><a href="#11---bars-shot-on-target">11 -Bar , Shots (On target %)</a></li>
        <li><a href="#13---xG-vS-g">13-xG VS G</a></li>
        <li><a href="#18---touch-locations">18- Touch Locations</a></li>
        <li><a href="#22---goals-timeline">22-Goals Timeline</a></li>
        <li><a href="#23---long-goalkicks">23- % Long Goalkicks</a></li>
        <li><a href="#42---sOT">42-SOT</a></li>
        <li><a href="#9---xG-lollipop">9-xG Lollipop</a></li>
      </ul>
    </li>
  </ol>
</details>

## Introduction
This repository contains a projects that are used to generate posts for my Twitter Account.Python is used for extraction,scraping,data pre-processing, analysis and visualisation. Libraries used are beautiful soup,matplotlib,pandas etc. These mini projects have helped me to understand data better and apply it to my field of interest which is Football. Check out my Twitter [(@Ligandro22_)](https://twitter.com/Ligandro22).


## Folder Structure

    Football-Viz-for-Twitter
    │
    ├── Projects
    │   ├── 11-Bar , Shots (On target %).ipynb
    |   ├── 13-xG VS G.ipynb
    |   ├── 18- Touch Locations.ipynb
    |   ├── 22-Goals Timeline.ipynb
    |   ├── 23- % Long Goalkicks .ipynb
    |   ├── 34-xT 2.ipynb
    |   ├── 42-SOT.ipynb
    |   ├── 9-xG Lollipop.ipynb
    │ 
    │ 
    ├── README.md 

## Workflow

As shown in the folder structure above, the repository contains three key folders:
- **data_directory**: Storage of raw football data used for projects.
- **analysis_tools**: Custom python package containing modules that support football data import, processing, manipulation and visualisation.
- **projects**: Series of projects that cover various elements of football data analytics. Also contains any template scripts used to import raw data from various football data APIs, websites or data services.

In general, each project follows a number of logical steps:
1. Create a folder within the Projects area to store files associated with the project.
2. Use analysis_tools package: get_football_data module [note this module is not available within the git repo] to import raw data from football data API, website or data service:
    * If imported dataset is large, save to data_directory area in compressed BZ2 format and create a new script for analysis.
    * If imported dataset is small, data import and analysis can be completed in the same script (without the need to store/save data).
3. Within the analysis script, import any required modules from the analysis_tools package.
4. Pre-process and format data using data_engineering modules within the analysis_tools package.
5. Synthesise additional information using custom_events and pitch_zones modules within the analysis_tools package.
6. With data formatted appropriately, create visuals and generate insight for end-consumer.

## Projects

Project table of contents: <br>
&nbsp; &nbsp; [01 - World Cup 2018 Box to Box Midfielder Analysis](#01---world-cup-2018-box-to-box-midfielder-analysis) <br>
&nbsp; &nbsp; [02 - Transfermarkt Web-Scrape and Analyse](#02---transfermarkt-web-scrape-and-analyse) <br>
&nbsp; &nbsp; [03 - Expected Goals Modelling](#03---expected-goals-modelling) <br>
&nbsp; &nbsp; [04 - Automated Match Reporting](#04---automated-match-reporting) <br>
&nbsp; &nbsp; [05 - Automated Competition Reporting](#05---automated-competition-reporting)


### 11 - Bars Shot On Target


**Summary**: Use Fbref data to plot bars of shots taken by the 20 Premier League clubs in a season. Also shown is the percentage of shots on target. Good teams take a high no of shots and have a good percentage of them on target. Not a decisive measure of a team's attacking prowess but still provides a good statistical view.


<p align="center">
  <img width="25%" src="./data_directory/misc_data/images/GB2_player_value_regression.png"> &nbsp &nbsp
  <img width="25%" src="./data_directory/misc_data/images/GB2_player_scouting.png"> &nbsp &nbsp
  <img width="25%" src="./data_directory/misc_data/images/GB2_value_league_table.png">
</p>

### 13 - xG VS G
**Summary:** Scrape team shooting data from Fbref.com . Get xG,xGA,Goals Scored and Goals Conceded for the 20 Premier League Teams.xG and xGA are expected goals scored and expected goals conceded respectively. Comparing these two metrics with actual goals scored and conceded gives a performance measure of teams in the league. If the team scored more goals than expected it is said to be performing well. If less goals are conceded than expected then it is said to be performing better too. 

<p align="center">
  <img width="35%" src="./data_directory/misc_data/images/xg_log_regression_model.png"> &nbsp &nbsp
  <img width="35%" src="./data_directory/misc_data/images/xg_neural_network.png"> &nbsp &nbsp
</p>
<p align="center">
  <img width="25%" src="./data_directory/misc_data/images/EPL-2017-Salah-Shotmap.png"> &nbsp &nbsp
  <img width="25%" src="./data_directory/misc_data/images/EPL-2017-Liverpool-Shotmap.png"> &nbsp &nbsp
  <img width="25%" src="./data_directory/misc_data/images/Bundesliga-2017-All-Shotmap.png"> &nbsp &nbsp
</p>


### 18 - Touch Locations

**Summary:** Scrape touches data from Fbref. Get total touches in final 3rd,Mid 3rd and Defensive 3rd for all 20 Premier League teams. Plot the numbers on mplsoccer pitch. Denote pitch areas by colour and annotate touches.


<p align="center">
  <img width="35%" src="./data_directory/misc_data/images/EPL-2022-08-06-Tottenham-Southampton.png"> &nbsp &nbsp
  <img width="35%" src="./data_directory/misc_data/images/EPL-2022-08-07-Manchester%20United-Brighton.png"> &nbsp &nbsp
</p>
<p align="center">
  <img width="25%" src="./data_directory/misc_data/images/EPL-1640700-Manchester United-Liverpool-passhulls.png"> &nbsp &nbsp
  <img width="29.55%" src="./data_directory/misc_data/images/EPL-1640709-Liverpool-Bournemouth-passreport_Liverpool.png"> &nbsp &nbsp
</p>

### 22 - Goals Timeline

**Summary:** Get Arsenal Team Data from Understat and plot no of goals scored and conceded distributed over the 90mins divided into 15 min brackets.
This helps us see when Arsenal tend to scored and concede during a time period in a match.

<p align="center">
  <img width="32%" src="./data_directory/misc_data/images/EPL-2021-top-defensive-actions-per-100-opposition-passes-in-that-third.png"> &nbsp &nbsp 
  <img width="32%" src="./data_directory/misc_data/images/europe5-top-pen-takers-2019-2022.png">
</p>
<p align="center">
  <img width="24%" src="./data_directory/misc_data/images/EPL-2022-defensive-contributions-player-variant.png"> &nbsp &nbsp 
  <img width="24%" src="./data_directory/misc_data/images/EPL-2022-opposition-half-passers-player-variant.png">
</p>


### 23 - Long Goalkicks

**Summary:** Plot bars of the percentage of long goalkicks taken by each team in the Premier League.Helps us get an insight on how teams tend to build up play.

<p align="center">
  <img width="32%" src="./data_directory/misc_data/images/EPL-2021-top-defensive-actions-per-100-opposition-passes-in-that-third.png"> &nbsp &nbsp 
  <img width="32%" src="./data_directory/misc_data/images/europe5-top-pen-takers-2019-2022.png">
</p>
<p align="center">
  <img width="24%" src="./data_directory/misc_data/images/EPL-2022-defensive-contributions-player-variant.png"> &nbsp &nbsp 
  <img width="24%" src="./data_directory/misc_data/images/EPL-2022-opposition-half-passers-player-variant.png">
</p>

### 42 - SOT

**Summary:** Compare Shots on Target taken and conceded by teams in the Premier League using scatter plot.Good teams take SOT Taken and concede less SOT 

<p align="center">
  <img width="32%" src="./data_directory/misc_data/images/EPL-2021-top-defensive-actions-per-100-opposition-passes-in-that-third.png"> &nbsp &nbsp 
  <img width="32%" src="./data_directory/misc_data/images/europe5-top-pen-takers-2019-2022.png">
</p>
<p align="center">
  <img width="24%" src="./data_directory/misc_data/images/EPL-2022-defensive-contributions-player-variant.png"> &nbsp &nbsp 
  <img width="24%" src="./data_directory/misc_data/images/EPL-2022-opposition-half-passers-player-variant.png">
</p>

### 9 - xG Lollipop

**Summary:** Plot shots taken in a match and xG of each shot accoring to time in match. Helps us see when teams are dominating in attack in a time period in match.
<p align="center">
  <img width="32%" src="./data_directory/misc_data/images/EPL-2021-top-defensive-actions-per-100-opposition-passes-in-that-third.png"> &nbsp &nbsp 
  <img width="32%" src="./data_directory/misc_data/images/europe5-top-pen-takers-2019-2022.png">
</p>
<p align="center">
  <img width="24%" src="./data_directory/misc_data/images/EPL-2022-defensive-contributions-player-variant.png"> &nbsp &nbsp 
  <img width="24%" src="./data_directory/misc_data/images/EPL-2022-opposition-half-passers-player-variant.png">
</p>
