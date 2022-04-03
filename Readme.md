
# Part A instructions  
## Entire assignment was done using google colab. However we provide options for CMD arguments as well    
  
### The following are instructions to execute code using command line   
```
usage: ipykernel_launcher.py [-h] [-pgb] [-visfilters] [-cgbm] [-runbest]
                             {run_model} ...

positional arguments:
  {run_model}
  
  arguments: the following are sub-arguments which follow the above "run_model" positional argument
  -h, --help            show this help message and exit
  --dropout DROPOUT     Specify dropout param
  --batch_norm BATCH_NORM
                        Specify batch normalization param
  --dense_layer_size DENSE_LAYER_SIZE
                        Specify number of neurons in dense layer param
  --conv_activations_conv CONV_ACTIVATIONS_CONV
                        Specify activation in convolution layer param
  --conv_activations_out CONV_ACTIVATIONS_OUT
                        Specify activation in output layer param
  --conv_activations_dense CONV_ACTIVATIONS_DENSE
                        Specify activation in dense layer param (mandatory argument)
  --filter_size_list FILTER_SIZE_LIST
                        Specify number of filters in each layer (mandatory argument)

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
  ## If command line call doesn't run a function of intension, then execute the follwing cell
  ## Execute the follwing commands in Google colab after executing all previous cells in Part_A.ipynb  for outputs if cmd not working
  **Go to cell with header "Execute below functions for outputs (comment the below cell it if command line is used for outputs)"**
**model,test_Generator = run_best_model()**
**pred_classes = {0: 'Amphibia', 1: 'Animalia', 2: 'Arachnida', 3: 'Aves', 4: 'Fungi', 5: 'Insecta', 6: 'Mammalia', 7: 'Mollusca', 8: 'Plantae', 9: 'Reptilia'}**
**images, labels = test_Generator.next()**
**predictions = model(images)**
**create_grid_from_best_model(model,test_Generator,pred_classes,images,labels,predictions)**
**visualize_filter_of_best_model(model)**
**generate_guided_propogation_plots()**
  
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
