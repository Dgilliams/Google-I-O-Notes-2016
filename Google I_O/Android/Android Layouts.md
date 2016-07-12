# Android Layouts: A whole new world
Friday May 20, 2016

Constraint Layout Speakers
- Nicolas Roard @Camaelon
- John Hoford @johnhoford

# Layouts
- 5400 combinations of layouts
- Simple layouts lead to nesting
  - nesting leads to performance issues
- Complex layouts can be hard to use or maintain

## Constraint Layout
- works back to gingerbread
- Why not RelativeLayout?
  - ConstraintLayout is a superset
  - more expressive, less nesting
  - unbundled library
  - Extensible
  - comes with a great UI builder

## A new platform for layouts
- Constraints
- Equations
- Solver

## The constraint model
- connection
- Baseline
- Center and Bias

## XML soooo many attributes
- app:layout_constraintLeft_toLeftOf="@+id/activity_main"

## UI Builder
- 2 way editiding
- direct integration into studio
- immediate feedback, easy to use
- in active deployment

## Notes
- Small library 100kb
- Ubundled library
- compatible with 99.9% of devices (API 9)
- Interface creates connections
- Manual edition - you are in control

## What's next?
- Improving performance
- guideline objects!
  - great for calculations and more detailed layouts
- Automatic optimizations
- Containers are coming
- Machine learning to learn from the layouts and tools they already have
- 
