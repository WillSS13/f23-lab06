# f22-rec06

## Task 1
Uses the anti-pattern "Feature Envy" as the function isOccupied() accesses the boolean[] occupied and then performs actions on it. Solved this by adding a function isOccupied(int position) to Road which is called in Frogger making it so that Frogger does not access the fields of Road.

## Task 2
Uses the anti-patter "Long Parameter List" since there are multiple locations that share identical groups of variables. This group of variables gets moved into a record called FroggerId. Now, instead of the Frogger storing all of its information in separate variables, it is all stored in the FroggerId id record. Plus, Records reduces the paramters for addRecord() as it only needs the FroggerId.

## Task 3
1. The "draw" function seems to duplicate itself. How would you refactor it so that we don't need to rewrite the functionality everytime we introduce a new file type?

   *Extract lines 35-39 and 45-49 to a new function called fileDraw(Writer w). Then, all the draw function has to do to implement a new file type is initialize the writer with the correct file type and call the fileDraw function.*

2. Somewhere inside the "draw function", the code seems to be explicitly creating an array of Lines and feeding it to the shape. How would you refactor it so that we don't need to expose and rely on such information inside our Drawing class?

    *I would remove the array of lines in the Drawing class then alter the draw function in the Shape class to not take in the parameter. Instead of using the parameter, the draw function will call its toLines() function on itself which it then loops through.*