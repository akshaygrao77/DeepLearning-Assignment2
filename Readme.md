
# Part A instructions  
### The following are instructions to execute code using command line
```
usage: ipykernel_launcher.py [-h] [-pgb] [-visfilters] [-cgbm] [-runbest]
                             {run_model} ...

positional arguments:
  {run_model}

optional arguments:
  -h, --help            show this help message and exit
  -pgb, --plot_guided_bp
                        Plot guided backprop on last model(call only after
                        running a model)
  -visfilters, --visualize_filters
                        Visualize filters of last model(call only after
                        running a model)
  -cgbm, --create_grid_model
                        Create grid for last model(call only after running a
                        model)
  -runbest, --run_best_model     
  ```
  ## Explanation of few functions in part A
  **cnn_Model() function:**   
  It accepts varies parameters are input and returns a model with architecture as specified in question 1   
  **dataset_Generators() function**    
  It returns train_dataset,test_dataset and validation_dataset after reshaping the image. It optionally augments the train data when argument passed is True   
  **HP_tuning_run() function**     
  This is the function called by wandb for hyper-parameter tuning   
  **run_best_model() function**   
  It trains and evaluates(on test data) the best model and returns the model and test_generator   
  **create_grid_from_best_model() function**   
  It creates a grid of test images prediction on model passed as arguments   
  **generate_guided_propogation_plots() function**   
  It generates graphs based on guided back propogation   
  **run_model() function**    
  Run a customized model passed as params   
  
  
  # Part B instrucions     
  ## Explanation of few functions in part B     
  **hyperparameter_run() function**   
  Runs hyper-parameter tuning on config file in notebook   
  **cnn_Model() function**     
  Returns a new model with base model as passed by arguments    
  **dataset_Generators() function**     
  Returns a train_dataset,test_dataset and validation_dataset iterator after reshaping the image. It optionally augments the train data when argument passed is True  
  
  # Part C instructions   
  
  Just play the video at this link: https://www.youtube.com/watch?v=jQQJmDkHdsQ  