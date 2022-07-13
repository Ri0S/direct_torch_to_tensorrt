# torch to onnx to tensorrt

## environment
RTX3090  
Ubuntu 20.04.4  
torch==1.12.0+cu113  
tensorrt==8.4.1.5  

## onnx_tensorrt_bert_test.py result  
```
onnx to tensorrt bert(fp32) =================================
batch size=16, num iterations=100
  Median text batches/second: 254.9, mean: 254.8
  Median latency: 0.062781, mean: 0.062785, 99th_p: 0.063209, std_dev: 0.000249
```

## onnx_tensorrt_bert_fp16_test.py result
```
onnx to tensorrt bert =================================
batch size=16, num iterations=100
  Median text batches/second: 693.9, mean: 691.4
  Median latency: 0.023057, mean: 0.023145, 99th_p: 0.024300, std_dev: 0.000263
```

# direct_torch_to_tensorrt

## environment
RTX3090  
Ubuntu 20.04.4  
torch==1.13.0a0_340c412  
torch_tensorrt==1.1.0a0  
tensorrt==8.2.5.1  

## bert_test.py result
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

## vit_test.py result
```
Normal ViT =================================
batch size=64, num iterations=100
  Median text batches/second: 637.9, mean: 637.6
  Median latency: 0.100335, mean: 0.100373, 99th_p: 0.100814, std_dev: 0.000191

Warm up ...
Start timing ...

Half Normal ViT =================================
batch size=64, num iterations=100
  Median text batches/second: 1196.7, mean: 1194.7
  Median latency: 0.053479, mean: 0.053570, 99th_p: 0.053961, std_dev: 0.000173

Warm up ...
Start timing ...

Script ViT =================================
batch size=64, num iterations=100
  Median text batches/second: 635.3, mean: 635.4
  Median latency: 0.100735, mean: 0.100721, 99th_p: 0.101074, std_dev: 0.000133

Warm up ...
Start timing ...

Half Script ViT =================================
batch size=64, num iterations=100
  Median text batches/second: 1191.0, mean: 1192.0
  Median latency: 0.053735, mean: 0.053690, 99th_p: 0.053962, std_dev: 0.000180

Warm up ...
Start timing ...

Traced ViT =================================
batch size=64, num iterations=100
  Median text batches/second: 634.2, mean: 634.3
  Median latency: 0.100921, mean: 0.100897, 99th_p: 0.101372, std_dev: 0.000219

Warm up ...
Start timing ...

Half Traced ViT =================================
batch size=64, num iterations=100
  Median text batches/second: 1114.4, mean: 1115.9
  Median latency: 0.057428, mean: 0.057353, 99th_p: 0.057843, std_dev: 0.000226

Warm up ...
Start timing ...

trt ViT =================================
batch size=64, num iterations=100
  Median text batches/second: 673.6, mean: 673.4
  Median latency: 0.095010, mean: 0.095037, 99th_p: 0.096635, std_dev: 0.000479

Warm up ...
Start timing ...

Half trt ViT =================================
batch size=64, num iterations=100
  Median text batches/second: 1382.6, mean: 1382.6
  Median latency: 0.046289, mean: 0.046290, 99th_p: 0.046431, std_dev: 0.000084
```
