---
created: 2026-06-03
tags:
  - note
  - journal
---
In the [[Clinical Article]] I want to work on the first session with [[PECAN]] and try to understand which [[ACT]] processes the clients are struggling with.

In order to do that I have to consider [[Vogel 2025a]] and its timeline.

The most important difference is the differentiation between symptom and process of change. The patients had to assess how certain they were that the node causally affected each of the other nodes with a VAS. [PECAN Survey Lavefjord 2025.docx](file:///Users/giorgioalagna/Desktop/PECAN-CA/PECAN%20Survey%20Lavefjord%202025.docx)

Considering the categories of [[Vogel 2025b]], [[Lavefjord 2025a]] used:
- as node property, modifiability
	- To what degree do you feel that you would be able to affect…
		1)	your levels of openness?
		2)	your levels of awareness?
		3)	your levels of engagement?
		4)	how difficult it is for you to conduct your desired activities?
- as edge assessment, certainty:
	- 5. Rate how sure you are that lack of openness leads to lack of awareness
			-Example: Difficult thoughts or feelings that govern you, in turn distract you in everyday life.
			-Example: Difficult thoughts or feelings that govern you, leads to tunnel vision/difficulties getting perspective on things.

Which other categories could I choose from?
**Node properties**: 
- ==Frequency==
- Severity
- Modifiability
- Controllability

**Assessing edges**: 
**Frequency**: How often do you feel sad, if you talked to your mother?
==**Certainty**: Do you think your sadness is caused by talking to your mother?==
**Counterfactuals**: If you no longer talked to your mother, would you still feel sad?
# Session 0
## 0. Materials
[visual_aids_PECAN-ACT.pdf](file:///Users/giorgioalagna/Desktop/PECAN-CA/visual_aids_PECAN-ACT.pdf)
[Dokumentationsbogen_PECAN-ACT.docx](file:///Users/giorgioalagna/Desktop/PECAN-CA/Dokumentationsbogen_PECAN-ACT.docx)
[PECAN-ACT_Network_Calculator_R.xlsx](file:///Users/giorgioalagna/Desktop/PECAN-CA/PECAN-ACT_R/PECAN-ACT_Network_Calculator_R.xlsx)
[PECAN2.R](file:///Users/giorgioalagna/Desktop/PECAN-CA/PECAN-ACT_R/PECAN2.R)
[PECAN-ACT_Network_Calculator](file:///Users/giorgioalagna/Desktop/PECAN-CA/PECAN-ACT_R/PECAN2.R)
## 1. psychoeducation
Here I want to explain to adolescents what the three triflex processes are
[[Psychoedukation zu ACT-Triflex]]
## 2. clarification of processes (ab jetzt [[interviewleitfaden PECAN-ACT]])
Discuss every card to check what the patients understand under the processes after the psychoeducation. Try to explore an example for every process.
## 3 frequency evaluation
Each node is rated by frequency from 0 to 10. "How often do you feel or behave with openness?"
## 4. causal nodes evaluation
Rate how sure participants are that a lack of openness affects engagement (0-10)
## 5. Evaluation and visualization
Evaluation can be assessed through centrality measures and feedback loops. Visualization can be made with [PeCaN Tool](https://pecan-tool.rpsychologist.com/network) or with the R-Packages ([[PECAN r packages]])

| Node              | Out-degree Cen. | In-Degree Cen. | Rel. Out-Impact | Rel. Vulnerability |
| :---------------- | --------------: | -------------: | --------------: | -----------------: |
| Awareness         |              21 |             20 |           0.259 |              0.247 |
| Engagement        |              17 |             21 |           0.210 |              0.259 |
| Life Satisfaction |              16 |             20 |           0.198 |              0.247 |
| Openness          |              27 |             20 |           0.333 |              0.247 |

# Session 1-8
[[ACT protocol PECAN-CA]]
