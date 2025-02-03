# ICR - Identifying Age-Related Conditions

## Folders
* data - train files 

* Draft Notebooks - several notebooks that I used for inspect different configurations and methods.

* Notebooks - some of the best notebooks I used.

* TabPFN_files - files that intended to help us use the TabPFN model insode Kaggle notebooks (instruction later)

## notebooks description

* best_all-models - PowerTransformer + Best TabPFN configuration -> 0.355

* a_all-models - PowerTransformer + Best XG depth configuration + reweight after prediction -> 0.363

* b_all-models - PowerTransformer + Best XG depth configuration -> 0.368

* c_all-models - PowerTransformer -> 0.387

* d_all-models - StandatdTransformer + Best XG depth configuration -> 0.395

* e_all-models - StandatdTransformer + 0.55 weight for TabPFN -> 0.398

* f_all-models - StandatdTransformer + 0.55 weight for TabPFN + best LGB -> 0.400

* KNN - K = 56, remove 89% of highest varianced columns -> 0.783

* n-networks - 3 layers, drop 10% of highest varianced columns -> 0.741

* RandomForest - best configuration model -> 0.442

## How to run?

- `all-models` files : Since TabPFN isn't recogized in kaggle environment - We needed to upload it's wheel file and checkpoint file which located in the folder TabPFN_files in order to perform pip install command.
Therefore, few steps needs to be done:

  1) Create a folder inside the notebook called - "datasets"
  2) Create a folder inside "datasets" called "tabpfn" abd upload TabPFN wheel to it. (relative path should be "datasets/tabpfn/tabpfn-0.1.9-py3-none-any.whl).
  3) Create another folder inside "datasets" called "checkpoint" and upload TabPFN checkpoint file to it, that's a saved state of the pre trained module that we use in our code(relative path should be "datasets/checkpoint/prior_diff_real_checkpoint_n_0_epoch_100.cpkt).
  4) RUN!

- Other files: just run!



