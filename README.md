# README #

### What is this repository for? ###

* oxnnet_core is a light weight python program designed to be extended to create more complex neural networks for patch based image analysis
* Version 0.01

### How do I get set up? ###

**Create a set of test cases** 

`python3 -m tests.utils ~/Desktop/TestVolumes`

**Write out the TensorFlowRecords**

`python3 main.py --model oxnnet.model.simplenet write --save_dir ~/Desktop/TestRect-tfr --data_dir ~/Desktop/TestVolumes/`

**Train the model**

`python3 main.py --model oxnnet.model.simplenet train --tfr_dir ~/Desktop/TestRect-tfr --save_dir ~/Desktop/TestRect-out --num_epochs 10 --batch_size 100`

**Test the model**

`python3 main.py --model oxnnet.model.simplenet test --save_dir ~/Desktop/TestRect-out/test --test_data_file ~/Desktop/TestRect-tfr/meta_data.txt --model_file ~/Desktop/TestRect-out/epoch_model.ckpt-<iteration_no> --batch_size 100`

**Dependencies**

`tflearn (v0.3), tensorflow (v1.5), pandas, nibabel`

Python 3.5 recommended.

** How to run tests **

`python3 -m unittest`
