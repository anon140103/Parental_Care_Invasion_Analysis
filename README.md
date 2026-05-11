# Evolutionary Invasion Analysis Model for Parental Care

This repository contains the Mathematica notebooks used for the modelling work in my dissertation project on the evolution of parental care.

The code is organised into two main parts.

Part 1 focuses on finding the optimal life history strategy (i.e., combination of life-history traits which maximises the fitness of care and the optimal level of care within the strategy) for the evolution of care under different trade-off shapes.

Part 2 extends the analysis by introducing stochastic variation into individual life-history traits, varying one trait at a time to examine how stochasticity affects the evolution of parental care.

The notebooks are written in a step-by-step format. They include more intermediate steps and analysis than are presented in the final dissertation. This is because the notebooks were used not only to generate results, but also to help my understanding of each stage of the analysis.

Each section has it's own heading or sub-heading to make it easier to follow. 

## Part 1: Identifying the Optimal Life-History Strategy for the Evolution of Care

The Part 1 notebook contains the optimisation section of the model.

This notebook identifies the optimal strategy for the evolution of parental care under four different trade-off shapes.

The trade-off shapes considered are:

1. A linear trade-off.
2. An exponential non-linear trade-off.
3. A saturating non-linear trade-off.
4. A sigmoid non-linear trade-off.

Although only the exponential trade-off is presented in the dissertation, the analysis was carried out for all four trade-off shapes. The code for all four is included in this repository to show the full modelling process and to keep a complete record of the analyses that were explored.

The purpose of this part of the code is to establish the baseline optimal care strategy before stochastic variation is introduced.

In general, this section of the code:

1. Defines the deterministic version of the parental care model.
2. Sets up the different care trade-off functions.
3. Calculates invasion fitness systematically across the range of life-history combinations and across the care gradient.
4. Identifies the  strategy that results in the greatest fitness.
5. Compares how the optimal strategy changes across different trade-off shapes.
6. Produces the results that are later used as the basis for the stochastic analyses.

This part of the analysis is therefore the foundation for the rest of the project. It shows how care evolves under the optimised deterministic model before random variation is added to each trait.

## Part 2: Exploring the Effects of Stochastic Variation on the Evolution of Care

Part 2 consists of five separate Mathematica notebooks.

Each notebook focuses on stochastic variation in one life-history trait, with traits varied one at a time.

The five traits analysed are:

1. Egg death rate.
2. Juvenile survival.
3. Adult mortality.
4. Fecundity.
5. Maturation rate.


Each Part 2 notebook follows the same general structure. A single trait is allowed to vary stochastically, while the other traits are held constant. This makes it possible to isolate the effect of stochastic variation in each trait and compare how different life-history traits influence the evolution of parental care.

For each trait, the analysis is repeated across the three non-linear trade-off shapes:

1. Exponential.
2. Saturating.
3. Sigmoid.

The linear trade-off is not included because in Part 1 I found that linear trade-offs do not produce biologically realistic results within the parameter space I considered.

In general, each Part 2 notebook:

1. Defines the relevant trade-off shape.
2. Introduces stochastic variation into one focal trait.
3. Runs the model across the range of care values.
4. Generates a distribution of invasion fitness values at each level of care, reflecting variation in fitness caused by stochastic variation in the focal trait.
5. Summarises these fitness distributions using the mean and standard deviation at each care value.
6. Plots the mean and standard deviation of invasion fitness across the care gradient.
7. Uses the mean invasion fitness landscape to compare three key properties with the deterministic model: maximum fitness, the optimal level of care, and the point at which no-care reinvasion becomes possible.
8. Uses the standard deviation of invasion fitness to assess how sensitive fitness is to stochastic variation across the care gradient (or selective landscape). I do this by considering: the magnitude of SD at the fitness peak(as a % of max fitness), and the location of the maximum SD relative to the fitness peak.
9. Uses these outputs together to quantify how variation in each life-history trait affects the evolution of parental care.

The aim of these notebooks is not only to produce final figures, but also to break the analysis into clear stages. Many sections are included to make the logic of the analysis easier to follow, even where those intermediate stages are not included in the final project.

The dissertation presents only the most relevant parts of the analysis, but this repository keeps the fuller version of the computational work.

## Summary of Repository Structure

The repository contains:

1. One Part 1 notebook for the deterministic optimisation analysis.
2. Five Part 2 notebooks for stochastic variation in individual traits.


## Notes on File Format

The code is stored as Mathematica notebook files with the `.nb` extension.

These notebooks contain the code, outputs, and intermediate working used during the project.

They are intended to be opened and run in Wolfram Mathematica.
