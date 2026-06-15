---
created: 2026-06-03
tags:
  - PBT
---
I want to replicate the study of [[Lavefjord et al., 2025]] with adolescents. [[Vogel et al., 2025a]] have developed a semi-standardized interview to assess [[PECAN]] with children and adolescents (12-18), but only using symptoms and network model of psychopathology.

The most important difference is the differentiation between symptom and process of change. In the study of [[Lavefjord et al., 2025]], the clients had to assess how certain they were that the node causally affected each of the other nodes with a VAS. 

Considering the categories of [[Vogel et al., 2025b]], [[Lavefjord et al., 2025]] used:
- as node property, ==modifiability==
	- To what degree do you feel that you would be able to affect…
		1)	your levels of openness?
		2)	your levels of awareness?
		3)	your levels of engagement?
		4)	how difficult it is for you to conduct your desired activities?
- as edge assessment, ==certainty==:
	- 5. Rate how sure you are that lack of openness leads to lack of awareness
			-Example: Difficult thoughts or feelings that govern you, in turn distract you in everyday life.
			-Example: Difficult thoughts or feelings that govern you, leads to tunnel vision/difficulties getting perspective on things.

I'll use as **node properties**: 
- ==Frequency==
- Severity
- Modifiability
- Controllability

and in order to assess **edges**: 

==**Certainty**: Do you think your sadness is caused by talking to your mother?==

**Frequency**: How often do you feel sad, if you talked to your mother?
 
 **Counterfactuals**: If you no longer talked to your mother, would you still feel sad?

The research question will be: Is there a benefit to start ACT with the most central node? 
# Session 0: Assess PECAN and Node Centrality
## 0. Materials
[visual_aids_PECAN-ACT.pdf]
[Dokumentationsbogen_PECAN-ACT.docx]
[PECAN-ACT_Network_Calculator_R.xlsx]
[PECAN2.R]
[PECAN-ACT_Network_Calculator]
## 1. psychoeducation
Here I want to explain to adolescents what the  triflex processes are
[[Psychoedukation zu ACT-Triflex]]
## 2. clarification of processes 
Discuss every card to check what the patients understand under the processes after the psychoeducation. Try to explore at least an example for every process.
## 3 frequency evaluation
Each node is rated by frequency from 0 to 10. "How often do you feel or behave with openness?"
## 4. causal nodes evaluation
Rate how sure participants are that a lack of openness affects engagement (0-10)
## 5. Evaluation and visualization
Evaluation can be assessed through centrality measures and feedback loops. Visualization can be assured with the R-Package [[PECAN2]]

| Node              | Out-degree Cen. | In-Degree Cen. | Rel. Out-Impact | Rel. Vulnerability |
| :---------------- | --------------: | -------------: | --------------: | -----------------: |
| Awareness         |              21 |             20 |           0.259 |              0.247 |
| Engagement        |              17 |             21 |           0.210 |              0.259 |
| Life Satisfaction |              16 |             20 |           0.198 |              0.247 |
| Openness          |              27 |             20 |           0.333 |              0.247 |

Out-degree Centrality: how much a node drives the network
In-degree Centrality: how much a node is driven by the network
Relative Out-Impact: How much a node (Openness) accounts for the total energy of the network (33.3%)
Relative Vulnerability: How much a node absorbs the energy of the network

**Out-degree Centrality** determines the process to start with in therapy since if the node that drives the network the most gets treated, the whole network gets disturbed the most.
# Session 1-8
ACT protocol with 12 sessions. 4 sessions/triflex process.
[[ACT protocol PECAN-CA]]
