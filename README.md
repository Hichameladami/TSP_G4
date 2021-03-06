# Heuristics for the TSP Problem
On this project we worked mainly on techniques that are more advanced than naive methods.
1-  `Greedy_2opt` is the combination of two algorithms the first one greedy for tour construction and the second one for tour improvement.

2- the second one is for the  `Nearest Neighbor method`.
## Greedy_2opt

In what follows we are going to apply a 2-step heuristic procedure to the solution of a TSP on a complete graph. The first step is to construct a feasible
solution and the second is to improve this solution.

A way of improving the current solution provided by the Greedy algorithm is the 2-opt technique. The 2-opt technique involves iteratively removing two edges and replacing these with two different edges that reconnect the fragments created by edge removal into a new and shorter tour.

The following R code implements the constructive and improving Greedy heuristic method and applies is in the file `Greedy_2opt.R` and `Greedy_2opt.cpp`.

Details on the heapsort algorithm can be found on [thisarticle (http://160592857366.free.fr/joe/ebooks/ShareData/Heuristics%20for%20the%20Traveling%20Salesman%20Problem%20By%20Christian%20Nillson.pdf). 
### Package installation

You first need to install the devtools package, it can be done easily from Rstudio. We install the package from Github :
```
devtools::install_github("Hichameladami/TSP_G4")
library(tspp)
```

### A first simple test 

we choose n=12 cities.
```
Greedy_2opt(12)
```

We will have an output of the following form, which explains the choice of the route. For this example `4->8->7->3->11->9->6->10->2->5->1`
```
[1] 4
[1] 8
[1] 7
[1] 3
[1] 11
[1] 9
[1] 6
[1] 10
[1] 2
[1] 5
[1] 1
[1] 69364.66
```
and at the end we choose the one with the lowest cost. 

we can proceed in the same way to call the function `Greedy_2opt.cpp`.


## Nearest Neighbor

One starts from an arbitrary summit from which one goes to the closest neighboring summit, then from this one to its closest non-visited neighbor, etc , until all the summits have been traversed, where one returns to the start.
### Example of execution :
in this example, we choose n=4 cities

![capture](https://user-images.githubusercontent.com/77694470/105101141-b573b300-5aae-11eb-881f-fc3f2c7c66ec.PNG)

## Built With

* [Article](http://160592857366.free.fr/joe/ebooks/ShareData/Heuristics%20for%20the%20Traveling%20Salesman%20Problem%20By%20Christian%20Nillson.pdf) - The web framework used


## Authors

* **EL JAMIY MOHAMED**
* **EL ADAMI HICHAM**
