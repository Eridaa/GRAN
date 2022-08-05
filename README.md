
# GRAN

PyTorch implementation of [Efficient Graph Generation with Graph Recurrent Attention Networks, tested for generating street networks

### Run the Dataset creation from osmnx.ipynb notebook for creating custom datasets.

## Dependencies
Python 3, PyTorch(1.2.0)

Other dependencies can be installed via 

  ```pip install -r requirements.txt```


## Run Demos

### Train
* To run the training of experiment ```X``` where ```X``` is gran_Cities.yaml:

  ```python run_exp.py -c config/X.yaml```
  

**Note**:

* Please check the folder ```config``` for a full list of configuration yaml files.
* Most hyperparameters in the configuration yaml file are self-explanatory.

### Test

* After training, you can specify the ```test_model``` field of the configuration yaml file with the path of your best model snapshot, e.g.,

  ```test_model: exp/gran_grid/xxx/model_snapshot_best.pth```	

* To run the test of experiments ```X```:

  ```python run_exp.py -c config/X.yaml -t```

**Note**:

* Please check the [evaluation](https://github.com/JiaxuanYou/graph-generation) to set up.



```
@inproceedings{liao2019gran,
  title={Efficient Graph Generation with Graph Recurrent Attention Networks}, 
  author={Liao, Renjie and Li, Yujia and Song, Yang and Wang, Shenlong and Nash, Charlie and Hamilton, William L. and Duvenaud, David and Urtasun, Raquel and Zemel, Richard}, 
  booktitle={NeurIPS},
  year={2019}
}
```



