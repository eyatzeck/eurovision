# Eurovision

How to win Eurovision

<img src="image.png" alt="drawing" width="60%"/>

# Business Problem 
If you are a broadcaster whose country participates in the Eurovision contest, it will be helpful to know factors that contribute to your country winning or not, some under your control, some not.  This analysis looks for those factors in Eurovision final results from 2013 to 2023.

This analysis looks at two possible factors:
* order of performance
* geographical bloc voting

Other questions that could have been answered with more data and more time might include:
* number of performers on stage
* color of costume
* repeat appearance of performer at Eurovision
* something about the actual songs!

So the question is:  what role do these factors play in the EV final results?

# Data Methods 
The definitive Eurovision data set is available here:  https://eschome.net/index.html

The site is designed to let the user request specific slices of data, which are returned in the form of an html page that shows the specified data in table form.  

The main ETL pipeline was comprised of python with pandas and matplotlib, along with Tableau:

1. use the Google Chrome "inspect" functionality to determine what POST commands to issue, to cause the eschome data to be visualized for scraping

2. using the python pandas .get_html() function, scrape the data from the html pages into useful dataframes 

3. save dataframe data in csv files for reuse to avoid re-scraping unnecessarily

4. build visualizations in python using built matplotlib to check various questions under the umbrella of "does order matter" and "do countries vote in blocs"

5. present the most important findings in a Tableau story which is available on Tableau public, and is also exported to PDF and available here for review.

Data dimensions about the participant countries were captured and massaged in an excel spreadsheet, from the following sources:
* Big Five countries:  https://eurovision.tv/
* Warsaw Pact countries:  https://en.wikipedia.org/wiki/Warsaw_Pact
* Countries belonging to the former USSR:  https://en.wikipedia.org/wiki/Republics_of_the_Soviet_Union
* Balkan countries:  https://en.wikipedia.org/wiki/Balkans
* Members of the European Union:  https://european-union.europa.eu/easy-read_en
* Nordic countries:  https://en.wikipedia.org/wiki/Nordic_countries
* Baltic countries:  https://en.wikipedia.org/wiki/Baltic_states
* Iberia:  https://en.wikipedia.org/wiki/Iberian_Peninsula

Data cleaning challenges included:
* Missing data, particularly for the case where some countries never actually voted for other countries -- required special handling in the web scraping code
* Missing semi-finals data for years prior to 2004.  This was handled by restricting the current inquiry to finals data only, but will be a limitation for further study which looks at semi-final voting.

# Results 

# Conclusion 
- include links to youtube and public data viz

# About Elena
* https://www.linkedin.com/in/eyatzeck/
* https://public.tableau.com/app/profile/elena.yatzeck/vizzes
* eyatzeck@gmail.com

# Background
The Eurovision Song Contest has been held annually for more than 60 years.  It is an internationally televised songwriting competition, organised by the European Broadcasting Union and featuring participants chosen by EBU member broadcasters representing their countries from across Europe and beyond.  (https://eurovision.tv/about/how-it-works)

## How it works
The contest consists of numerous dress rehearsals and culminates in two semi-finals and one final.  Full rules are here:  https://en.wikipedia.org/wiki/Rules_of_the_Eurovision_Song_Contest#:~:text=All%20remaining%20competing%20countries%20are,case%2025%20countries%20would%20compete

The "Big Five" and the host country automatically participate in the finals.  (Big Five:  France, Germany, Italy, Spain and the United Kingdom - the group of countries who via their broadcasters make the biggest financial contribution towards the organisation of the Contest.)  The remaining countries are assigned at random to one of two semi-finals.  Semi-final votes are all done by viewers via phone or the app.

For the final, there are 25 or 26 acts - 
* the host country of the contest and the "Big Five" countries automatically qualify 
* the top ten finishers from each semi-final also compete.  If the host country is in the big 5, that year only has 25 acts in the final.

## Finals voting rules
For the finals, the rules are:  

*In each show, after all songs have been performed, each country will give two sets of points (1, 2, 3, 4, 5, 6, 7, 8, 10 and 12) to their favourite songs; one set is given by a jury of five music industry professionals from that country, and one set given by viewers watching the show in country. Viewers can vote by telephone, SMS and through the official app.*

*Out of fairness, you cannot vote for your own country.*

*At the end of the Grand Final, the song that has received the most points wins the iconic trophy, and is performed once more. (Plus there are some tie-breaking rules)*

# Cool resources
Article about affinity voting from the BBC:  https://www.bbc.com/future/article/20230512-eurovision-why-some-countries-vote-for-each-other

Awesome Max Levites Tableau visualization:  https://public.tableau.com/app/profile/max.levites/viz/EveryEurovisionResultEver2021/TheUltimateEurovisionGuide2021

Reuters site:  https://www.reuters.com/graphics/MUSIC-EUROVISION/dwpkdykkzvm/

Some interesting facts and figures:  (https://eurovision.tv/about/facts-and-figures)

Study on impact of order effects plus round up of other data studies:  https://www.cambridge.org/core/journals/judgment-and-decision-making/article/order-effects-in-the-results-of-song-contests-evidence-from-the-eurovision-and-the-new-wave/C03D0D5AA384362736FE1EB59A75516C

Suggested way to reform the voting process:  https://www.electoral-reform.org.uk/time-for-a-key-change-how-we-would-reform-eurovision-voting/

# Needed to complete github structure:
* Jupyter Notebook containing your code
* Supporting scripts and data files in appropriate folders
* Pdf of your presentation

[DAP Checklist Here](dap_checklist.md)


