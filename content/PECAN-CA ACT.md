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
- ==frequency==
- severity
- modifiability
- controllability

To assess edges, I'll use:
- ==certainty==: "Do you think your sadness is caused by talking to your mother?"
- frequency: "How often do you fell sad, when you talked to your mother?"
- counterfactuals: "If you no longer talked to your mother, would you still feel sad?"

The research question will be: Is there a benefit to start ACT with the most central node?
# Session 0: Assess PECAN and Node Centrality

## 0. Materials
The following materials can be found in the [OSF Project](https://osf.io/2cj6g/overview?view_only=d462e8aab7a344fa93ba019c7ff445ca):
- Design of the visual aids (visual_aids_PECAN-ACT.pdf)
- Semi-structured interview in German - English version is on the way (Dokumentationsbogen_PECAN-ACT.docx)
- Raw data for R to calculate the Network (PECAN-ACT_Network_Calculator_R.xlsx)
- R-script for PECAN2 (PECAN2.R)
- Excel table to assess centrality (PECAN-ACT_Network_Calculator)

An example of an interview with an adolescent (Marie) can be found in this video: https://www.youtube.com/watch?v=RvC3WEW9BRM

![[STEPS PECAN_CA-ACT.png]]
## 1. psychoeducation
Here I want to explain to adolescents what the triflex processes are
[[Psychoedukation zu ACT-Triflex]] (GER)
## 2. clarification of processes 
Discuss every card to check what the patients understand under the processes after the psychoeducation. Try to explore at least an example for every process.
## 3 frequency evaluation
Each node is rated by frequency from 0 to 10. "How often do you feel open or behave with openness?"
## 4. causal nodes evaluation
Rate how sure participants are that a lack of openness affects engagement (0-10)
## 5. Evaluation and visualization
Evaluation can be assessed through centrality measures and feedback loops. Visualization can be assured with the R-Package [[PECAN2]]

**Perceived Causal Network of Marie (Video):** 
- The size of the nodes (red) describes the frequency of behavior (Engagement is tinier, as Marie feels disoriented and doesn't know what's important in her life)
- The color of the edges describes the certainty (Lack of Life satisfaction certainly influences awareness)
![[Screenshot 2026-06-16 at 14.09.48.png|430]]

**Simplified Perceived Causal Network of Marie (Video)**
![[Screenshot 2026-06-16 at 14.08.44.png|488]]


| Node              | Out-degree Cen. | In-Degree Cen. | Rel. Out-Impact | Rel. Vulnerability |
| :---------------- | --------------: | -------------: | --------------: | -----------------: |
| Awareness         |              20 |             27 |           0.206 |              0.278 |
| Engagement        |              23 |             24 |           0.237 |              0.247 |
| Life Satisfaction |              27 |             23 |           0.278 |              0.237 |
| Openness          |              27 |             23 |           0.278 |              0.237 |

- Out-degree Centrality: how much a node drives the network
- In-degree Centrality: how much a node is driven by the network
- Relative Out-Impact: How much a node (Openness) accounts for the total energy of the network (33.3%)
- Relative Vulnerability: How much a node absorbs the energy of the network

**Out-degree Centrality** determines the process to start with in therapy since if the node that drives the network the most gets treated, the whole network gets disturbed the most.

The Most Central Node Intervention (MCNI) of Marie would be Openness, whereas the Least Central Node Intervention (LCNI) of Marie would be Awareness.

In the SCED, there will be a baseline, than a MCNI Phase and a LCNI Phase. The order of MCNI and LCNI will be randomized in order to assess if individuals starting with MCNI have a faster progression in [[psychological flexibility]].
# Session 1-8
ACT protocol with 12 sessions. 4 sessions/triflex process.
[[ACT protocol PECAN-CA]]
