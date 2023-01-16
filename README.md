
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
        <li><a href="#11---bars-shot-ontarget)">11 -Bar , Shots (On target %)</a></li>
        <li><a href="#03---expected-goals-modelling">03 - Expected Goals Modelling</a></li>
        <li><a href="#04---automated-match-reporting">04 - Automated Match Reporting</a></li>
        <li><a href="#05---automated-competition-reporting">05 - Automated Competition Reporting</a></li>
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
    │ 
    ├── .gitignore 
    │     
    ├── LICENSE 
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


**Summary**: Use Fbref data to plot bars of shots taken by the 20 Premier League clubs in a season. Also shown is the percentage of shots on target. Good teams take a high no of shots and have a good percentage of them on target. Not a decisive measure of a team's attacking prowess but still
**Summary:** Scrape team and player market value information from transfermarkt.co.uk. This work includes the development of a "scouting tool" that highlights players from a given league that have a favourable combination of Age and Goal Contribution per £m market value. The work also explores the use of statistical models to predict market value based on player performance, as well as identifies teams that under and over-performed (league position) based on squad value.

<p align="center">
  <img width="25%" src="./data_directory/misc_data/images/GB2_player_value_regression.png"> &nbsp &nbsp
  <img width="25%" src="./data_directory/misc_data/images/GB2_player_scouting.png"> &nbsp &nbsp
  <img width="25%" src="./data_directory/misc_data/images/GB2_value_league_table.png">
</p>

### 03 - Expected Goals Modelling

**Summary:** Implementation and testing of basic expected goals probabilistic models. This work includes development and comparison of a logistic regression expected goals model and a neural network expected goals model, each trained off over 40000 shots taken across Europe's 'big five' leagues during the 2017/2018 season. The models are used to calculated expected goals for specific players, clubs and leagues over a specified time period.

<p align="center">
  <img width="35%" src="./data_directory/misc_data/images/xg_log_regression_model.png"> &nbsp &nbsp
  <img width="35%" src="./data_directory/misc_data/images/xg_neural_network.png"> &nbsp &nbsp
</p>
<p align="center">
  <img width="25%" src="./data_directory/misc_data/images/EPL-2017-Salah-Shotmap.png"> &nbsp &nbsp
  <img width="25%" src="./data_directory/misc_data/images/EPL-2017-Liverpool-Shotmap.png"> &nbsp &nbsp
  <img width="25%" src="./data_directory/misc_data/images/Bundesliga-2017-All-Shotmap.png"> &nbsp &nbsp
</p>


### 04 - Automated Match Reporting

**Summary:** Development of automated scripts to produce match reports immediately after a match has concluded. This work includes collection and processing of public-domain match event data, and the production of multiple visuals that together constitute informative and appealing match reports. Visuals currently include shot maps, inter-zone passflows, pass plots and offensive action convex hulls.

<p align="center">
  <img width="35%" src="./data_directory/misc_data/images/EPL-2022-08-06-Tottenham-Southampton.png"> &nbsp &nbsp
  <img width="35%" src="./data_directory/misc_data/images/EPL-2022-08-07-Manchester%20United-Brighton.png"> &nbsp &nbsp
</p>
<p align="center">
  <img width="25%" src="./data_directory/misc_data/images/EPL-1640700-Manchester United-Liverpool-passhulls.png"> &nbsp &nbsp
  <img width="29.55%" src="./data_directory/misc_data/images/EPL-1640709-Liverpool-Bournemouth-passreport_Liverpool.png"> &nbsp &nbsp
</p>

### 05 - Automated Competition Reporting

**Summary:** Development of automated scripts to produce competition reports and multi-match player evaluations at any point throughout a competition. This work includes collection and processing of public-domain match event data, and the production of multiple visuals that generate novel and meaningful insight at a team and player level. Visuals currently include an assessment of progressive passes, defensive actions and penalty placement.

<p align="center">
  <img width="32%" src="./data_directory/misc_data/images/EPL-2021-top-defensive-actions-per-100-opposition-passes-in-that-third.png"> &nbsp &nbsp 
  <img width="32%" src="./data_directory/misc_data/images/europe5-top-pen-takers-2019-2022.png">
</p>
<p align="center">
  <img width="24%" src="./data_directory/misc_data/images/EPL-2022-defensive-contributions-player-variant.png"> &nbsp &nbsp 
  <img width="24%" src="./data_directory/misc_data/images/EPL-2022-opposition-half-passers-player-variant.png">
</p>
