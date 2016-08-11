# Logistic_Regression

This folder contains the macro backend and associated files for the **Logistic_Regression** tool in Alteryx. Shown below is a brief description of the contents. 

| File                   | Description                                       |
|----------------------  |---------------------------------------------------|
| Data/                  | Data files needed for macro to run as workflow    |
| Supporting_Macros/     | Auxilliary macros used inside the main macro      |       
| Logistic_Regression.yxmc  | Main macro for the plugin                         | 
| Logistic_Regression1.R    | R code used in the R Tools contained in the macro |
| Help                   | Help                                              |


#### Usage

__R Code__

1. Edit `Logistic_Regression1.R` to update the logic of the tool. 
2. Use the [style guide](Style_Guide.md) while writing your R code. 
3. Use the `Data` folder to store any data used. 
4. Run `insertRcode("Logistic_Regression.yxmc", "Logistic_Regression1.R")` to insert R code back into the macro. Note that you will have to close and reopen the macro for the changes in the R tool to take effect.

#### Configuration Parameters

This configuration is autogenerated from `Logistic_Regression.yxmc`.



|dataName         |label                            |default |values                                       |
|:----------------|:--------------------------------|:-------|:--------------------------------------------|
|Model Name       |Model Name                       |        |                                             |
|Y Var            |Select the target variable       |        |                                             |
|X Vars           |Select the predictor variables   |        |                                             |
|Link             |Model type                       |logit   |["logit", "probit", "complementary log-log"] |
|Use Weights      |                                 |false   |                                             |
|Weight Vec       |Select the sampling weight field |        |                                             |
|graph.resolution |Graph Resolution                 |1x      |["1x", "2x", "3x"]                           |