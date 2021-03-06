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

**Figure 3:** *Monitoring service that scrapes population-level data for a given target population as well as the entire population for control.*

Monitoring agents must be designed specifically for each data source to be monitored, though off-the-shelf monitoring agents and dashboards already exist for most social media platforms (Batrinca & Treleaven, 2015). Further to (Rozenshtein, 2017) and the notion that social media companies act as brokers between government requests and a population's raw data, these corporations actually act as broker against **any third-party** wishing to access a user's detailed behavioural data, not just state entities. Any company large enough to be considered a surveillance intermediary must recognize that they are actually in competition with a variety of actors trying to gain access to their behavioural datastores for a variety of actor-specific purposes. The clever big social data broker engineers services that preserve user anonymity while still facilitating the monetization of user data, because the raw data represents the long term value to the provider and anyone capable of obtaining it. Partial data access is typically available using an API key for sampled or rate-limited access to raw data feeds or user account data. Headless browsers, like PhantomJS, and scraping tools, like Beautiful Soup, permit web-only scraping of any public website data. For those with deep pockets, Twitter makes their entire raw data feed available to private entities (GET CITE - Cambridge Analytica) and downstream aggregation providers like Google Search (GET CITE - Twitter Sharing w/ Google). The firehose method is by definition a superset of API sampling, though the two can provide comparable results for geographic, topical and network-level measures using multi-day aggregations of data (Morstatter et al., 2013). Most web content providers employ rate limiting and other defensive measures to prevent scraping of public or authenticated-only content as is now required by law in North America (Kosseff, 2017). Thus, for the enterprising PRCaaS architect, creative measures are needed to provide sufficient ongoing monitoring coverage against a surveillance intermediary. For example, fake social accounts can follow private profiles and crawl the resulting content (Varol et al., 2017). Multiple accounts and token swapping are useful approaches in circumventing per-key limitations (Seriot, 2013, 2016). The PRCaaS employs a token brokering PKI to ensure timely access to user-specific tokens, fresh tokens, and that per-token API restrictions are not exceeded. Thus, monitoring service design must reflect the need to capture and aggregate ongoing feeds of data about an ever-growing population, while segmenting responses and conversation around a specific topic, possibly in the face of opposition from the data source itself.

### 2.2. Profiling & Feature Extraction Service
Human personality can be accurately predicted using a very small number of data points about that individual (Kosinski, Matz et al., 2015). To that end, the Profiling service intakes the raw data acquired from Monitoring and builds categorical profiles about the target population, as well as the general population for control. Automated tools such as VADER (Hutto & Gilbert, 2014) and SentiStrength (Thelwall, 2013) compute sentiment profiles over textual input and output a sentiment score for each sentence. Mined images are processed to extract sentiment based on visual-textual analysis, like in (You et al., 2016), whereupon aggregates of sentence and image sentiment are computed for each individual and group in the target population. For a full comparison of language-based sentiment analysis tools and methodology see (Ribeiro et al., 2016). Bridging these sentiment profiles with long term retail sales data, for example, would reveal exactly the personality types who purchase one brand of soda over another because the system knows everyone who purchases soda, at what frequency, and everyone's personality type. Custom and contextualized profiling algorithms are possible using singular value decomposition (SVD) and latent Dirichlet allocation (LDA) (see: Kosinski, Wang et al., 2016). The construction of psychological models based on human event data is a proven way to accurately profile a population's personalities and the first step to deriving a credit assignment problem for human behaviour and conversation. Returning to the Coke/Pepsi example, the Profiling service takes data on everyone in a population - "Coke drinkers", "Pepsi drinkers", "Both Drinkers", "Non-soda drinkers" - and categorizes them based on their event data into one of those categories. The system then measures differences between each group to understand personality overlap, opposites, and potential avenues of exploitation for propaganda as attributed to social communication data. Attributes derived from Profiling propagate back to user records as actionable metrics for targeted propaganda generation and delivery. Propaganda can be tested against diverse members of the population or streamlined towards a well-understood or cost-effective target group. The best way to think of Profiling is as an automated Q & A service for credit assignment of observed outcomes against the target population's ongoing daily behaviour.

**Figure 4:** *Profiling & feature extraction service that aims to derive credit assignment from language and behavioural data.*

Insufficient or poor quality behavioural data will result in poor profile calculations and thus poorly fitted propaganda as output. We must remain realistic about the system's capabilities in the face of insufficient understanding of its targets and delivery capabilities. The goal is to make minute differentiations and derive accurate predictive propaganda for an entire population. For this you need a lot of data. Generative techniques that necessitate fewer test cases, like one-shot and  evolution strategy, are well suited to this case (Salimans et al., 2017). The desire to understand the psychometric and linguistic patterns behind "Michigan residents who drink Pepsi", or narrowed further to a specific county or township, is driven by the desire to deliver targeted propaganda to influence that specific subsample. Profiling represents the application of credit assignment models to personality and choice as big social data fragments, tying them to actions that lead humans to make specific choices (Youyou et al., 2017). The service takes the raw event data and infers causation at scale about actions of individual actors, groups of actors, and the population as a whole, as a function of their communications. These profiles are then transposed over other segments of the population based on observable human metrics and the fine-grained behavioural data amalgamated during Monitoring. By establishing conversational and behavioural profiles of real humans who are really "for", "against", and "ambivalent" towards a certain topic, it becomes possible to develop targeted messaging designed to move a profile (or set of profiles) from one category to another, and to express that desire mathematically.

#### 2.2.1. Calculate Sentiment Profiles
TODO

#### 2.2.2. Human Sentence Extraction
TODO

#### 2.2.3. Converting Sentences to Templates
TODO

### 2.3. Modeling Service
TODO

### 2.4. Propaganda Generation Service
TODO

To generate contextualized propaganda the service utilizes 1) medium-specific grammars, 2) sentiment-gating, and 3) template messages. 

The system takes an understanding of the population (Profiling), template messages (Profiling), a plan of attack (Modeling), and generates targeted and contextualized propaganda according the messages it receives using the "Propaganda Generation Service" (PGS). The Modeling service makes a simple `getPropaganda(campaign)` call to start the flow. Propaganda is needed for each individual and profile of individuals across each sentiment category in the target population specified. This is entirely configurable to focus on individuals or groups as specified in target profiles provided to the service: Mimic anyone, target anyone. The system described here employs only text-based profiling and generation, though image- and video-based systems should be straightforward to integrate (see: Duan et al., 2017 ; GET CITE - for video). Text is generated from sentence templates according to a medium-specific grammar and the sentences extracted during Profiling. Text generation is more advanced and is best modeled as a pipeline of transformations that occur on template sentences to achieve what appears to be unique language according to configuration parameters, not unlike (Hu et al., 2017). Grammatical processing rules are needed beyond templates because, unlike natural human conversation, propaganda must conform to hard rules of the delivery medium. Solutions exist already for human-passable term papers (GET CITE - term papers); legal tedium (GET CITE - automating legal proceedings); press releases (GET CITE); and even t-shirts and swag (GET CITE). The provided example employs a Twitter-specific grammatical ruleset: 140 characters for text and URLs. Messages must conform to this hard count, and a number of other API-based restrictions, so the PGS must force agents and resulting propaganda to conform to these rules. Arranging this as a pipeline, the system generates and delivers messaging using a shared grammatical ruleset of type "Twitter". That is, all input and output messages are 140 chars and conform to the variations permitted by Twitter's API: tweets, replies, retweets, favourites, lists, private messages and blocks. Context-specific grammars consist of these platform-specific variations as a set of rules to parse and generate messages of that type (see: "2.4.1 Medium-Specific Grammar").

**Figure 6:** *Propaganda Generation Service*

### 2.5. Delivery Service
To achieve "last mile" delivery of propaganda to the target population the Delivery service utilizes a dispatcher, medium-specific queues, and delivery agents. Like with Monitoring the communication medium dictates agent design. Service architecture took inspiration from (Smith & Clair, 2011, Figure 9) for the service-level message queue leading to a central dispatcher, as well as for agent-specific rendering. The PRCaaS takes this a step further by incorporating offensive capabilities for voluminous delivery by design (see: 2.5.2. Circumventing Barriers to Voluminous Delivery). Messages are forwarded to the appropriate last mile delivery queue, rendering is performed if needed, and delivery receipts stored to an external datastore.  Token and secret management is handled similarly to Monitoring, with secrets reused across both services as permitted by API restrictions. Some human intervention may necessarily be required for certain delivery mediums (eg. purchasing SuperBowl television advertising space) while not all delivery mediums are for sale in the traditional sense (eg. the sentiment score of Reddit and YouTube comments). Just like Monitoring, Delivery is indifferent to propaganda it receives and imparts: Character limits, platform-specific language, and content restrictions are already handled during Propaganda Generation. API rate-limiting, IP blocking, traffic fingerprinting, and other defensive measures must be circumvented continually by Delivery for the system to be effective.

**Figure 7:** *Delivery service using medium-specific agents to deliver digital and physical messaging.*

#### 2.5.1. Social Bots as Delivery Agents
Increasingly, bots (social and otherwise) are seen as a credible tool for propaganda delivery with the ability to "influence political processes of global significance" (Woolley & Guilbeault, 2017). The PRCaaS supports bot-based communication perfectly due to its support for medium-specific communication and voluminous, topical, and unique message generation and delivery. The use of human-seeming profiles and friend networks can make bots nearly indistinguishable from human users, though bot detection frameworks are increasingly accurate at distinguishing between them (Varol et al., 2017). Like the SPAM wars that have endured since the internet's conception (see: Brunton, 2013), surveillance intermediaries are increasingly fighting off AI-driven content as it starts to affect bottom lines and users' social perceptions (Bickert, 2017 ; Chapman, 2017).  This will be a challenging fight: The volume of messaging generated and delivered is limited only by computing and financial capabilities. This is a good match for the limitless storage capabilities of the surveillance intermediaries. Since the long term value of these companies is represented by **human** behavioural data, it follows that they have a vested interest in filtering non-human content to prevent manipulation and degradation of their platforms. Put simply, PRCaaS message generation and delivery at such a high volume, limited only by technical and financial constraints, begins to look a lot like SPAM. Palantir's psychological warfare techniques - "Potential Proactive Tactics" - (Coleman, 2017, p. 207) could easily be automated through the service.

#### 2.5.2. Barriers to Voluminous Monitoring & Delivery

Platform-specific defensive measures like curation, IP blocking, rate limiting, SPAM/bot detection, and content removal are potential impediments to message delivery. For this reason, Delivery should employ platform-agnostic delivery services using a distributed queuing mechanism. Traffic should be disguised so that the source of propaganda is not obvious. One million accounts delivering identical messages is trivial to identify, trace, and counter. Slight variations like those achieved by the PGS make detection and identification more difficult. Delivery mechanisms can be incredibly specialized if needed since they need only deliver a message and track the read receipt. Monitoring already handles measurement of propaganda, interaction metrics, and any social conversation that arises from it. Anticipating defensive measures, agent engineering calls for security circumvention techniques by design. Platform-specific protections against digital automation, like CAPTCHAS, can be circumvented using custom software or paid human solvers (Motoyama et al., 2010). Upfront development efforts are considerable since you are effectively working to outsmart the security teams at top-tier surveillance intermediaries to introduce SPAM into their networks. However, once built the agents require only maintenance in the case of API changes or new access restrictions. Native support by surveillance intermediaries for automated messaging means the clever Delivery service should simply be designed to mimic human behaviour as closely as possible. If the content is "human enough", networks will be unable to distinguish the SPAM messages from human ones. This follows from Propaganda Generation where messaging that seems to be human-generated is desirable in order to increase credibility of messaging and reduce filterability. Since propaganda sentences and topics are derived directly from human conversation the systems performs well towards that end.

### 2.6. Visualization & Administration Services
All of the other services generate significant data visualization and administration requirements. Visualization represents data about the actual PRCaaS campaigns, digital footprint data, propaganda and services, whereas Administration handles user and system management tasks. Under the hood components are implementation specific, but assuming containers you might have a Mesos/Marathon/Docker stack with each service running inside a Docker container. Typical cloud management techniques to ensure scalability and performance are needed. Administration really represents the entire set of configuration utilities employed to manage the system's operations. Visualization overlays for each component of each campaign are desirable. Measurements and A/B testing of propaganda before mass delivery is an essential function of the PRCaaS: Without the ability to measure propaganda uptake and improve messaging, the system cannot be self-learning and propaganda effectiveness remains guesswork. 

***Figure 8:*** *Administer the system and visualize messaging performance using an industry standard data pipeline with custom analytics overlay.*

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
