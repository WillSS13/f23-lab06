# f22-rec06

## Task 1
Uses the anti-pattern "Feature Envy" as the method isOccupied() accesses the boolean[] occupied and then performs actions on it. Solved this by adding a method isOccupied(int position) to Road which is called in Frogger making it so that Frogger does not access the fields of Road.

## Task 2
Uses the anti-patter "Long Parameter List" since there are multiple locations that share identical groups of variables. This group of variables gets moved into a record called FroggerId. Now, instead of the Frogger storing all of its information in separate variables, it is all stored in the FroggerId id record. Plus, Records reduces the paramters for addRecord() as it only needs the FroggerId.

## Task 3
