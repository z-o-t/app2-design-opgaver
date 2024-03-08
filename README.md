# Learning outcome
Knowledge about algorithms, datastructure and common programming paradigme. 

## Purpose
The purpose of this branch is to test your knowledge about algorithm, datastructure and programming paradigm. 

## Goal
This gives you a indication of wether you have a sufficient understanding of the subjects and wether you should be aware of some pit in your knowledge. 


# Part 1 - Algorithms
## What is the key difference between a functions and algorithm?

## The following code example, why is it a algorithm and why is it not?

```PYTHON
import numpy as np


def Possibility(x,y,n) :
    global Box
    if Box[x][y] == 0 :
        for i in range(9) :
            if Box[x][i] == n :
                return False
        for j in range(9) :
            if Box[j][y] == n :
                return False
        r = x
        c = y
        boxx = 0
        boxy = 0
        while r - 3 >= 0 :
            r = r - 3
            boxx = boxx + 1
        while c - 3 >= 0 :
            c = c - 3
            boxy = boxy + 1
        for i in range(3) :
            for j in range(3):
                if Box[i+boxx*3][j+boxy*3] == n:
                    return False
        return True

def Solve() :
    global Box
    for r in range(9):
        for c in range(9):
            if Box[r][c] == 0:
                for n in range(1,10):
                    if Possibility(r,c,n) == True:
                        Box[r][c] = n
                        if Solve() == False:
                            Box[r][c] = 0
                        else :
                            return True
                return False

Box = [
    [5, 0, 0,   6, 7, 0,    9, 0, 0],
    [0, 4, 0,   8, 0, 0,    0, 0, 0],
    [8, 0, 0,   5, 0, 0,    6, 1, 3],

    [0, 6, 2,   4, 0, 0,    0, 7, 0],
    [1, 0, 0,   0, 0, 3,    0, 2, 0],
    [3, 7, 4,   9, 0, 8,    0, 0, 0],

    [0, 9, 6,   1, 0, 7,    8, 0, 2],
    [2, 1, 8,   0, 0, 6,    0, 4, 5],
    [0, 5, 0,   0, 8, 0,    0, 9, 0]
    ]

Solve()
print(np.matrix(Box))
    


```

# Part 2 - Datastructure

## What is the primary difference between datastructure and datatypes?

## Name three datastructures 

### What are the strength

### What are the weakness

### What are the difference

### What are the simalarities

# Part 3 - Paradigm

## What is a programming paradigm?

## Compare two paradigms
