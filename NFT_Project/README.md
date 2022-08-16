**Finding Value With NFT Utility**

_Research paper_

Roman Bravo, Cal Poly Pomona, United States, [romanbravo@cpp.edu](mailto:romanbravo@cpp.edu)

Erik Correa, Cal Poly Pomona, United States, [erikcorrea@cpp.edu](mailto:erikcorrea@cpp.edu)

Sergio A. Figueroa, Cal Poly Pomona, United States, [safigueroa@cpp.edu](mailto:safigueroa@cpp.edu)

Tallal M. Moshrif, Cal Poly Pomona, United States, [tmmoshrif@cpp.edu](mailto:tmmoshrif@cpp.edu)

**Abstract:**

_In 2021, Non-fungible tokens (NFT) became widely popular in online communities as individuals spent thousands of dollars to purchase these digital pieces of art. Many entrepreneurs gathered select teams of artists, computer programmers, marketers, and community managers to build NFT projects with the goal of selling these products to the highest bidders. As a result, the purchasers speculated on the value of these NFTs, purchasing them as investments, or gambling with them as get rich quick schemes. However, given all of this financial speculation, there is an ultimate question that becomes apparent: Is there a true value behind NFTs? In order to answer this question, we select 20 random NFT projects on rarity tools, and pre-process the project whitepapers for text mining purposes with the goal of searching for utility within these NFT projects. The objective is see if utility can be found within these NFT projects, and consequently describe this utility as a form of value for both investors and speculators of the NFT world._

_Keywords: Non-Fungible Token, NFT, Utility, Blockchain, Digital Art, Investing, Speculation, Metaverse, Web 3.0, Virtual Avatars, Cryptocurrency, Tokens, Collectibles, Smart Contracts._

**1 Introduction**

Non-Fungible tokens, or NFTs for short, are non-interchangeable units of data that are bought and sold through crypto currency. Every NFT is digital, and they represent real world objects like art, videos, moments, and audio. NFT's are unique and are considered to be one of ones, which establishes the reasoning for them to be non-interchangeable. While cryptocurrencies like Ethereum are equal to one another, NFTs can represent much more than that, thus creating a different value for each one. Each NFT is supported by a block chain. The blockchain is what provides a record of transactions that cannot be tampered with while at the same time keeping track of who owns what in the NFT space.

NFTs were created in 2014 but have become trendy and have grown in popularity over the past few years. In 2021, NFTs hit the mainstream, and the public awareness of them was at its peak. The digital artwork of NFT's have become a big appeal when buying NFT's, but there is much more to them that have led to some great questions about how NFT's can be taken further. While learning about them, we decided to take a deeper look and have asked the question, what utility do NFT'S provide that translate into value creation? Text mining is a great way to go about this question due to the amount of information that can be provided when looking at NFT's. Text mining is a great way to discover new information and in general it helps answer specific questions. Specifically, we used white papers from different NFT's in order to find our data.

**2 Background and Prior Research**

Prior to the text mining process, it was best to find further information that can help us with the question at hand. There are three articles that we used in order to gain a better understanding of how NFTs are valuable and how they offer utility.

The first of which is named "HOW NFTS CREATE VALUE," from the Harvard Business Review. It Specifically talks about how NFTs fundamentally changed the market for digital assets, creating the possibility for new types of transactions (Kaczynski, 2021; Kominers, 2021). It also discussed how to tell the difference between NFT's that are actually creating value and not just riding the hype (Kaczynski, 2021; Kominers, 2021).

The second article is named "How Do NFTs Add Value," from Martech Vibe. This article goes into details on how NFTs are Capable of creating unique brand experiences, increasing brand awareness, and encouraging customer engagement, which are all things that can create value. It goes over how they are usable, accessible, and recoverable (Chandni U,2021)

Our last article is named "The Growing Utility of NFTs," which is published by CoinDesk. The information involved in this article informs people on how NFT's can be used. We see that NFT's aren't just valuable because they are unique now, but because they can be used in other ways. An example from the article is that it talks about how video games are using NFT's as in game items, and how gaming companies are creating games that will be available on OpenSea (CoinDesk, 2021).

**3 Methodology and Dataset**

In order to find utility, and consequently value in NFT projects, white papers became the primary source of textual data for this project. The textual data itself contains various important information about the NFT project. This includes: The strategic intent of the project, the identities of individuals involved within the project, information about purchasing the project, the funding for the project, the future roadmap of the project, and solutions to business problems that the project is trying to solve (CoinTelegraph, 2022). Essentially, the whitepaper is a one-stop informative document that an investor reviews for specific project details and potential value.

The collection of this data began on Rarity.tools - a website that is dedicated to cataloging, ranking, and collecting various metrics of information about NFT projects. During the collection process, more than 800 NFT projects were reviewed, and the projects were randomly selected regardless of genre, or any quantitative metrics, and with the only prerequisite that the NFT project held a whitepaper. Of the 800 NFT that were reviewed, only 20 were selected for the purpose of this project.

The textual data within the white paper required preprocessing before undergoing data modeling. In order to pre-process the white papers a list variable named corpus was created. A loop was created that ran the length of the white paper column in our dataframe. The loop utilized the function of a regular expression to remove all non-word characters, numbers, empty spaces, single characters, and lowercase all words. The new string is then appended to the corpus list. The corpus list is later passed within a function that eliminates all 'stop words' from the documents. These 'stop words' are a combination of the most commonly used words in the English language involving determiners, coordinating conjunctions, and prepositions (Ganesan, 2021). Essentially, the 20 white papers have their textual data reduced to their purest form in order to determine their topics.

During the project there were several data limitations that we encountered. The first major issue is that white papers had awkward formatting. For example, white papers had text indentations, tables, graphics, bullet points, and lists that required manual formatting prior to placing this text into the spreadsheet. The second data limitation was the lack of white papers as it appeared that new projects began to phase these out for roadmaps instead. However, roadmaps were not suitable replacements for white papers. The issue with roadmaps is that they focused on quantitative metrics such as procuring a specific amount of partnerships per a given time period, or obtaining a certain user base to purchase their NFTs prior to a launch. Whereas white papers defined the strategic intent of the project, and therefore white papers became the superior textual data for the project.

In order to develop the model, the normalized corpus was taken, and a count vectorizer object was created. The count vectorizer took the most frequently used words in the white paper as a feature. 'Stop words' were ignored, and words that appeared in more than 60% of all documents and less than three times were also omitted—this allows us to focus on unique words to obtain a better set of features (Verma, 2020). The normalized corpus is then transformed and fitted to the count vectorizer object and a matrix is produced as its result. This matrix is then fitted and transformed to the latent Dirichlet allocation (LDA) model. Afterwards an LDA matrix is produced. Utilizing the components of the LDA model, a components matrix is produced that reveals the topic constituents for the respective topics. Finally, it becomes possible to identify the topic clusters.

**4 Analysis and Results**

The use of a latent Dirichlet allocation (LDA) model was implemented to best analyze our dataset (Sakar, 2019). This generative probabilistic model of a corpus results in latent topics, where each topic is formed by a distribution of words and their respective weights. In total, three distinct topics were formed after applying our normalized corpus to the aforementioned model. Using these three set clusters, a weighted average of floor prices for each category was used as a performance metric defined as follows:

![](images/weighted_avg.png)

The weighted floor price uses the average floor price of all nfts in that cluster and weight of volume, or the 90 day transaction of the nft. Since the nft market is so volatile, volume is a great metric of measuring the popularity of it (Kazczynski and Kominers, 2021). Due to the nature of this model no topic is strictly defined, however, using our best judgment and information provided from NFTs in each cluster, we were able to produce possible labels for each topic. These included: Collectibles as Topic 1, Utility as Topic 2, and Gaming as Topic 3. The results show a much higher weighted floor price (0.43 ETH) for Utility compared to Collectibles (0.13 ETH) and Gaming (0.29 ETH). It's also worth noting that the weighted floor price and volume for gaming NFTs is quite high.

| Topic Constituents for Topic 1 | Weighted Floor Price |
| --- | --- |
| ('assets', 91.00), ('users', 70.51), ('rock', 66.24), ('digital', 54.03), ('card', 49.07), ('tools', 48.31), ('wolf', 47.33), ('gaming', 44.43), ('company', 36.33), ('owners', 35.91), ('staking', 34.99) | 0.13 ETH |

| Topic Constituents for Topic 2 | Weighted Floor Price |
| --- | --- |
| ('dao', 116.35), ('coins', 53.34), ('icon', 42.33), ('users', 27.95), ('erc', 27.64), ('planet', 27.52), ('creators', 26.90), ('crypto', 26.33), ('discord', 25.88), ('ownership', 25.00), ('special', 24.31), ('set', 24.18), ('events', 23.18), ('reward', 20.33) | 0.42 ETH |

| Topic Constituents for Topic 3 | Weighted Floor Price |
| --- | --- |
| ('kingdom', 74.32), ('bots', 70.35), ('generation', 60.66), ('fighters', 58.30), ('genesis', 52.33), ('player', 47.35), ('weapons', 38.22), ('battle', 35.78), ('gameplay', 34.10), ('lands', 30.91), ('games', 30.27), ('resources', 29.11), ('rarity', 28.71) | 0.29 ETH |

**5 Discussion and Conclusion**

We started with the hypothesis that NFTs seeking a high sense of community would create more value to their owners and creators in other ways than floor price. In order to best visualize this analysis, an LDA model proved to be a best fit for our dataset. Our results have shown that the model used here proves that there is worth in these nfts that seek to provide utility. Potential investors can then look into these certain markets, not for the NFTs themselves, but the technology behind it: they are extremely difficult to counterfeit, and can tie royalty payments, credentials and tickets to them (Kazczynski and Kominers, 2021).

NFTs are still new and have huge potential for the future. Working on this particular topic was difficult due to the lack of information available but not impossible. It was interesting to gather raw data from different sources such as text files and white pages into a CSV file then clean it and process it using specific methods. According to Google Trend the word "NFT" has been researched the most by the end of 2021. The top 3 states looking for NFTs are California, Nevada and New Jersey. Low income and high income people buy NFTs for different reasons such as trading, collecting and long-term investment since they are considered by many as unique and artistic. Most of NFT's buyers are between 18 and 34 years looking to become rich as early Bitcoin investors. Text mining methods used in this project allowed us to understand why some NFTs are selling more than others and what characteristics buyers were specifically looking for while buying or researching into it.

**References**

Coindesk Staff (2021). _The Growing Utility of NFTs._ URL:

https://www.coindesk.com/sponsored-content/the-growing-utility-of-nfts/ (Visited on 1 March 2022).

CoinTelegraph (2022). _What is a Whitepaper? A Beginner's Guide on how to Format and Write_

_One._ URL: https://cointelegraph.com/funding-for-beginners/what-is-a-white-paper-a-beginners-guide-on-how-to-write-and-format-one (Visited on 2 March, 2022).

Sarkar, D. _Text Analytics with Python: A Practitioner's Guide to Natural Language Processing._

Ganesan, K. _What are Stop Words?_ URL: https://kavita-ganesan.com/what-are-stop-words/

(Visited on 2 March 2022).

U, C. (2021). _How do NFTs Add Value?_ URL:

https://martechvibe.com/martech/how-do-nfts-add-value/ (Visited on 1 March 2022).

Kazczynski, S. and S. D. Kominers. _How NFTs Create Value_. URL:

https://hbr.org/2021/11/how-nfts-create-value (Visited on 1 March 2022).

Verma, K. _Using Count Vectorizer to Extract Features from Text._ URL:

https://www.geeksforgeeks.org/using-countvectorizer-to-extracting-features-from-text/

(Visited on 2 March 2022).
