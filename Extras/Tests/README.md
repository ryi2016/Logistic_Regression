# Logistic_Regression Workflow Tests



These tests were run at 2017-01-11 16:06:08



| id|name                         |status   |time           |message                  |
|--:|:----------------------------|:--------|:--------------|:------------------------|
|  1|LogisticTest1                |&#9989;  |8.443 seconds  |                         |
|  2|LogisticTest2                |&#9989;  |8.404 seconds  |                         |
|  3|LogisticTest3                |&#9989;  |7.723 seconds  |                         |
|  4|LogisticTest4                |&#9989;  |9.364 seconds  |                         |
|  5|LogisticTest5                |&#9989;  |12.940 seconds |3 warnings               |
|  6|LogisticTest6                |&#9989;  |15.040 seconds |2 warnings               |
|  7|LogisticTest7                |&#9989;  |18.009 seconds |2 warnings               |
|  8|logreg_and_linreg_cv_reports |&#9989;  |33.161 seconds |                         |
|  9|logreg_stepwise              |&#x274C; |31.840 seconds |2 errors and 11 warnings |
| 10|SampleTest                   |&#9989;  |8.535 seconds  |                         |


## UI Test Checklist.


1. Check that configuration persists. This includes widgets, tabs, pages, accordions, and pretty much any other ui element that the user interacts with. The configuration window should always.
2. Check navigation. This includes checking if pages show up correctly when the Customize/Back buttons are clicked. It is also important to check that persistence holds under these operations.
3. The `Customize` button should always appear.
4. Clicking on the `Customize` button should take the user to the second page.
5. Checking `Use a weighted variable ...` should bring up a dropdown to let the user select a weighting variable. This dropdown should be clearable. If the user checks this option, but does not select a weighting variable, then the workflow should display a configuration time error.
6. Checking the box in the upper left corner of the "Select the Predictor Variables" should check all the variables when checked for the first time on a fresh tool. Checking it again should uncheck all the variables.
7. A variable should show up under in the list of potential target variables if and only if it is a String, VString, WString, or VWString.
8. All words should be spelled correctly. Additionally, no config text should end in punctuation, and all config options should be in sentence case.
9. The option to use regularized regression should not display if an XDF input is connected to the tool. Neither should the option to use cross-validation.
10. The config options `Enter value of alpha` `Standardize predictor variables` and `Use cross-validation to determine model parameters` should display if and only if regularization is selected.
11. If regularization is selected, `Standardize predictor variables` and `Use cross-validation to determine model parameters` should be selected by default. Additionally, the report generated should be the appropriate type depending on whether regularization is used.
12. If `Use cross-validation to determine model parameters` is selected, the options `Simpler model` and `Set seed` should be selected by default. The default value of the seed should be 1. Additionally, the cross-validation graphs should appear in the R report if cross-validation is selected.
13. The options `Number of folds` `What type of model` and `Set seed` should display if and only if cross-validation with regularization is selected.
14. The slider under `Enter value of alpha` should prevent you from selecting a value less than 0 or greater than 1. If you type a value into the box or use the up/down widget to change the value of alpha, the slider should change its position accordingly.
15. `Use Cross-validation to determine estimates of model quality` should be unchecked by default. 
16. In the Cross-validation tab, `Number of folds`, `Number of trials`, `Set seed`, `Enter the positive class...` and `Use stratified cross-validation` should appear if and only if cross-validation is selected. If CV is selected, `Set seed` should be checked by default, and the default value of the seed should be 1. The default value for `Number of folds` should be 5, and the default for `Number of trials` should be 3.
17. The default graph resolution should be 1x.
