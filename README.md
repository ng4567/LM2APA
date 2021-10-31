# LM2APA

  This R package is used to create Microsoft Word documents containing graphs frequently used in checking Linear Regression model assumptions, and regression table outputs in APA format.

  The only function in the package is **make_lm_plots()**, and it takes the parameters: model, output_path, reg_table, reg_table_name 

* **model**: lm object to pass to the function
* **output_path**: path of where you would like the graphs to be saved 
* **reg_table**: binary variable to indicate if you would like the regression table to also be made (1=Yes, 2=no)
* **reg_table_name**: name of word document containing table (will be .doc not .docx)

# Example code 

If you want to include a regression table:

mod <- lm(mpg ~ wt, data = mtcars)
make_lm_plots(mod, "test.docx", 1, "table.doc")

No Regression table:

mod <- lm(mpg ~ wt, data = mtcars)
make_lm_plots(mod, "2.docx")
