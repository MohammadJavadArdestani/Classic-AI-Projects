# Classic AI Projects


## Table of Contents
* [NLP Persian Poet Identification](https://github.com/MohammadJavadArdestani/Classic-AI-Projects/edit/main/README.md#nlp-persian-poet-identification-link)
* [Solve Sudoku as a Constraint Satisfaction Problem ](https://github.com/MohammadJavadArdestani/Classic-AI-Projects/edit/main/README.md#solve-sudoku-as-a-constraint-satisfaction-problem-link)
* [Sort Clored Cards with AI Search Algorithms](https://github.com/MohammadJavadArdestani/Classic-AI-Projects/edit/main/README.md#sort-clored-cards-with-ai-search-algorithms-link)

## NLP Persian Poet Identification [[link]](https://github.com/MohammadJavadArdestani/NLP-persian-poet-identification)
In this NLP project, model get a line from one of three famous Iranian poets(Ferdowsi, Hafez, and Molavi), and predicts the poet name as output.<br>
we use a unigram and a bigram model trained on a dataset which contains over 9 thousand lines of poems for each poet.<br>
The probability calculates by backoff model like the following:
```bash
P`(ci | ci-1) = [(y3 * P(ci | ci-1)) + (y2 * P(ci)) + (y1 * e)] 
y1 + y2 + y3 = 1 
0 < e < 1 
```
After tuning the above parameter, I got accuracy= 91. % by following parameters: 
```bash
y1 = 0.05
y2 = 0.1
y3 =0.85
e = 10 ^-6 
```

To access the code and the dataset, click [Here](https://github.com/MohammadJavadArdestani/NLP-persian-poet-identification).

## Solve Sudoku as a Constraint Satisfaction Problem [[link]](https://github.com/MohammadJavadArdestani/solve-sudoku-by-CSP)
Here we have two kinds of sudoku puzzles first one is just a numeric n*n table, and the other one contains colored cells.
We solve tables as a CSP problem using the Backtrack algorithm with forward-checking and MRV and Degree heuristics.
#### Normal Sudoku
There is just one rule here: Each number should be unique in its row and column.

#### Colored Sudoku
1- Each number should be unique in its row and column.<br>
2- Each cell must contain a color s.t for every two adjacent cells. If a cell has a greater number, then its color should have more priority over that adjacent

To access the code and more details, click [Here](https://github.com/MohammadJavadArdestani/solve-sudoku-by-CSP).

## Sort Clored Cards with AI Search Algorithms [[Link]](https://github.com/MohammadJavadArdestani/sort-colored-cards-with-AI-search-algorithms)
Here I used A*, IDS, and BFS to sort colored cards in ascending order.
In the initial state, we have different unsorted decks of cards (they could have different colors), and as output, you get sorted cards with the same color in each deck.
You can run the same test case on each algorithm to understand the great effect of the heuristic function on decreasing computation time by creating fewer nodes than BFS and IDS.<br>

To access the code and more details, click [Here](https://github.com/MohammadJavadArdestani/sort-colored-cards-with-AI-search-algorithms).
