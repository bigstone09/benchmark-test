# Benchmark Test

## Requirements
- Install [Torch](http://torch.ch/docs/getting-started.html) on a machine with CUDA GPU
- Install [cuDNN v5](https://developer.nvidia.com/cudnn)

## Instructions

```bash
git clone https://github.com/andyzeng/benchmark-test.git benchmark-test # (~40mb)
cd benchmark-test
unzip files.zip
wget https://d2j0dndfm35trm.cloudfront.net/resnet-101.t7
nvidia-smi # report GPU info
th main.lua # report last 7 lines of console output
```

## Our Machines

* Andy's work computer (similar to robot's computer for competition)

	```bash
	+-----------------------------------------------------------------------------+
	| NVIDIA-SMI 367.48                 Driver Version: 367.48                    |
	|-------------------------------+----------------------+----------------------+
	| GPU  Name        Persistence-M| Bus-Id        Disp.A | Volatile Uncorr. ECC |
	| Fan  Temp  Perf  Pwr:Usage/Cap|         Memory-Usage | GPU-Util  Compute M. |
	|===============================+======================+======================|
	|   0  GeForce GTX TIT...  Off  | 0000:03:00.0      On |                  N/A |
	| 22%   48C    P8    16W / 250W |    438MiB / 12198MiB |      1%      Default |
	+-------------------------------+----------------------+----------------------+

	Simple runtime statistics (wall-clock elapsed time):	
	Loading input to GPU (average runtime):		0.0057008361816406 seconds.	
	Training forward pass (average runtime):	0.20827218055725 seconds.	
	Training backward pass (average runtime):	0.25785929679871 seconds.	
	Total runtime for 25 training iterations:	69.340086936951 seconds.	
	Average runtime per training iteration:		2.7736037540436 seconds.	
	Testing forward pass (average runtime):		0.019329044818878 seconds.	
	```

