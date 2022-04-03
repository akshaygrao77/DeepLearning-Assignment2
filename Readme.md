
# Part A instructions  
# Output Execution using command lines and CMD (part_a.py)
**There are two files for Part A execution i) part_a.py in Part_A folder or  Part_A.ipynb. you can execute either of them for outputs**
## Entire assignment was done using google colab. However we provide options for CMD arguments as well by using part_a.py in Part_A folder
  
### The following are instructions to execute code using command line  
**download part_a.py and mount the path where file is downloaded**<br />
## Install required pakages like keras,Tensorflow etc and  execute below three command lines **<br />
**pip install wandb**<br />
**wandb login**<br />
**pip install wget**<br />
**python part_a.py -h**<br />
**below is the usage of diiferent cmd commands to get the respective outputs**<br />
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
  # Output Execution using google colab (Part_A.ipynb )
  # Run all cells in Part_A.ipynb to get outputs(last before two cells output) and ignore last two cells (cmd args)
  ## If command line call doesn't run a function of intension, then execute the follwing cell
  ## Execute the follwing commands in Google colab after executing all previous cells in Part_A.ipynb  for outputs if cmd not working
  **Go to cell with header "Execute below functions for outputs (comment the below cell it if command line is used for outputs)"**
**model,test_Generator = run_best_model()**<br />
**pred_classes = {0: 'Amphibia', 1: 'Animalia', 2: 'Arachnida', 3: 'Aves', 4: 'Fungi', 5: 'Insecta', 6: 'Mammalia', 7: 'Mollusca', 8: 'Plantae', 9: 'Reptilia'}**<br/>
**images, labels = test_Generator.next()**<br />
**predictions = model(images)**<br />
**create_grid_from_best_model(model,test_Generator,pred_classes,images,labels,predictions)**<br />
**visualize_filter_of_best_model(model)**<br />
**generate_guided_propogation_plots()**<br />
   ## Execute the follwing commands in Google colab for (test data) output and accuracies
   **model,test_Generator = run_best_model()**<br />
**pred_classes = {0: 'Amphibia', 1: 'Animalia', 2: 'Arachnida', 3: 'Aves', 4: 'Fungi', 5: 'Insecta', 6: 'Mammalia', 7: 'Mollusca', 8: 'Plantae', 9: 'Reptilia'}**<br/>
**images, labels = test_Generator.next()**<br />
**predictions = model(images)**<br />
   **create_grid_from_best_model(model,test_Generator,pred_classes,images,labels,predictions)**<br />
   ## Execute the follwing commands in Google colab visualizing filters and guided back propogation
**visualize_filter_of_best_model(model)**<br />
**generate_guided_propogation_plots()**<br />
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
