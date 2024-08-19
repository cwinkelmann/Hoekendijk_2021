

====== README ====== 

 The documents provided here supplement the paper "Counting using deep learning regression gives value to ecological surveys",
 by Hoekendijk et al. (2021), published in Scientific Reports.


====== IMAGES ====== 

 All images are available on request


====== ANNOTATIONS ====== 

 You can also find the corresponding .CSV files with image-level annotations, which include:

 For the otolith application:
  * Labels_and_predictions_Otolith_test_set.csv
  * Labels_Otolith_training_and_validation_set.csv

 For the seal application:
  * Labels_and_predictions_Seal_test_set.csv
  * Labels_Seal_Remaining_main_dataset.csv
  * Labels_Seal_subset_1.csv
  * Labels_Seal_subset_1_and_2.csv

  - Note that the CSV files for the test sets also include the predictions made by the models. 
  - 'Labels_Seal_subset_1_and_2.csv' includes the labels of both seal subset 1 and 2 combined.
  - 'Labels_Seal_Remaining_main_dataset.csv' includes the noisy labels of the remaining main dataset, after the 
    'Seal test set' and 'Seal subset 1' have been removed, but it still includes the noisy labels (i.e. before recounting)
    of 'Seal subset 2', so that the experiments in the paper can be repeated in their entirety.


====== CODE AND MODELS ====== 

 Finally, you can find the code and various trained models, as described in the paper.

 * 'Hoekendijk_et_al_Code.ipynb' is the code (JupyterNotebook) used for all experiments in the paper. 
   It also includes an example output for the otolith application. 

 For the otolith application:
 * Otolith_Stage_1.pth is the best performing model for the otolith application after stage 1
 * Otolith_Stage_2.pth is the best performing model for the otolith application after stage 2

 For the seal application:
 * Seal_Step_1_model_Stage_1.pth is the best performing 'Step 1 model' for the seal application after stage 1
 * Seal_Step_1_model_Stage_2.pth is the best performing 'Step 1 model' for the seal application after stage 2
 * Seal_Step_2_model.pth is the best performing 'Step 2 model' for the seal application after stage 2

Nb:
During Stage 1, the network is frozen, and only the added layers are trained (see paper and code).
During Stage 2, the network is unfrozen, and all layers are trained (see paper and code).
