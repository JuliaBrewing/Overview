# JuliaBrewing Overview

This is not a package repository. It is initially a placeholder for ideas for the general development of the packages in JuliaBrewing. Eventually, it should tend more to contain an overview of the packages available in JuliaBrewing.

## Packages

### JuliaBrewingLogo

This is easy. It should be the repository with the code for generating the would-be logo for JuliaBrewing org, in [Luxor.jl](https://github.com/JuliaGraphics/Luxor.jl).

### UnitfulBrewing.jl

This should define the necessary units for brewing, such as bitterness, color, gravity/sugar content. It is an extension to [Unitful.jl](https://github.com/PainterQubits/Unitful.jl). It is under-development.

### BrewingCore.jl

This should have all the types and conversion functions needed to build a recipe, but not the recipe builder yet.

The basic stuff I can think of are the following

* Ingredient
* Equipment
* Process

### Simple recipe builder/planner/designer (name?)

BrewingDesigner.jl? or BrewingRecipe.jl?

It should be for designing a straight-up traditional brewing recipes, with a single mash, boil, fermentation, and packaging.

mash -> sparge -> boil -> ferment -> package

### Complex recipe builder/planner/designer (name?)

BrewingGraph.jl?

For designing more complicate types of recipes, in the form of planar digraphs, so we could have multiple mashes, boils, fermentations, packagings, etc.

This would include parti-gyle, double-mashing, refermentations, and so on.

### BrewingProcess.jl

For managing actual brews being made and keep a record of those that have been made. This is a long-term project, after the others are complete.

### GUI

Initially the recipe builder above will not have a GUI. That is a different step. Ideally I think they should be separate packages that use the previous packages.

## Comments

The recipe builders should add

* An **Inventory**, containing
  * a List of ingredients;
  * a List of Equipments;

and

* A **Library of Recipes**.
