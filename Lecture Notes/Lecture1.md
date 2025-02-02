# Lecture 1 Notes (Monday - 20th Jan)

## 01 - Introduction 

AI is the study of intelligent agents that do the following: 
- Perceive an environment
- Perform actions to achieve some sort of goal.

What is an intelligent agent?
- The perception of the environment is done through sensors
- The actions performed on the environment is done through actuators


Generally, the way an **intelligent agent** works is as follows: 

```
function[input] = output
```

The ```input``` is something that is *perceived* in the environment. The ```output``` is an action that is performed on the environment. This is like a cycle. You can draw a nice figure out of this (I'll do this later)

Now on the side of the intelligent agent, how does it map the sensory input to the actuators? This is what we'll study. 

### Examples of intelligent agents
- Most act within this perception-action cycle. There's loads of them. One example is route finding, constraint satisfaction agents, etc...
- **Bayesian Network**: The environment contains random variables and conditional probability values. The agent performs probabilistic inference, so it's no longer definite perceptions being mapped to definitive actions. It's all based on probability.

### Types of **environments**: 
- Observation: Full vs. Partial:
  - Fully observable means that the agent is aware of all the variables in the environment at the current time. An example of this would be a game of chess. Entire board is visible to both players
  - Partially observable means that the agent does not have access to the complete *current* state of the environment
-  Deterministic vs. Nondeterministic:
  - Deterministic means that the next state of the environment depends entirely on the current state **only**.
  - Nondeterministic means that the actions of the agent cannot be predicted based on only the current state. It could lead to multiple possible outcomes. An example of this would be self-driving cars.
- Discrete vs. Continuous:
  - Discrete means that there is a finite, countable number of states. Again, like a game of chess.
  - Continuous means that there is an infinite number of states. Anything could happen. Again, self-driving cars.
- Static vs. Dynamic:
  - Static means that the environment does not change while an agent is "thinking" of what to do.
  - Dynamic means that the environment **can** change.
- Benign vs. Adversarial:
  - Benign basically means that the environment is friendly. There's nothing working **against** the AI agent.
  - Adversarial means that there is an active opposition to the agent. Like two player games (chess, again).
 
What is the structure of an AI agent? 
```
agent = architecture + program
```
- The agent architecture consists of sensors and actuators.
- The program implements the mapping from the sensors to the actuators.

### Types of agent **programs**:
- Simple reflex agents: Responding directly to the actions that are perceived. This is the simplest type of AI agent. It's basically an ```if, then``` cycle.
- Model-based reflex agents: Maintain an internal state to track aspects of the environment, because there are some aspects that may not be currently visible in the environment.
- Goal-based agents: They have a goal. They need to achieve it.
- Utility-based reflex agents: Optimizing some sort of utility function. They make decisions based on how "useful" it is. It's more flexibile and can handle more diverse situations.
- 

## 02 - Solving Problems by Searching
Let's say you have a map. How do you pick the best route given a starting state and a goal state? This is the essence of what we are doing in this lecture. Determining the "best" set of decisions that lead to a goal state. Let's first go through the concept of problem formulation: 

A search problem is defined by the following 5 items: 
```
1. initial state
2. Actions: Given a state s, Actions(s) returns the set of actions that can be executed in the state s
3. Transition model: Result(s,a) returns the state that results from doing an action a in state s
4. Goal test: bool goal_test(s) determines whether we are at the goal state or not. T/F
5. Path cost: c(s, a, s') is the cost of performing an action in state s to get to state s'. Assumed non-negative. 
```
The **solution** is a sequence of actions $(a_1, a_2, ..., a_g)$ that lead to the goal state. The set of all states is called the state space. 

### Search algorithms: 
 

