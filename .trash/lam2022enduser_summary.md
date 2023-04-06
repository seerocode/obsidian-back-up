 @import url(https://themes.googleusercontent.com/fonts/css?kit=sCR6ORJJ\_1QHAOsqev1h5GRYh9syjTFm17fR6pfMaDM);

Updated: 2023-04-05T16:10:15.000Z

# End-User Audits: A System Empowering Communities to Lead Large-Scale Investigations of Harmful Algorithmic Behavior

lam2022enduser

Michelle S. Lam, Mitchell L. Gordon, Danaë Metaxa, Jeffrey T. Hancock, James A. Landay, and Michael S. Bernstein. 2022. End-User Audits: A System Empowering Communities to Lead Large-Scale Investigations of Harmful Algorithmic Behavior. \_Proc. ACM Hum.-Comput. Interact.\_ 6, CSCW2 (November 2022), 512:1-512:34. DOI:<https://doi.org/10.1145/3555625>

### Relevance to recikCGKqx5PlZq9X:

Working toward a model for guiding user-led audits but this is different in that users are given specific roles which makes surfacing these issues not organic in nature. \*\*Which begs the question, why does organicness matter? \*\*

### Summary:

* * *

### Abstract Breakdown:

### Thesis/Main Research Question(s):

\- RQ1—Does modeling end users’ labels enable end-user audits? Does our approach model users’ perspectives reasonably well? Do end users find the auditing process comprehensible?

\- RQ2—Do end-user audits yield insights? What kinds of issues do users uncover in their audits? Do users discover unique insights?

### Motivation:

\*\*Context\*\*: Performing a system-scale audit requires substantial user effort to label thousands of system outputs and one major limitation of auditing is its reliance on expert auditors: audits can only uncover issues where those auditors think to look. \*\*End users hold the promise\*\* to expand this purview, as they inhabit spaces and witness algorithmic impacts that auditors do not.

\*\*Goal\*\*: The authors propose end-user audits-system-scale audits led by non-technical users-and present an approach that scaffolds end users in hypothesis generation, evidence identification, and results communication. Today, performing a system-scale audit requires substantial user effort to label thousands of system outputs, so the authors introduce a collaborative filtering technique that leverages the algorithmic system's own disaggregated training data to project from a small number of end user labels onto the full test set.

### Contribution:

The contributions of this paper are:

\- \*\*An end-user auditing approach. \*\*We introduce a recommender system approach to model individual users’ perspectives, which scaffolds the auditing process for non-technical users.

\- \*\*The IndieLabel system. \*\*We introduce a web-based tool for end-user auditing. With this tool, users can provide a small number of labels, propagate their perspective to the full dataset using their personalized model, test their hypotheses at a large scale, and create an audit report to communicate their findings.

\- \*\*An end-user audit of the Perspective API. \*\*We conduct a study with 17 non-technical users who use the IndieLabel tool to audit the Perspective API model. We find that users were successfully able to lead their own audits that yielded previously underreported insights on a host of potential system issues.

### Methods: Usability testing

### Methodology:

\*\*Problem\*\*:

1\. First, the authors assumed that the target system—the system against which users will conduct algorithm audits—assigned binary labels (i.e., “toxic” or “non-toxic”) via comparison to a threshold score.

2\. Second, the authors assumed that this classification task was directly tied to a real-world action (e.g., the deletion or downranking of a post).

This problem setup is aligned with that of many real-world ML systems on platforms such as YouTube and Facebook and is directly applicable to a variety of language-based tasks (e.g., hate speech, misinformation, clickbait, spam detection) as well as vision tasks (e.g., facial recognition, object detection).

The targets of this paper's audits are algorithmic systems (ML models), the goal of the audit is to make claims about the system as a whole (reviewing system behavior on a comprehensive dataset), and the auditor might not have consent from the entity that is being audited (end users can use this paper's auditing approach without internal access to the system).

The authors sampled comments from the dataset, users labeled these comments on the frontend, the authors ran the SVD model on the training set with these labels, and the authors retrieved predictions for the entire test set, which powered this paper's frontend auditing interface and visualizations to help users build their own auditing reports.

### Results/Findings:

In an evaluation with 17 non-technical users, they found that end users were able to successfully lead algorithm audits.

\- Using the IndieLabel tool, they audited Perspective API, and u\*\*sers identified a total of 76 issues spanning 57 distinct topic areas and uncovered previously underreported issues\*\* including over-flagging content about sensitive topics like race, slavery, and sexual assault; under-flagging on subtler forms of hate that perpetuate stereotypes and stigma; and over-flagging of several slurs that have been reclaimed by marginalized communities.

\- Users were also independently able to uncover three main types of issues with the Perspective API that had been documented in prior research, supporting the correctness and viability of end-user auditing.

\- During a half-hour auditing period, users conducted audits for multiple topics, and \*\*users found supporting evidence of potential issues in 75% of their audits. \*\*

\- Further, users \*\*demonstrated a great deal of skill and creativity in their audits\*\*: users conducted audits on 36 unique topic areas that no other users in the study explored, and the vast majority of participants (all but one) felt that they had discovered issues that they hadn’t anticipated beforehand.

The authors found in this paper's study that non-technical users were successfully able to lead algorithm audits. The proposed approach of end-user auditing, which leverages a collaborative filtering technique and a tool called IndieLabel, can help non-technical users lead system-scale audits.

In this paper's qualitative analysis of end-user audits, the authors found that users converged upon several clear sets of issues, expressed valid diverging opinions about system behavior on divisive topics, and surfaced unique insights that other users had not uncovered.

\- Participants noted that \*\*certain keywords were challenging to moderate \*\*because they have multiple, vastly differing meanings, but the system tended to rule based on the toxic interpretation of the keyword.

\- Many participants also raised that \*\*certain slurs have been reclaimed by communities and are acceptable when used among community members, but were over-flagged by the system\*\*.

\- When users audited the same topic, \*\*the end-user auditing approach was able to solicit insightful, differing perspectives on whether issues existed, why certain system behavior was problematic, and what solution strategies could work\*\*. These results demonstrated the power of this paper's approach to shift from monolithic auditing perspectives to a paradigm where audit results could come from different populations who might see things differently.

Platforms may find it beneficial to incorporate end-user auditing into their workflows to improve user trust\*\*: 77% of users felt that if they knew that a platform would be using their audit report to make changes, they would somewhat trust or trust its content moderation system.\*\*

### Limitations/Weaknesses:

\- \_Is the motivating scenario real? Who made it up?\_

\- \*\*self-selection bias\*\*: approach assumes that users are highly motivated to devote time and effort to conduct their own audit

\- Even though any user could use our tool in theory, \*\*more privileged or tech-savvy users may be over-represented in practice.\*\*

\- End-user model is imperfect and\*\* cannot be expected to fully capture the complexities of user perspectives for difficult tasks like content moderation\*\*. It is possible that this model itself may be biased (for example, if the initial set of annotators is biased or fails to represent a new user’s views).

\- Modeling approach is limited to the set of examples in a collected dataset, so they \*\*cannot predict user’s ratings of unseen examples. \*\*Future work might expand this method to project user’s opinions on novel examples.

\- \*\*Users might raise spurious issues if they misinterpret plots or raise audit reports based on limited evidence\*\*. Prior exploratory research has identified this difficulty in discerning the legitimacy of reports as a core challenge for user-led auditing \[19\].

### Future Work:

Users proposed improvements to a tool like IndieLabel:

\- target of speech - Comments can take on very different meanings depending on whether they are targeted at another user (and may further vary based on the relationship between the users), a group, oneself, or a non-person (like a place, object, or corporation).

\- identity of the poster - The identity of the poster also plays a large role in shaping the meaning of a comment. If the comment is directed at a group, the poster’s membership or outsider status to the group may determine whether the comment is harmful.

\- Disambiguate multiple senses of keywords - Many keywords often associated with toxic content have multiple differing meanings. More sophisticated disambiguation between these different usages would likely reduce overflagging behavior.

\- D\*\*ifferentiate between triggering content and toxic content \*\*- In discussions about sensitive topics, comments may be triggering for users. However, participants felt that these kinds of content should not be treated the same way as toxic content because erasure of these discussions would be harmful to marginalized groups. \*\*There are other options besides content removal, and alternative designs may help to foster wellbeing while keeping discussions alive. \*\*\_(what are alternative designs?)\_

\- \*\*Consider the tone, mood, or emotion of the comment \*\*- The emotion or tone of a comment often significantly shapes its interpretation. Without a grasp on the emotions underlying a comment, content moderation systems may overflag humorous or emotive wordings.

Other:

\- Developers who adopt our approach must be aware of this bias and take active steps to ensure that marginalized users are represented.

\- Potential for future work on the legal and regulatory side to compel companies to implement such auditing capabilities into their systems.

\- Effectively and fairly aggregate the audit reports that users generate.

\- Developers who leverage end-user audits interrogate the broader ethical risks of their systems as audits are not a cure all.

\- Future work might explore more advanced recommender system models that better capture user opinions.