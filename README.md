# Public Relations Council as a Service
Public Relations Council as a Service

- Dustan Curtis, Athabasca University
- July 17, 2017
- Version: 0.2.1, release candidate
- TRUTH SEEKERS: http://bit.ly/2uTacmk

For Aaron (heart), Ed (foresight), and all those yet to display courage in the face of tyranny.

> If you tell a lie big enough and keep repeating it, people will eventually come to believe it. The lie can be maintained only for such time as the State can shield the people from the political, economic and/or military consequences of the lie. It thus becomes vitally important for the State to use all of its powers to repress dissent, for the truth is the mortal enemy of the lie, and thus by extension, the truth is the greatest enemy of the State."

— JOSEPH GOEBELLS

## Abstract
This paper introduces a novel concept for manipulating conversation at scale by way of a big social data system termed the "Public Relations Council as a Service" (PRCaaS). By combining psychometric profiling models with machine reinforcement learning techniques and cloud services, it becomes possible to engineer a self-reinforcing propaganda system that learns and generates propaganda directly from a target population's event and communication data (their "digital footprint"). As the volume of propaganda generation and delivery increases it becomes possible to control the conversation across digital social platforms. The combination of services, agents, and datastores that make up the system are detailed and sample code for the propaganda engine is provided. Given that effective propaganda drives real-world actions, the result of the well-implemented PRCaaS is the ability to manipulate real outcomes within a population towards a specific goal. Through proper preparation and implementation, the resulting service provides a faithfully automated version of Edward Bernays's Public Relations Council (Bernays, 2011), albeit adopted for the digital age. Finally, given the availability of this technology, the text briefly examines potential population scale manipulations that could result from the well-implemented system.

**Keywords**: computational propaganda, big social data, propaganda engine

## 1. Digital Footprint Data as Foundation
Machine-based psychometric analysis techniques are increasingly accurate at analyzing and predicting real-world personality traits based on digital footprints (Kosinski, Wang et al., 2016) and other big social data (see: Zuboff, 2015). There are a multitude of sources for human behavioural data through acquisition from public and private data sources. I consider public sources to include anything a corporation can legally acquire on its own or from a third-party aggregator. Examples of public sources are browsing history, geo-location data, tracking cookies, public social data, ad network data, search trends, news media, and visits to public websites. Private sources include voting records, incarceration records, political mailing lists, deed and property sales, CRM data, automotive sales records, credit card and purchase histories, credit reports, medical records, Amazon and other online purchases, income level, and social conversation data. Linking of these previously disparate big social data sets beyond the Facebook and Twitter aggregation techniques employed in (Leskovec & Krevl, 2014; Kosinski, Matz, et al., 2015; Eichstaedt et al., 2015) is achieved by employing symbolic contact chaining (Segal et al., 2016) and set intersection with edge reduction (Segal et al., 2014 ; Veiga & Eichhoff, 2016), not unlike the MAINWAY (GET CITE - check program) program of the National Security Agency (NSA) (Risen & Poitras, 2013). In unifying big social data from disparate sources, the resulting user-footprint matrices are necessarily more accurate since they contain more accurate behavioural event data as input. Increasingly accurate behavioural data gleaned on a population can be used to enhance the quality of psychographic and other models built on that population (Kosinski et al., 2013), and thus any dependent algorithms downstream.

**Figure 1:** *Public and private data sources available for scraping of digital footprint data.*

Services built upon this digital footprint data have long been a boon for corporations who serve targeted advertisements or otherwise profile their users and use the collected data for profit (Levy, 2009; Lavalle et al., 2011; Schmarzo, 2014). Peter Thiel's concept of "Creative Monopoly" reflects the notion that these behavioural data flows, often measured simply as "active daily users", often represent the long term profit model for these companies (Thiel, 2014). Companies are incentivized - indeed now required, due to competition - to engineer addictive systems by design (Eyal, 2014) in order to increase data breath and quality of big social data inflows. Literal metrics for success include retention, average session length, number of engagements, or simply "addictiveness". Product features are increasingly prioritized towards increasing inflows of this valuable behavioural data and the mining of human capital, rather than driving value for the user (Zuboff, 2016). This is because all internet communications are now monetizable as a unit of the surveillance economy, whether for corporate, educational, or government use. The marketplace is dominated by a few large players, termed "surveillance intermediaries" (see: Rozenshtein, 2017) for their ubiquity, that aim to fill the role of monopolist over various flows of human data, including text, audio, and video content. These end-flow aggregators (EFAs) will get your data, eventually, through some avenue or another. Besides merely collecting data for profit, the PRCaaS as EFA shows that data obtained from a population can be used to derive targeted propaganda in similarity to that population. This is because the real-world results on a population of decades of internet and electronic device use is taking many of the same forms as drug addiction: We are literally addicted to the machines (Alter, 2017). Social networks have long manipulated social feeds in pursuit of increased engagement and understanding of user habits (Kramer et. al., 2014). That is, they employ models over user data to manipulate existing users' behaviour and increase user acquisition, to great success. Facebook has supplemented organic user data with purchased data from data brokers since at least 2012 (Angwin et al., 2016).

## 2. The PRCaaS System & Components
Built upon this valuable behavioural data, the PRCaaS is a distributed system that aims to automate all aspects of data collection and propaganda generation towards a given population for a given campaign across all desired mediums of communication. This paper aims to provide a general design for a PRCaaS while recognizing that specific mediums may require alternate approaches. Components of the system, modeled as microservices, are: 1. Monitoring, 2. Profiling, 3. Modeling, 4. Propaganda Generation, 5. Delivery, and 6. Visualization & Administration. These services represent the general architecture of a PRCaaS as data acquisition, processing, modification and delivery pipeline with multiple interactive cycles (see: Appendix A). The digital footprint data represents the training data for building psychometric models and extracting a datastore of mined human sentences for propaganda generation (see: 2.2.3. Human Sentence Extraction & "/data/sentence_templates.csv"). In this approach, human conversation data is used as the basis for generated propaganda, which then undergoes substitution, transformations, and knockout for diversity and humanization of messaging. Derived messaging is then compared to source and target groups to prove its similarity (to test) and uniqueness (to the global set of messages). After delivery, message uptake and engagement is measured and the propaganda tweaked to achieve a self-reinforcing feedback loop for propaganda generation and delivery. Well performing propaganda pieces are boosted and remixed, while bad performers are throttled or even erased entirely. Ongoing management is needed to keep the models and data fresh, since the system uses live human feedback to plan future actions of manipulation and to expand its vocabulary. If public mood shifts, the PRCaaS must identify the shift, update profiles and models, and then generate and deliver targeted propaganda to influence population-level outcomes towards that goal. By using scalable and component-based microservices in a public cloud, the system can achieve maximum scalability in order to analyze and manipulate massive populations beyond 200,000,000 persons (Grasseger & Krogerus, 2017; O'Sullivan, 2017). Amalgamation of population-level datasets is inherently the best baseline, both to measure the accuracy of drawn samples against the entire population and as "one true source" for contact chaining operations.

**Figure 2:** *High-level architectural components with source data and target mediums.*

### 2.1. Monitoring Service
The initial and ongoing collection of population-level event data is essential to the understanding and manipulation of outcomes within that population. Monitoring agents act as platform- or medium-specific sensors, pulling in digital footprint data on a population as event-based streams of behavioural data. Any public and private sources of digital footprint data can be monitored once or on an ongoing basis depending on financial resources available and technical constraints imposed by surveillance intermediaries. Monitoring operates under two phases: An initial pass to gather digital footprint data on the entire population and to segment the target population; followed by ongoing monitoring of only the target population and a control group from the general population. This is because monitoring is not merely a one-off exercise. As propaganda messages are introduced to the population, the Monitoring service measures feedback of both the pulse of the conversation and of individual actors within it. Weights can be assigned to individual actors or groups to achieve better coverage and lower monitoring costs. Consider the monitoring agent as similar to Google's web crawling technology, albeit adopted to bring in private, non-voluntarily disclosed data as well. Tools and methodologies for scraping and aggregating big social data are mature and diverse (see: Batrinca & Treleaven, 2015). The importance of this behavioural data is that, when employed correctly, it is possible achieve a fundamentally higher level of behavioural understanding than from human analysis alone on the same dataset (Youyou et al., 2015).  Agents might have a broad purpose (e.g. interpret flow of conversation about Coke vs. Pepsi) or a very specific one (e.g. monitor the public Facebook conversations for negative mentions about Pepsi for people living in Michigan).

Despite their position as information brokers, big social networks are regulated and bound by government restrictions as far as collection of personal-level data not voluntarily disclosed by its owner (Kosseff, 2017). Google's illegal collection of unencrypted Wi-Fi traffic containing personal identifiers (see: Franzen, 2013) provides the ideal analogy to the monitoring approach for the PRCaaS: Corporations face virtually no barriers to the mass collection of publicly available data, the penalties are lax, so "collect first and apologize later". The effect of one billion-plus Android phones regularly reporting their cellular, GPS, and Wi-Fi locations home to Google raises no concerns because users implicitly opt-in to data sharing by using Google's operating system. Somewhat ironically, Google, the company largely based on systematically scraping data from others, has a terms of service that explicitly forbids scraping and appropriation of its content that it appropriates and scrapes from others (Google, 2017). The PRCaaS takes this same approach to indignant aggregation, but instead scrapes multiple surveillance intermediaries directly and then supplements with additional datasets from data brokers. When executed correctly, the resulting PRCaaS dataset actually becomes more authoritative than any other aggregate source on that population, including the surveillance intermediary who operates within the confines of strictly lawful data aggregation techniques. Notably, most federal surveillance agencies do not operate within the confines of lawful data acquisition and are perhaps original architects of the class of PRCaaS system, albeit lacking in generative propaganda.

## References
Alter, A. L. (2017). Irresistible: The rise of addictive technology and the business of keeping us hooked. New York: Penguin Press.

Angwin, J., Parris, T., & Mattu, S. (2016, December 27). Facebook doesn't tell users everything it really knows about them. ProPublica. Retrieved from: https://www.propublica.org/article/facebook-doesnt-tell-users-everything-it-really-knows-about-them

Batrinca, B., & Treleaven, P. C. (2015). Social media analytics: A survey of techniques, tools and platforms. AI & SOCIETY, 30(1), 89-116.

Bernays, E. (2011). Crystallizing public opinion. Brooklyn, N.Y: Ig Publishing. Reprint.

Bickert, M. (2017, June 15). Hard questions: How we counter terrorism. Facebook. Facebook Newsroom. Retrieved from: https://newsroom.fb.com/news/2017/06/how-we-counter-terrorism/

Brunton, F. (2013). Spam: A shadow history of the Internet. MIT Press.

Chapman, B. (2017, June 22). Facebook and Google losing hundreds of millions of pounds of advertising because of extremist videos. The Independent. Retrieved from: http://www.independent.co.uk/news/business/news/facebook-google-extremist-videos-advertising-money-isis-kkk-a7802516.html

Chomsky, N. (1998). On language: Chomsky's classic works ‘Language and Responsibility’ and ‘Reflections on Language’ in one volume. New York, N.Y.: New Press.

Coleman, G. (2014). Hacker, hoaxer, whistleblower, spy: The many faces of Anonymous. Verso Books.

Davis, C., Varol, E., Ferrara, E., Flammini, A., & Menczer, F. (2016). BotOrNot: A system to evaluate social bots. In Proceedings of the 25th International Conference Companion on World Wide Web (pp. 273–274). New York, NY: Association for Computing Machinery (International World Wide Web Conferences Steering Committee). doi:10.1145/2872518.2889302

Duan, Y. et al. (2017). One-shot imitation learning. arXiv preprint arXiv:1703.07326.

Eichstaedt, J. C., Schwartz, H. A., Kern, M. L., Park, G., Labarthe, D. R., Merchant, R. M., Seligman, M. E. P. (2015). Psychological language on Twitter predicts county-level heart disease mortality. Psychological Science, 26, 159–169. http://dx.doi.org/10.1177/0956797614557867

Eyal, N. (2014). Hooked: How to build habit-forming products. Penguin.

Franzen, C. (2013, March 8). Google reportedly nears $7 million settlement with states over Street View privacy violations. The Verge. Retrieved from: https://www.theverge.com/2013/3/8/4080230/google-nears-settlement-states-street-view-wi-fi-privacy-investigations

Google. (2017). Google APIs terms of service. Retrieved from: https://developers.google.com/terms/

Grasseger, H. & Krogerus, M. (2017, January). The data that turned the world upside down. Motherboard. Retrieved from: https://motherboard.vice.com/en_us/article/how-our-likes-helped-trump-win

Gu, L., Kropotov, V., Yarochkin, F. (2017). The fake news machine: How propagandists abuse the internet and manipulate the public. TrendMicro: Forward-Looking Threat Research (FTR).

Hu, Z., Yang, Z., Liang, X., Salakhutdinov, R., & Xing, E. P. (2017). Controllable text generation. arXiv preprint arXiv:1703.00955.

Hutto, C.J. & Gilbert, E.E. (2014). VADER: A Parsimonious Rule-based Model for Sentiment Analysis of Social Media Text. Eighth International Conference on Weblogs and Social Media (ICWSM-14). Ann Arbor, MI, June 2014.

Jackendoff, R. S. (1972). Semantic interpretation in generative grammar. MIT Press.

Kosinski, M., Matz, S. C., Gosling, S. D., Popov, V., & Stillwell, D. (2015). Facebook as a research tool for the social sciences: Opportunities, challenges, ethical considerations, and practical guidelines. American Psychologist, 70, 543–556. http://dx.doi.org/10.1037/a0039210

Kosinski, M., Stillwell, D., & Graepel, T. (2013). Private traits and attributes are predictable from digital records of human behavior. Proceedings of the National Academy of Sciences, 110(15), 5802-5805.

Kosinski, M., Wang, Y., Lakkaraju, H., & Leskovec, J. (2016). Mining big data to extract patterns and predict real-life outcomes. Psychological Methods, 21(4), 493.

Kosseff, J. (2017). Cybersecurity law. Hoboken, NJ: Wiley.

Kramer, A. D., Guillory, J. E., & Hancock, J. T. (2014). Experimental evidence of massive-scale emotional contagion through social networks. Proceedings of the National Academy of Sciences, 111(24), 8788-8790.

LaValle, S., Lesser, E., Shockley, R., Hopkins, M. S., & Kruschwitz, N. (2011). Big data, analytics and the path from insights to value. MIT Sloan Management Review, 52(2), 21.

Leskovec, J., & Krevl, A. (2014). SNAP Datasets: Stanford Large Network Dataset Collection. Retrieved from: http://snap.stanford.edu/data

Levy, S. (2009). Secret of googlenomics: Data-fueled recipe brews profitability, Wired. Retrieved from: http://archive.wired.com/culture/culturereviews/magazine/17-06/nep_googlenomics

Morstatter, F., Pfeffer, J., Liu, H., & Carley, K. M. (2013). Is the sample good enough? Comparing data from Twitter's streaming API with Twitter's firehose. arXiv preprint arXiv:1306.5204.

Motoyama, M., et al. (2010, August). Re: CAPTCHAs - Understanding CAPTCHA-solving services in an economic context. In USENIX Security Symposium (Vol. 10, p. 3).

O'Sullivan, D. (2017, June 19). The RNC files: Inside the largest US voter data leak. UpGuard. Retrieved from: https://www.upguard.com/breaches/the-rnc-files

Pathak, N., DeLong, C., Banerjee, A., & Erickson, K. (2008, August). Social topic models for community extraction. In 2nd SNA-KDD Workshop (Vol. 8).

Quine, W. V. (2013). Word and object. Mansfield Centre, CT: Martino Publishing.

Ribeiro, F. N., Araújo, M., Gonçalves, P., Gonçalves, M. A., & Benevenuto, F. (2016). SentiBench - a benchmark comparison of state-of-the-practice sentiment analysis methods. EPJ Data Science, 5(1), 1-29.

Risen, J., & Poitras, L. (2013, September 28). NSA gathers data on social connections of US citizens. The New York Times. Retrieved from: https://www.nytimes.com/2013/09/29/us/nsa-examines-social-networks-of-us-citizens.html

Rozenshtein, A. Z. (2017). Surveillance intermediaries. Stanford Law Review.

Saif, H., He, Y., & Alani, H. (2012). Semantic sentiment analysis of Twitter. The Semantic Web – ISWC 2012, 508-524.

Salimans, T. et al. (2017, March). Evolution Strategies as a scalable alternative to reinforcement learning. OpenAI Research, arXiv:1703.03864v1.

Schmarzo, B. (2014, June 10). The value of data: Google gets it!, EMC InFocus. Retrieved from: https://infocus.emc.com/william_schmarzo/the-value-ofdata-google-gets-it/

Segal, A., Feigenbaum, J., & Ford, B. (2016, October). Privacy-preserving lawful contact chaining:[Preliminary Report]. In Proceedings of the 2016 ACM on Workshop on Privacy in the Electronic Society (pp. 185-188). ACM.

Segal, A., Ford, B., & Feigenbaum, J. (2014, August). Catching bandits and only bandits: Privacy-preserving intersection warrants for lawful surveillance. In Proceedings of the Fourth USENIX Workshop on Free and Open Communications on the Internet.

Seriot, N. (2013). Abusing Twitter API & OAuth implementation. Hack In The Box. Retrieved from: http://seriot.ch/resources/abusing_twitter_api/abusing_twitter_api_hitb.pdf

Seriot, N. (2016). STTwitter (v0.2.6) [Computer software]. Retrieved from: https://github.com/nst/STTwitter/archive/0.2.6.tar.gz

Smith, C. M., & Clair, H. D. S. (2011). U.S. Patent No. 7,966,373. Washington, DC: U.S. Patent and Trademark Office.

Thelwall, M. (2013). Heart and soul: Sentiment strength detection in the social web with SentiStrength. Proceedings of the CyberEmotions, 5, 1-14.

Thiel, P. (2014). Zero to one: Notes on startups, or how to build the future. New York: Crown Business.

Varol, O., Ferrara, E., Davis, C. A., Menczer, F., & Flammini, A. (2017). Online human-bot interactions: Detection, estimation, and characterization. arXiv preprint arXiv:1703.03107.

Veiga, M. H. & Eickhoff, C. (2016). A cross-platform collection of social network profiles. arXiv preprint arXiv:1607.03274v1.

Woolley, S. & Guilbeault, D. (2017). Computational propaganda in the United States of America: Manufacturing consensus online. Computational Propaganda Research Project. Oxford University.

You, Q., Luo, J., Jin, H., & Yang, J. (2016, February). Cross-modality consistent regression for joint visual-textual sentiment analysis of social multimedia. In Proceedings of the Ninth ACM International Conference on Web Search and Data Mining (pp. 13-22). ACM.

Youyou, W., Kosinski, M., & Stillwell, D. (2015). Computer-based personality judgments are more accurate than those made by humans. Proceedings of the National Academy of Sciences, 112(4), 1036-1040.

Youyou, W., Stillwell, D., Schwartz, H. A., & Kosinski, M. (2017). Birds of a feather do flock together: Behavior-based personality-assessment method reveals personality similarity among couples and friends. Psychological science, 28(3), 276-284.

Zhang, Y., Gan, Z., & Carin, L. (2016). Generating text via adversarial training.

Zuboff, S. (2015). Big other: Surveillance capitalism and the prospects of an information civilization. Journal of Information Technology, 30(1), 75-89.

Zuboff, S. (2016). The secrets of surveillance capitalism. Frankfurter Allgemeine Zeitung.
