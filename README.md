# Regex to minimized DFA :cyclone:
## a fully functional Regex :point_right: NFA :point_right: DFA :point_right: min DFA generator and vizualizer

This project was an assignment for the compilers' course, written in python.
graph theory students might as well take a look.

Regex rules are the normal modern rules which are:

| Rule               | Example       |
| :---               |    :----:     |
| Concatenation      | ab            |
| ORing              | a | b         |
| Zero or One | a? |
| Zero or more | a* |
| One or more | a+ |
| Character or Num Classes | [123ab] |
| Ranges | [a-zA-Z0-9] |
| escaping characters | a/*b |
| escaping inside class | [ab*e] |


![phpxKQIRD](https://github.com/aymanreda56/RE-to-minDFA/assets/58632281/f1b8e54f-57a9-4a74-9fa2-9e77fdfd25b4)

---

## how to Run ? :crystal_ball:
* Navigate to the input cell in the bottom of the notebook
```
#@title input your Regex here
Input_Regex = "a/*bm/+" #@param {type:"string"}
nfa_graph, dfa_graph, cleanDFA_graph, minDFA_graph = CompileRegex(Input_Regex)
```
* Write your input regex as a string
* Run all
* Voila

---

## Outputs :art:
* NFA graph
* DFA graph
* Cleansed DFA graph (petty printed)
* minimized DFA graph
* NFA.json
* minDFA.json
---
## Overview :eyeglasses:
first we use shunting yard algorithm to parse the input regex into some states.
We tried to avoid recursions as much as possible so we used iterative stack-based methods

second we interpret those states to build a NFA using a very simple switch statement

third we implement the Powerset Algorithm to get a DFA out of the NFA

fourth we implement the Lower-Triangle method to get the minimized DFA, this lower triangle method just iteratively checks for state which CANNOT be equivalent and marks them all, after 2 consecutive iterations of no changes in the matrix, we can safely merge the theoritically equivalent states.

---

## Theory :tea:
For some in-depth explanations you can refer to my playlist [in Arabic] from here:
https://youtube.com/playlist?list=PLT7hbSdLHIDXpkQZo8meEKPad3jJQoi0m



