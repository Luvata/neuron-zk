---
tags: [course, MLSS]
---

# Probabilistic Graphical Model (PGM) - MLSS 2013 - Bishop
The course comes with 3 lecture videos that was taught by [[Christopher Bishop]] at MLSS 2013. I took this course when I'm stuck at Lecture 5 of CS330. It's also the first course I learn from [[MLSS]]. IMO he did give a brief introduction to graphical model and its applications (which is quite interesting), but to understand PGM only from these three lecture videos is still far from enough. I suggest reading chapter 8 of PRML for deeper understanding. Below is my summary of this course

## 1. Topic covers
### 1.1 Review of probability:
The first and second lecture video give a brief explain about probability overview
- 4 rules of Probability:
    - Product rule
    - Sum rule
    - Denominator rule 
    - [[Bayes' theorem]]
- Conditional independence,  and how it changes under different observations

### 1.2. Graphical Model
The last half of first lecture, and the second lecture dive deeper into how represent event as graph, its application, 

Combine probability with graph. It comes with some advantages:
 - Using graph theories for efficient inference (Instead of greedy compute, we use graph factorization to calculate particular interested event)

- Three types of graph to represent joint probability:
	- [[Directed graph]] 
    - [[Undirected graph]]
    - [[Factor graph]]

- Algorithms that were mentioned and their applications:
	- Under the hood, [[Sum-Product Algorithm]] played an important roles to infer efficiently by only looking at message schedule from each nodes in two directions
		- Calculate probability of a node, as a recursive algorithm
		- Efficient for tree structure
		- If the graph has loops, approximation (ignore the loops, treat it like a normal tree) can still give a decent answer
    - [[Image denoising]], by finding the image that has lowest energy between predict pixel and truth pixel, and also between neighbor pixel
    - [[Markov Random Field]] for [[Image Segmentation]]
    - [[Kalman Filter]] for hand tracking with noisy sensor and moving hand :
		- Estimate the noise level of sensor
		- Lower the uncertainty of predictions from recent observation
    - [[Expectation Propagation]] for player ranking, in [[TrueSkill]]

## 2. Interesting readings
- Variables could be dependent together or not under different observations
- Image denoising example is some kind of energy based model, that minimize energy of true pixel value and observable pixel (pixel could be noise)
- Directed graph to represent [[Principle Component Analysis]]
- Calculate player's Elo, over time, solo or with team, with [[Expectation Propagation]]
- Programming language for probabilistic models: CSoft
