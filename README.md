# Scalable-Imputation-Technique-for-Effective-Computation-of-Missing-Battery-Parameters
 ## :paperclip: Overview

•	Modelling contains implementation of the following models: </br>
	o	Saits (saits.py) </br>
    o	Brits (brits.py) </br>
    o	Mrrn (mrrn.py)  </br>
    o	Transformer(transformer.py) </br>
    
•	Data Pre-processing steps are covered in Data-Preprocessing. </br>
    &ensp; All the datasets used are included in Datasets.
    
•	Configs includes configurations of different models.
 
**:round_pushpin:Code has been executed in Google Colaboratory.**

 -------------------------------------------------------------------------------------------------------------------

 ### :paperclip: The code excecution has 3 parts : </br>
 
 i)	Generating Dataset : ` python gene_battery_dataset.py ` </br>
ii)	Model training:  ` CUDA_VISIBLE_DEVICES=0 python run_models.py --config_path configs/Battery_SAITS_best.ini ` </br>
iii)	Model testing: ` CUDA_VISIBLE_DEVICES=0 python run_models.py --config_path configs/Battery_SAITS_best.ini --test_mode ` </br>

--------------------------------------------------------------------------------------------------------------------------

### :paperclip: Steps to be followed to run the code:

•	Download the code and unzip it. </br>
•	Upload the code to google drive and mount the drive.  </br>
•	First generate the required dataset (change the file paths of datasets and saving dirs in `gene_battery_dataset.py`, as it is may be different on personal computers).  </br>
•	Select a model and Train it (:pushpin: Change the `[file_path]` , `[dataset]` as it is on your personal computer in :file_folder: `cofigs/Battery_SAITS_best.ini`).  </br>
•	Test the model (:pushpin: before testing update the `model_saving_dir` , `Test_Result`  in :file_folder: `cofigs/Battery_SAITS_best.ini`).  </br>

-----------------------------------------------------------------------------------------------------------------------------
:round_pushpin: Results are saved in :file_folder: `NIPS_results/Battery_SAITS_best/Test_Result`.
