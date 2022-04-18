# Scalable-Imputation-Technique-for-Effective-Computation-of-Missing-Battery-Parameters
 ## :paperclip: Overview

•	[`Modeling`](https://github.com/Niharikajo/self-attention-based-imputation-technique/tree/main/modeling) contains implementation of the following models: </br>
    o   Self Attention Imputation [`SA_models.py#L93`](https://github.com/Niharikajo/self-attention-based-imputation-technique/blob/main/modeling/SA_models.py#L93) </br>
    o	MRNN [`mrrn.py`](https://github.com/Niharikajo/self-attention-based-imputation-technique/blob/main/modeling/mrnn.py)  </br>
    o	Transformer [`SA_models.py#L28`](https://github.com/Niharikajo/self-attention-based-imputation-technique/blob/main/modeling/layers.py#L28) </br>
    
•	Data Pre-processing steps are covered in [`Data-Preprocessing`](https://github.com/Niharikajo/self-attention-based-imputation-technique/tree/main/Data_Preprocessing). </br>
    &ensp; All the datasets used are included in [`Datasets`](https://github.com/Niharikajo/self-attention-based-imputation-technique/tree/main/Data_Preprocessing/Datasets).
    
•	[`Configs`](https://github.com/Niharikajo/self-attention-based-imputation-technique/tree/main/configs) contains configurations of different models.
 
**:round_pushpin:Code has been executed in Google Colaboratory.** [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1QSQ70DDeuKo0cKzIP6YOF7Hl8BBpsnyL#scrollTo=RVXApi9zT4q1)

 -------------------------------------------------------------------------------------------------------------------

 ### :paperclip: The code excecution has 3 parts : </br>
 
 i)	Generating Dataset : ` python gene_battery_dataset.py ` </br>
ii)	Model training:  ` CUDA_VISIBLE_DEVICES=0 python run_models.py --config_path configs/Battery_Self-Attention_best.ini ` </br>
iii)	Model testing: ` CUDA_VISIBLE_DEVICES=0 python run_models.py --config_path configs/Battery_Self-Attention_best.ini --test_mode ` </br>

--------------------------------------------------------------------------------------------------------------------------

### :paperclip: Steps to be followed to run the code:

•	Download the code and unzip it. </br>
•	Upload the code to google drive and mount the drive.  </br>
•	First generate the required dataset (change the file paths of datasets and saving dirs in [`gene_battery_dataset.py`](https://github.com/Niharikajo/self-attention-based-imputation-technique/tree/main/Data_Preprocessing/gene_battery_dataset.py), as it is may be different on personal computers).  </br>
•	Select a model and Train it (:pushpin: Change the section [`[file_path]`](https://github.com/Niharikajo/self-attention-based-imputation-technique/blob/main/configs/Battery_SAITS_best.ini#L1) , [`[dataset]`](https://github.com/Niharikajo/self-attention-based-imputation-technique/blob/main/configs/Battery_SAITS_best.ini#L14) as it is on your personal computer  in</br>  :file_folder: [`cofigs/Battery_SAITS_best.ini`](https://github.com/Niharikajo/self-attention-based-imputation-technique/blob/main/configs/Battery_SAITS_best.ini).  </br>
•	Test the model (:pushpin: before testing update the `model_saving_dir` , `Test_Result`  in </br> :file_folder: [`cofigs/Battery_SAITS_best.ini`](https://github.com/Niharikajo/self-attention-based-imputation-technique/blob/main/configs/Battery_SAITS_best.ini).  </br>

-----------------------------------------------------------------------------------------------------------------------------
:round_pushpin: Results are saved in :file_folder: `NIPS_results/Battery_Self-Attention_best/Test_Result`.

--------------------------------------------------------------------------------------------------------------------------

## Acknowledgments 
We appreciate the following github repository a lot for their valuable code base </br>
https://github.com/WenjieDu/SAITS

Dataset source : Diao, W., Saxena, S., Pecht, M. Accelerated Cycle Life Testing and Capacity Degradation Modeling of LiCoO2 -graphite Cells. J. Power Sources 2019, 435, 226830. </br>
https://web.calce.umd.edu/batteries/data.htm
