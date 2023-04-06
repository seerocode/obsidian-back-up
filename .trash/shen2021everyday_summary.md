 @import url(https://themes.googleusercontent.com/fonts/css?kit=sCR6ORJJ\_1QHAOsqev1h5GRYh9syjTFm17fR6pfMaDM);

Updated: 2023-04-05T16:10:18.000Z

# Everyday Algorithm Auditing: Understanding the Power of Everyday Users in Surfacing Harmful Algorithmic Behaviors

shen2021everyday

Hong Shen, Alicia DeVos, Motahhare Eslami, and Kenneth Holstein. 2021. Everyday Algorithm Auditing: Understanding the Power of Everyday Users in Surfacing Harmful Algorithmic Behaviors. \_Proc. ACM Hum.-Comput. Interact.\_ 5, CSCW2 (October 2021), 433:1-433:29. DOI:<https://doi.org/10.1145/3479577>

### Relevance to recikCGKqx5PlZq9X:

Strengths: they provided clear limitations of existing auditing approaches and separated organic audits from crowdsourced audits which were more the focus of the devos paper in a way and confounded the two.

### Summary:

* * *

### Abstract Breakdown:

### Thesis/Main Research Question(s):

1\. What factors facilitate “\*\*successful\*\*” user-driven algorithmic audits, and what factors prevent such audits from having an impact?

2\. How might we effectively harness everyday users’ motivation and strengths in surfacing harmful algorithmic behaviors, so as to \*\*overcome the limitations of existing auditing approaches\*\*?

### Motivation:

Formal auditing approaches often suffer major blindspots, with critical issues surfacing only in the context of everyday use once systems are deployed but little attention in literature has been paid to everyday algorithm auditing.

Many open questions remain regarding how users of algorithmic systems come to detect, report, and theorize about harmful algorithmic biases and behaviors in their day-to-day use of a platform. The authors attempt to answer the following questions:

The authors aim to bridge the gap between algorithmic auditing approaches proposed in the academic research literature and auditing behaviors that users exhibit day-to-day.

### Contribution:

They outlined 5 broad categories of \*\*potential design interventions\*\* —

\- (a) community guidance such as designing spaces specifically for everyday audits,

\- (b) expert guidance by inviting relevant exprrts to monitor discussions and intervene when necessary but much like the previous paper, this may backfire and influence the sensemaking of the user audit (also making bidirectional feedback mechanisms),

\- (c) algorithmic guidance, \[\*\*Instance-based auditing \*\*applies to cases where the observation of an isolated harmful algorithmic behavior is sufficient to ground an argument for remediation.....\*\*comparison-based auditing\*\* applies to cases where, in order to establish that a harmful bias truly exists and is worth addressing, it is necessary to compare multiple instances and demonstrate the existence of statistical patterns.\]

\- \*\*(d)\*\* organizational guidance -> encourage users to take on roles during an audit process that may be important and may not come up organically , and

\- (e) incentivization — bounty programs but with the risk of reducing \*\*spontaneity. also incentivize developers and platforms possibly by public awareness raising\*\*

### Methods: Case Studies

### Methodology:

They adopted an exploratory case study approach to \*\*examine the Twitter cropping algorithm and Yelp advertising bias as well as Booking.com quality bias\*\*. Many small business owners on Yelp came together to investigate Yelp’s potential bias against businesses that do not advertise with Yelp. A group of users on Booking.com scrutinized its rating algorithm after realizing the ratings appeared mismatched with their expectations.

They asked:

\- How can we better understand the characteristics, dynamics, and progression of everyday auditing practices?

\- How can we support everyday users in detecting, reporting, and theorizing about problematic machine behaviors during the course of their interactions with algorithmic systems?

They developed key words to search for cases of everyday algorithm auditing that met their \*\*definition\*\* for everyday algorithm auditing: one or more everyday users act to detect, understand, and/or interrogate biased and harmful algorithmic behaviors through their everyday use of a platform. They wanted to formalize this concept to guide future empirical work.

### Results/Findings:

They found that everyday algorithm audits follow the process of

\- (1) initiating an audit usually by stumbling upon the issue,

\- (2) raising awareness of observed harm by broadcasting it to others,

\- (3) hypothesizing about observed behavior by usually developing folk theories that help them form hypotheses about the cause of the bias

\- (4) \*\*remediation through external awareness and subsequent pressure for change or in the form of legal action where 700 lawsuits were filed against Yelp. Lastly, platform level change which they argued is the most effective change.\*\*

They also found through their case study analysis that everyday algorithm auditing is more powerful when they are conducted \*\*collectively\*\* through interactive discussions.

The authors made a distinction between everyday audits that were initiated by experts such as Sweeney and non-experts who have little algorithm expertise. The organicness of these audits also varied in that they may have started organically and ended in a more systematic approach such as Sweeney. Likewise, they could be organic from end to end with minimal intervention from others.

They believe this type of auditing to be algorithmic resistance and that when done collectively, can be seen as a form of \*\*counterpublics\*\*.

They offer recommendations for bridge the gap between existing algorithm auditing approaches in academia and industry versus everyday auditing behaviors that emerge in day-to-day use of algorithmic systems by exploring what lessons might be drawn from the study to overcome limitations of previously proposed auditing approaches. They asked:

1\. how designers might facilitate everyday algorithm auditing practices, building upon regular users’ existing motivations to engage in such auditing behaviors and\*\* supporting their unique strengths in surfacing harmful algorithmic behaviors\*\*. How might designers support and scaffold everyday algorithm audits, \*\*without intervening so heavily as to sacrifice their bottom-up, user-driven natur\*\*e?

### Limitations/Weaknesses:

\- Only targeting recent examples

\- \*\*Why does organicness matter? That wasn't made clear, only that it was used as a factor for case study choice.\*\*

### Future Work:

However, currently we have very limited understanding of the appropriate timing for intervention. For example, how can we maintain the organic nature of everyday algorithm auditing, especially at the initiation stage, but also prompt a group of people to start auditing ￿rst, which might inevitably remove some of the organic nature?

Currently we are only at the starting point to understand and explore the appropriate degrees of these interventions. How much intervention is too much? What are the trade-o￿s in moving from more organic to more organized at di￿erent phases of an everyday audit? These questions need further research and investigation; the exploration of everyday algorithm auditing is in its infancy, and our work presents a ￿rst step.

\- \*\*Future research should conduct in-depth follow-up studies with users to investigate the practices and strategies they use to ￿nd and make sense of harmful algorithmic behaviors. \*\*

Another fruitful, complementary area for future research includes an exploration of the design opportunities discussed above. For example, how can we design platforms that support users in conducting more e￿ective everyday algorithm audits, both individually and collectively?