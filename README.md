# f22-rec06

## Task 1
Uses the anti-pattern "Feature Envy" as the method isOccupied() accesses the boolean[] occupied and then performs actions on it. Solved this by adding a method isOccupied(int position) to Road which is called in Frogger making it so that Frogger does not access the fields of Road.

## Task 2

## Task 3