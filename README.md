Project introduction:

Background research: "AI systems can now pass medical or legal exams, increase white collar productivity in many occupations by over 50%, generate new photo realistic images, and help power more dangerous, autonomous weapons." "Public First ran an extensive nationally representative poll of 2,000 adults in the UK, asking them their opinions around a range of AI related issues. We saw mixed emotions around the rise of AI. The most commonly expressed emotion was curiosity, but otherwise we saw nearly equal excitement and worry." (https://publicfirst.co.uk/ai/)

"Overall, 52% of Americans say they feel more concerned than excited about the increased use of artificial intelligence. Just 10% say they are more excited than concerned, while 36% say they feel an equal mix of these emotions." "Americans with higher levels of education are more likely than others to say AI is having a positive impact across most uses included in the survey. "(https://www.pewresearch.org/short-reads/2023/08/28/growing-public-concern-about-the-role-of-artificial-intelligence-in-daily-life/)

"Nearly $14B has been invested into Generative AI through the first half of 2023. This represents nearly 40% of total VC investment this year to date and an astounding 3x increase on the total capital invested into the sector from 2022." (https://marchcp.com/the-rise-of-generative-ai-a-tale-of-two-venture-markets/)


Based on the background that the Artificial Intelligence technology is rapidly developing in a relatively short time, this project is dedicated to finding out the public opinion on AI in different fields from customers' perspective to provide insights for Venture Capital Companies in terms of their investment on AI industry. As one of the world's biggest VC firms, Sequoia Capital expanded its portfolio in artificial intelligence industry. In 2023, nearly 60% of the company's new investments are in AI startups.

Data Souce:
1. For the public opinion, a survey is created manually and distributed to the public on the 2 survey platforms: Quatrics(globaly) and SurveyMonkey(solely to the US). The survey consists demographic data collection and 5 questions about AI from different angles. The anonymous link to the survey is https://qualtricsxmw8jmz7ws2.qualtrics.com/jfe/form/SV_d9Z7bWloIVdkFQa
2. For the catalog of AI companies invested by Sequoia, Web scraping by using Selenium is performed in the meanwhile.
3. For the data of the venture capital industry in the US, free open dataset is from https://www.kaggle.com/datasets/adnananam/largest-us-venture-funding-deals-of-2023

Data Wrangling:
1. Survey respondenses: shortening the column names, standardizing the ratings from the two platforms and combining the two datasets into one and save the result into a csv file.
2. Company information: re-categorizing the companies into 2 levels. 
1st level: Enterprise(product is designed for enterprise directly), Consumer(product is designed for individual consumers directly), AI/ML(product's target audience is not defined)
2nd level: Customer relationship, Healthcare, Self-driving technology, Law firm, and Other
3. US funding deals: data cleaning

Hypothesis setting:
H0 hypothesis: Customers' opinions on the 4 different AI products, namely "Customer Relationship Management", "Healthcare Use",
"Self-driving Vehicle", and "Law Firm Related" and their general opinion on AI are the same.
Ha hypothesis: At least one of 5 customers' opinions on AI, namely "Customer Relationship Management", "Healthcare Use",
"Self-driving Vehicle", "Law Firm Related" and general opinion is different from the others.

Hypothesis testing:
One-Way ANOVA model and Tukey's Honestly Significant Difference

Conclusion:
F-statistic: 3.9325592796237743, p-value: 0.003609137552494191
Reject the null hypothesis. There is a significant difference among group means.
Specifically, the ratings between customer_relationship and law_firm, and the ratings between customer_relationship and sel_driving_tech are significantly different.

Estimated rating for the population:

'The estimated rating with 95% Confidence Interval for knowledge of the public is in the range': (44.93811056095711,   52.23472894521573),
 'The estimated rating with 95% Confidence Interval for general of the public is in the range': (46.79471861652086,  55.378120889651974),
 'The estimated rating with 95% Confidence Interval for customer_relationship of the public is in the range': (49.23753358654359,   58.16987382086381),
 'The estimated rating with 95% Confidence Interval for healthcare of the public is in the range': (43.890102633029684,   52.69014428055057),
 'The estimated rating with 95% Confidence Interval for self_driving_tech of the public is in the range': (39.65663008049801,   48.62732053678594),
 'The estimated rating with 95% Confidence Interval for law_firm of the public is in the range': (39.35171696879666,   47.710011426265076)

Interpretation on the prediction:
1. The public believe they know a less-than-moderate amount of knowledge about AI
2. It's possible that the public are willing to use AI to resolve practical issues 
3. The public are more likely to use AI for the purpose of Customer Relationship Management than other 3 types of AI
4. The public are less likely to use AI for Self-Driving Technology and Law Firm

Interesting EDA findings:
#Male has a higher tendency of using AI for all 5 scenarios
#the higher the education level is, the more likely the respondent is to use AI in all 5 scenarios.
#knowledge does not seem to have very strong correlation with any of the ratings
#rating of customer_relationship seems to have a high correlation with healthcare
#rating of self_driving seems to have a high correlation with law_firm


Background knowledge on the investment stages from Sequoia:
Arc:

Description: The "Arc" stage typically refers to the earliest phase of a startup's development, even before traditional seed funding. It may involve very early investment to help the founders shape their idea, conduct initial market research, and potentially develop a prototype.
Seed:

Description: The "Seed" stage is similar to the conventional seed funding stage. It involves providing capital to startups in their initial phases to help them validate their business idea, develop a minimum viable product (MVP), and establish a founding team.
Early:

Description: The "Early" stage likely corresponds to the broader early-stage funding rounds, such as Series A and Series B. At this point, startups have typically demonstrated product-market fit and are focused on scaling operations and expanding their market presence.
Growth:

Description: The "Growth" stage involves investing in more mature companies that have proven their business models and are in a phase of rapid expansion. This funding is intended to fuel further growth, potentially in terms of market reach, customer acquisition, and product development.
Acquired:

Description: The "Acquired" stage likely refers to companies that have been acquired by larger entities. Sequoia may have played a role in funding these companies during their earlier stages and continues to support them through acquisition.
IPO (Initial Public Offering):

Description: The "IPO" stage signifies the point at which a company goes public by offering its shares on the stock market. Sequoia may have been an early investor and continues to be involved in supporting the company through the process of becoming a publicly traded entity.


"Reactive AI stems from statistical math and can analyze vast amounts of data to produce a seemingly intelligence output."
Examples of Reactive Machine AI
IBM Deep Blue: IBM’s chess-playing supercomputer AI beat chess grandmaster Garry Kasparov in the late 1990s by analyzing the pieces on the board and predicting the probable outcomes of each move
The Netflix Recommendation Engine: Netflix’s viewing recommendations are powered by models that process data sets collected from viewing history to provide customers with content they’re most likely to enjoy

"Unlike Reactive Machine AI, this form of AI can recall past events and outcomes and monitor specific objects or situations over time. Limited Memory AI can use past- and present-moment data to decide on a course of action most likely to help achieve a desired outcome. "
Examples of Limited Memory AI
Generative AI: Generative AI tools such as ChatGPT, Bard and DeepAI rely on limited memory AI capabilities to predict the next word, phrase or visual element within the content it’s generating
Virtual assistants and chatbots: Siri, Alexa, Google Assistant, Cortana and IBM Watson Assistant combine natural language processing (NLP) and Limited Memory AI to understand questions and requests, take appropriate actions and compose responses
Self-driving cars: Autonomous vehicles use Limited Memory AI to understand the world around them in real-time and make informed decisions on when to apply speed, brake, make a turn, etc.
(https://www.ibm.com/blog/understanding-the-different-types-of-artificial-intelligence/)
