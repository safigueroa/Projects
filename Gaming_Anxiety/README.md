

# Overview

Over the last few years, especially during COVID-19 quarantine, the whole world has been plagued with more mental health issues than we've ever seen before. Almost an entire year of being locked up has dealt some serious damage to our anxiety, social phobia, and overall life satisfaction. One community, which we are members of, that has suffered greatly in regard to mental health is the gaming community. Having already displayed severe mental disorders and an infamous reputation of lacking social skills, the gaming community continues to struggle with these issues, which give rise to more serious behaviors such as addiction. It is important to remove the social stigma of mental health problems in order to assist those in need of rehabilitation and we believe that displaying the severity of our concerns is only the first step. Further than this, we can use big data to focus our attention on what we should be directing our very limited resources to and help prescribe this problem – not just the scale of the problem, but the root-cause and solution of it. Our expected outcome of this analysis is not only to achieve all of this, but to also gain insights to how we can halt the damage that's already been done and prevent more serious issues such as gaming addiction.

# Variable Descriptions

1. All 13,464 participants provided information about their **Demographics** including **Age** , **Gender** , and **country of birth / residence**.
2. **Platform** which means what do these participants game on? - Console (Ps4, Ps5, Xbox 1, Xbox 360) or PC (Qualitative)
3. **Game** - There are 11 games these participations can choose from (Qualitative)
4. **Workplace** – Are these participations working, unemployment, a student, a student and employed (Qualitative)
5. **Degree** – Are they graduated with a degree if so, this could include high school, bachelors, masters, PHD (Qualitative)
6. **Playstyle** – This would be the participant's preference of game: Multiplayer, Single player, Multiplayer-Online with Strangers, or Multiplayer with Friends (Qualitative)
7. **Why Play** – This would describe why these participants choose to game, for fun, to improve, to win. (Qualitative)
8. **Hours played** – How often these participants spend on gaming a day, per week (Quantitative)
9. **GAD-7 (The Generalized Anxiety Disorder)** – Was used to measure generalized anxiety rated on a 5-point scale comprised of seven items with the result being out of 0(no anxiety) to 21(severe anxiety).
10. **SWLS (The Life Satisfaction with Life Scale)** – Participants responded on the 7-point scale to 5 items indicating their agreement from "strongly disagree" to "strongly agree" The scale was designed to investigate subjective experience of well-being without respect to specific life domains such as health or employment status.
11. **SPIN (Social anxiety)** – These results are formed by a 17-item questionnaire. This variable measured specific symptoms such as (fear, avoidance, and physiologic arousal). This is measured on a 5-point scale:0("Not at all") , 1("A little bit"), 2 ("Somewhat"), 3 ("Very much") or 4 ("Extremely"). These scores are summed up and  interpreted as degree of social anxiety as follows: none (less than 20 points), mild (21-30 points), moderate (31-40 points), severe (41-50 points) and very severe (51 or more points)

12. **Narcissism** – Measured by the Single Item Narcissism Scale that has reasonable reliability, is significantly correlated with longer narcissism scales, and uncorrelated with self-esteem.

# Methods

We anticipate quite a bit of data cleaning on this dataset to meet our needs: exploratory data analysis, dimension reduction, and principal component analysis will be very useful here. Once we're satisfied with what we have, a predictive model such as linear regression will help anticipate any sudden increase of the included anxiety, social phobia, and life satisfaction (GAD-7, SPIN, SWL, and SINS) scores in relation to how much someone games (hours played) – any organization that fights for mental health rehabilitation will know where to look according to each test. Cluster analysis may also prove useful. To display the severity of the issue, we may need to apply some form of clustering analysis (k-means, silhouette, etc.). There may be no correlation between gaming and test scores, but overall life satisfaction may be at risk here. It is important to cluster the "unhealthy" gamers and apply data analysis methods to better show the risk of addiction and what it can lead to.
