1. File naming
* use lowercase;
* use dash or underscore to link words;
* with extension `.R`.

  e.g.: `eda.R`, `lin_reg.R`.

2. Variable naming
* use lowercase typically;
* use uppercase for global constant;
* use nouns and numbers;
* use underscore to link words.

  e.g.: `lin_reg_model1`, `train_data`, `preditors1`.
 
3. Functions
* use CamelCase as function name;
* use verbs and nouns as function name;
* `return()` clause is not necessary in function body.

  e.g.: `tuningRandomForest()`, `getTestErr()`.
  
4. Spacing
* use spaces around all binary operators, `r <- 2`, `x + y`, `x %in% predictors`;
* always place a space after a comma, `df[1, ]`, `df[, 1]`;
* always place a space before a left parentheses, `if (x <= 3)`.

5. Curly brace
* Opening curly brace does not go on its own line;

6. Assignment
* use `<-`.

7. Organizing
* use `###` for head;
* use `----` or `====` to separate code chunks

8. Indent
* typically use two spaces to indent;
* disable vertically align arguments in auto-indent.
