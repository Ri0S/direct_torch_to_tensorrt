# direct_torch_to_tensorrt

## environment
RTX3090  
Ubuntu 20.04.4  
torch==1.13.0a0_340c412  
torch_tensorrt==1.1.0a0  
tensorrt==8.2.5.1  

## Bert result
```
Normal Bert =================================
batch size=16, num iterations=100
  Median text batches/second: 202.1, mean: 201.9
  Median latency: 0.079167, mean: 0.079256, 99th_p: 0.079729, std_dev: 0.000260

Warm up ...
Start timing ...

Half Normal Bert =================================
batch size=16, num iterations=100
  Median text batches/second: 375.6, mean: 375.5
  Median latency: 0.042594, mean: 0.042615, 99th_p: 0.042792, std_dev: 0.000111

Warm up ...
Start timing ...

Script Bert =================================
batch size=16, num iterations=100
  Median text batches/second: 201.5, mean: 201.5
  Median latency: 0.079419, mean: 0.079417, 99th_p: 0.079475, std_dev: 0.000031

Warm up ...
Start timing ...

Half Script Bert =================================
batch size=16, num iterations=100
  Median text batches/second: 374.5, mean: 374.7
  Median latency: 0.042724, mean: 0.042705, 99th_p: 0.042966, std_dev: 0.000089

Warm up ...
Start timing ...

Traced Bert =================================
batch size=16, num iterations=100
  Median text batches/second: 241.1, mean: 241.2
  Median latency: 0.066375, mean: 0.066349, 99th_p: 0.066799, std_dev: 0.000223

Warm up ...
Start timing ...

Half Traced Bert =================================
batch size=16, num iterations=100
  Median text batches/second: 450.4, mean: 450.0
  Median latency: 0.035526, mean: 0.035553, 99th_p: 0.036090, std_dev: 0.000210

Warm up ...
Start timing ...

trt Bert =================================
batch size=16, num iterations=100
  Median text batches/second: 238.7, mean: 238.4
  Median latency: 0.067026, mean: 0.067125, 99th_p: 0.067480, std_dev: 0.000297

Warm up ...
Start timing ...

Half trt Bert =================================
batch size=16, num iterations=100
  Median text batches/second: 478.8, mean: 478.0
  Median latency: 0.033417, mean: 0.033482, 99th_p: 0.036420, std_dev: 0.000470
```
