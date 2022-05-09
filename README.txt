Il progetto è strutturato in due file:
-"frcnn_graspD_train", per il training della rete
-"frcnn_graspD_test", per la validazione dei risultati

"frcnn_graspD_train" ha il compito di salvare i file:
-"model_vgg_config.pickle", contenente la configurazione utilizzata 
-"rpn_model.h5", "cls_model.h5", "grp_model.h5" contenente i modelli salvati durante il training
-"record.csv" utilizzato per salvare i dati ottenuti durante il training (loss, accuracy, ecc.)

"frcnn_graspD_test" utilizzerà poi questi file per poter valutare le performance della rete sul test set.

-Organizzazzione cartelle:
I due file .ipynb accedono al filesystem attraverso due variabili, "dataset_path" e "base_path" :

base_path = './myFolder/Project'
dataset_path = './myFolder/VMRDv2/'

[+]myFolder
 |------[+]Project
 |	 |------frcnn_graspD_train.ipynb
 |	 |------frcnn_graspD_train.ipynb
 |	 |------model_vgg_config.pickle
 |	 |------[+]model
 |		 |------rpn_model.h5
 |		 |------cls_model.h5
 |		 |------grp_model.h5
 |		 |------record.csv
 |	 	 |------vgg16_weights_tf_dim_ordering_tf_kernels.h5
 |
 |------[+]VMRDv2

P.S.
In caso di problemi con i packages utilizzati è presente il file "tf_gpu.yml" per replicare l'enviroment utilizzato			 