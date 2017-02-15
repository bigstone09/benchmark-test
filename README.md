# Benchmark Test

## Requirements
- Install [Torch](http://torch.ch/docs/getting-started.html) on a machine with CUDA GPU
- Install [cuDNN v5](https://developer.nvidia.com/cudnn)

## Instructions

```shell
git clone https://github.com/andyzeng/benchmark-test.git benchmark-test # (~40mb)
cd benchmark-test
unzip files.zip
wget https://d2j0dndfm35trm.cloudfront.net/resnet-101.t7
nvidia-smi # report GPU info
th main.lua # report last 7 lines of console output
```

## Our Machines

* Andy's work computer trial #4 (similar to robot's computer for competition)

	```shell
	+-----------------------------------------------------------------------------+
	| NVIDIA-SMI 367.48                 Driver Version: 367.48                    |
	|-------------------------------+----------------------+----------------------+
	| GPU  Name        Persistence-M| Bus-Id        Disp.A | Volatile Uncorr. ECC |
	| Fan  Temp  Perf  Pwr:Usage/Cap|         Memory-Usage | GPU-Util  Compute M. |
	|===============================+======================+======================|
	|   0  GeForce GTX TIT...  Off  | 0000:03:00.0      On |                  N/A |
	| 22%   48C    P8    16W / 250W |    438MiB / 12198MiB |      1%      Default |
	+-------------------------------+----------------------+----------------------+

	Training iteration 1	
		Sampling mini-batch (8 x 3 images):	0.099837064743042 seconds.	
		Loading input mini-batch to GPU:	0.0119309425354 seconds.	
		Forward pass:						0.83366012573242 seconds.	
		Backpropagation:					0.8948118686676 seconds.	
	Training iteration 2	
		Sampling mini-batch (8 x 3 images):	0.065521001815796 seconds.	
		Loading input mini-batch to GPU:	0.012498140335083 seconds.	
		Forward pass:						0.20031785964966 seconds.	
		Backpropagation:					0.24098420143127 seconds.	
	Training iteration 3	
		Sampling mini-batch (8 x 3 images):	0.069196939468384 seconds.	
		Loading input mini-batch to GPU:	0.19375610351562 seconds.	
		Forward pass:						0.20017719268799 seconds.	
		Backpropagation:					0.24017810821533 seconds.	
	Training iteration 4	
		Sampling mini-batch (8 x 3 images):	0.066982984542847 seconds.	
		Loading input mini-batch to GPU:	0.19562411308289 seconds.	
		Forward pass:						0.1999819278717 seconds.	
		Backpropagation:					0.24144196510315 seconds.	
	Training iteration 5	
		Sampling mini-batch (8 x 3 images):	0.069797039031982 seconds.	
		Loading input mini-batch to GPU:	0.19170784950256 seconds.	
		Forward pass:						0.19968295097351 seconds.	
		Backpropagation:					0.24080109596252 seconds.	
	Training iteration 6	
		Sampling mini-batch (8 x 3 images):	0.060125112533569 seconds.	
		Loading input mini-batch to GPU:	0.19904899597168 seconds.	
		Forward pass:						0.19950604438782 seconds.	
		Backpropagation:					0.24078106880188 seconds.	
	Training iteration 7	
		Sampling mini-batch (8 x 3 images):	0.067155838012695 seconds.	
		Loading input mini-batch to GPU:	0.19238781929016 seconds.	
		Forward pass:						0.19941997528076 seconds.	
		Backpropagation:					0.23980689048767 seconds.	
	Training iteration 8	
		Sampling mini-batch (8 x 3 images):	0.065262079238892 seconds.	
		Loading input mini-batch to GPU:	0.19376993179321 seconds.	
		Forward pass:						0.19994211196899 seconds.	
		Backpropagation:					0.24090909957886 seconds.	
	Training iteration 9	
		Sampling mini-batch (8 x 3 images):	0.064054012298584 seconds.	
		Loading input mini-batch to GPU:	0.19869995117188 seconds.	
		Forward pass:						0.20143818855286 seconds.	
		Backpropagation:					0.24237203598022 seconds.	
	Training iteration 10	
		Sampling mini-batch (8 x 3 images):	0.068015098571777 seconds.	
		Loading input mini-batch to GPU:	0.19572305679321 seconds.	
		Forward pass:						0.20136380195618 seconds.	
		Backpropagation:					0.24220895767212 seconds.	
	Training iteration 11	
		Sampling mini-batch (8 x 3 images):	0.071031093597412 seconds.	
		Loading input mini-batch to GPU:	0.19466114044189 seconds.	
		Forward pass:						0.20219302177429 seconds.	
		Backpropagation:					0.24465298652649 seconds.	
	Training iteration 12	
		Sampling mini-batch (8 x 3 images):	0.062084913253784 seconds.	
		Loading input mini-batch to GPU:	0.20227718353271 seconds.	
		Forward pass:						0.20234298706055 seconds.	
		Backpropagation:					0.24388194084167 seconds.	
	Training iteration 13	
		Sampling mini-batch (8 x 3 images):	0.078464984893799 seconds.	
		Loading input mini-batch to GPU:	0.18648195266724 seconds.	
		Forward pass:						0.20270609855652 seconds.	
		Backpropagation:					0.24345207214355 seconds.	
	Training iteration 14	
		Sampling mini-batch (8 x 3 images):	0.075786113739014 seconds.	
		Loading input mini-batch to GPU:	0.18905806541443 seconds.	
		Forward pass:						0.20253109931946 seconds.	
		Backpropagation:					0.24333691596985 seconds.	
	Training iteration 15	
		Sampling mini-batch (8 x 3 images):	0.078267097473145 seconds.	
		Loading input mini-batch to GPU:	0.18746495246887 seconds.	
		Forward pass:						0.20221900939941 seconds.	
		Backpropagation:					0.24356293678284 seconds.	
	Training iteration 16	
		Sampling mini-batch (8 x 3 images):	0.077510118484497 seconds.	
		Loading input mini-batch to GPU:	0.18847298622131 seconds.	
		Forward pass:						0.20224905014038 seconds.	
		Backpropagation:					0.24331712722778 seconds.	
	Training iteration 17	
		Sampling mini-batch (8 x 3 images):	0.079019069671631 seconds.	
		Loading input mini-batch to GPU:	0.18532085418701 seconds.	
		Forward pass:						0.20204997062683 seconds.	
		Backpropagation:					0.24342608451843 seconds.	
	Training iteration 18	
		Sampling mini-batch (8 x 3 images):	0.063156127929688 seconds.	
		Loading input mini-batch to GPU:	0.20040106773376 seconds.	
		Forward pass:						0.20171403884888 seconds.	
		Backpropagation:					0.24290490150452 seconds.	
	Training iteration 19	
		Sampling mini-batch (8 x 3 images):	0.05597186088562 seconds.	
		Loading input mini-batch to GPU:	0.20666289329529 seconds.	
		Forward pass:						0.20226407051086 seconds.	
		Backpropagation:					0.24291300773621 seconds.	
	Training iteration 20	
		Sampling mini-batch (8 x 3 images):	0.060302972793579 seconds.	
		Loading input mini-batch to GPU:	0.20330691337585 seconds.	
		Forward pass:						0.20165085792542 seconds.	
		Backpropagation:					0.24320483207703 seconds.	
	Training iteration 21	
		Sampling mini-batch (8 x 3 images):	0.068582057952881 seconds.	
		Loading input mini-batch to GPU:	0.19452810287476 seconds.	
		Forward pass:						0.20212388038635 seconds.	
		Backpropagation:					0.24304890632629 seconds.	
	Training iteration 22	
		Sampling mini-batch (8 x 3 images):	0.066182136535645 seconds.	
		Loading input mini-batch to GPU:	0.19750905036926 seconds.	
		Forward pass:						0.20176601409912 seconds.	
		Backpropagation:					0.24348282814026 seconds.	
	Training iteration 23	
		Sampling mini-batch (8 x 3 images):	0.058594942092896 seconds.	
		Loading input mini-batch to GPU:	0.20702815055847 seconds.	
		Forward pass:						0.20201301574707 seconds.	
		Backpropagation:					0.24300098419189 seconds.	
	Training iteration 24	
		Sampling mini-batch (8 x 3 images):	0.06843113899231 seconds.	
		Loading input mini-batch to GPU:	0.19640588760376 seconds.	
		Forward pass:						0.20216798782349 seconds.	
		Backpropagation:					0.24410200119019 seconds.	
	Training iteration 25	
		Sampling mini-batch (8 x 3 images):	0.073641061782837 seconds.	
		Loading input mini-batch to GPU:	0.19171619415283 seconds.	
		Forward pass:						0.20234894752502 seconds.	
		Backpropagation:					0.24435710906982 seconds.	

	Simple runtime statistics (wall-clock elapsed time):	
	Loading input to GPU (average runtime):		0.18061017036438 seconds.	
	Training forward pass (average runtime):	0.22666820526123 seconds.	
	Training backward pass (average runtime):	0.26863368988037 seconds.	
	Total runtime for 25 training iterations:	21.190505981445 seconds.	
	Average runtime per training iteration:		0.84762207984924 seconds.	
	Testing forward pass (average runtime):		0.019637157917023 seconds.		
	```
