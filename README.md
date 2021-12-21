<div align="center">
<h1>Poseformer Plus and Domain adversarial STS-GCN</h1>
<h3> <i>Sazan Mahbub, Chuong Huynh, Jayesh Jayashankar and Aswath Muthuselvam</i></h3>
 <h4> <i>Sapienza University of Maryland, College Park</i></h4>
 

<div align="center"> <h3> Abstract </h3>  </div>
<div align="justify">

</div>
--------


 ### Install dependencies:
```
 $ pip install -r requirements.txt
```
 
 ### Get the data

[Human3.6m](http://vision.imar.ro/human3.6m/description.php) in exponential map can be downloaded from [here](http://www.cs.stanford.edu/people/ashesh/h3.6m.zip).
 
Directory structure: 
```shell script
H3.6m
|-- S1
|-- S5
|-- S6
|-- ...
`-- S11
```

```
Put the all downloaded datasets in ../datasets directory.

### Train
The arguments for running the code are defined in [parser.py](utils/parser.py). We have used the following commands for training the network,on different datasets and body pose representations(3D and euler angles):
 
```bash
 python main_h36_3d.py --input_n 10 --output_n 25 --skip_rate 1 --joints_to_consider 22 
 ```
```bash
 python main_h36_ang.py --input_n 10 --output_n 25 --skip_rate 1 --joints_to_consider 16 
  ```
 
 ### Test
 To test on the pretrained model, we have used the following commands:
 ```bash
 python main_h36_3d.py --input_n 10 --output_n 25 --skip_rate 1 --joints_to_consider 22 --mode test --model_path ./checkpoints/CKPT_3D_H36M
  ```
  ```bash
  python main_h36_ang.py --input_n 10 --output_n 25 --skip_rate 1 --joints_to_consider 16 --mode test --model_path ./checkpoints/CKPT_ANG_H36M
  ```

### Visualization
 For visualizing from a pretrained model, we have used the following commands:
 ```bash
  python main_h36_3d.py --input_n 10 --output_n 25 --skip_rate 1 --joints_to_consider 22 --mode viz --model_path ./checkpoints/CKPT_3D_H36M --n_viz 5
 ```
 ```bash
  python main_h36_ang.py --input_n 10 --output_n 25 --skip_rate 1 --joints_to_consider 16 --mode viz --model_path ./checkpoints/CKPT_ANG_H36M --n_viz 5
 ```


### Citing
 If you use our code,please cite our work
 
 ```
@misc{
}
 ```
 
 ### Acknowledgments
 

