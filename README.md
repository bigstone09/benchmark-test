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

* Andy's work computer trial #1 (similar to robot's computer for competition)

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

	Simple runtime statistics (wall-clock elapsed time):	
	Loading input to GPU (average runtime):		0.0057008361816406 seconds.	
	Training forward pass (average runtime):	0.20827218055725 seconds.	
	Training backward pass (average runtime):	0.25785929679871 seconds.	
	Total runtime for 25 training iterations:	69.340086936951 seconds.	
	Average runtime per training iteration:		2.7736037540436 seconds.	
	Testing forward pass (average runtime):		0.019329044818878 seconds.	
	```

* Andy's work computer trial #2 (similar to robot's computer for competition)

	```shell
	Training iteration 1	
		Sampling mini-batch (8 x 3 images):	1.0885901451111 seconds.	
		Loading input mini-batch to GPU:	0.008091926574707 seconds.	
		Forward pass:				1.2628321647644 seconds.	
		Backpropagation:			1.5927588939667 seconds.	
	Training iteration 2	
		Sampling mini-batch (8 x 3 images):	1.3089759349823 seconds.	
		Loading input mini-batch to GPU:	0.0072019100189209 seconds.	
		Forward pass:				0.19748497009277 seconds.	
		Backpropagation:			0.24005794525146 seconds.	
	Training iteration 3	
		Sampling mini-batch (8 x 3 images):	1.0738339424133 seconds.	
		Loading input mini-batch to GPU:	0.0067920684814453 seconds.	
		Forward pass:				0.19745707511902 seconds.	
		Backpropagation:			0.24005508422852 seconds.	
	Training iteration 4	
		Sampling mini-batch (8 x 3 images):	0.91724109649658 seconds.	
		Loading input mini-batch to GPU:	0.0054490566253662 seconds.	
		Forward pass:				0.19797992706299 seconds.	
		Backpropagation:			0.23982000350952 seconds.	
	Training iteration 5	
		Sampling mini-batch (8 x 3 images):	1.0118088722229 seconds.	
		Loading input mini-batch to GPU:	0.0067391395568848 seconds.	
		Forward pass:				0.19767808914185 seconds.	
		Backpropagation:			0.23929810523987 seconds.	
	Training iteration 6	
		Sampling mini-batch (8 x 3 images):	1.2485098838806 seconds.	
		Loading input mini-batch to GPU:	0.0069780349731445 seconds.	
		Forward pass:				0.21638202667236 seconds.	
		Backpropagation:			0.25906896591187 seconds.	
	Training iteration 7	
		Sampling mini-batch (8 x 3 images):	1.4963691234589 seconds.	
		Loading input mini-batch to GPU:	0.0072200298309326 seconds.	
		Forward pass:				0.21259713172913 seconds.	
		Backpropagation:			0.25630712509155 seconds.	
	Training iteration 8	
		Sampling mini-batch (8 x 3 images):	1.5836210250854 seconds.	
		Loading input mini-batch to GPU:	0.0086398124694824 seconds.	
		Forward pass:				0.19771695137024 seconds.	
		Backpropagation:			0.24735116958618 seconds.	
	Training iteration 9	
		Sampling mini-batch (8 x 3 images):	1.3060088157654 seconds.	
		Loading input mini-batch to GPU:	0.0068881511688232 seconds.	
		Forward pass:				0.20563101768494 seconds.	
		Backpropagation:			0.24005579948425 seconds.	
	Training iteration 10	
		Sampling mini-batch (8 x 3 images):	1.5016791820526 seconds.	
		Loading input mini-batch to GPU:	0.0087959766387939 seconds.	
		Forward pass:				0.20795392990112 seconds.	
		Backpropagation:			0.23990321159363 seconds.	
	Training iteration 11	
		Sampling mini-batch (8 x 3 images):	0.95963597297668 seconds.	
		Loading input mini-batch to GPU:	0.0052051544189453 seconds.	
		Forward pass:				0.19778990745544 seconds.	
		Backpropagation:			0.2397289276123 seconds.	
	Training iteration 12	
		Sampling mini-batch (8 x 3 images):	1.4488909244537 seconds.	
		Loading input mini-batch to GPU:	0.0084428787231445 seconds.	
		Forward pass:				0.19838190078735 seconds.	
		Backpropagation:			0.23987483978271 seconds.	
	Training iteration 13	
		Sampling mini-batch (8 x 3 images):	1.2787959575653 seconds.	
		Loading input mini-batch to GPU:	0.0070669651031494 seconds.	
		Forward pass:				0.19770383834839 seconds.	
		Backpropagation:			0.23999500274658 seconds.	
	Training iteration 14	
		Sampling mini-batch (8 x 3 images):	0.88185691833496 seconds.	
		Loading input mini-batch to GPU:	0.0051460266113281 seconds.	
		Forward pass:				0.19840121269226 seconds.	
		Backpropagation:			0.23940706253052 seconds.	
	Training iteration 15	
		Sampling mini-batch (8 x 3 images):	1.0237729549408 seconds.	
		Loading input mini-batch to GPU:	0.0052249431610107 seconds.	
		Forward pass:				0.19794893264771 seconds.	
		Backpropagation:			0.23999714851379 seconds.	
	Training iteration 16	
		Sampling mini-batch (8 x 3 images):	0.9360179901123 seconds.	
		Loading input mini-batch to GPU:	0.0081250667572021 seconds.	
		Forward pass:				0.19771099090576 seconds.	
		Backpropagation:			0.2394700050354 seconds.	
	Training iteration 17	
		Sampling mini-batch (8 x 3 images):	1.0573718547821 seconds.	
		Loading input mini-batch to GPU:	0.0051419734954834 seconds.	
		Forward pass:				0.19793486595154 seconds.	
		Backpropagation:			0.23975014686584 seconds.	
	Training iteration 18	
		Sampling mini-batch (8 x 3 images):	0.9336998462677 seconds.	
		Loading input mini-batch to GPU:	0.0056068897247314 seconds.	
		Forward pass:				0.19775390625 seconds.	
		Backpropagation:			0.2399959564209 seconds.	
	Training iteration 19	
		Sampling mini-batch (8 x 3 images):	1.3629169464111 seconds.	
		Loading input mini-batch to GPU:	0.0069229602813721 seconds.	
		Forward pass:				0.19793295860291 seconds.	
		Backpropagation:			0.2399730682373 seconds.	
	Training iteration 20	
		Sampling mini-batch (8 x 3 images):	0.99309611320496 seconds.	
		Loading input mini-batch to GPU:	0.0055160522460938 seconds.	
		Forward pass:				0.19780993461609 seconds.	
		Backpropagation:			0.23993992805481 seconds.	
	Training iteration 21	
		Sampling mini-batch (8 x 3 images):	0.95115900039673 seconds.	
		Loading input mini-batch to GPU:	0.0070431232452393 seconds.	
		Forward pass:				0.19788503646851 seconds.	
		Backpropagation:			0.24021291732788 seconds.	
	Training iteration 22	
		Sampling mini-batch (8 x 3 images):	0.88082098960876 seconds.	
		Loading input mini-batch to GPU:	0.0052390098571777 seconds.	
		Forward pass:				0.19821405410767 seconds.	
		Backpropagation:			0.2404100894928 seconds.	
	Training iteration 23	
		Sampling mini-batch (8 x 3 images):	0.83696794509888 seconds.	
		Loading input mini-batch to GPU:	0.0053892135620117 seconds.	
		Forward pass:				0.1985330581665 seconds.	
		Backpropagation:			0.24021220207214 seconds.	
	Training iteration 24	
		Sampling mini-batch (8 x 3 images):	1.0375819206238 seconds.	
		Loading input mini-batch to GPU:	0.0069489479064941 seconds.	
		Forward pass:				0.19799017906189 seconds.	
		Backpropagation:			0.24109196662903 seconds.	
	Training iteration 25	
		Sampling mini-batch (8 x 3 images):	0.86194705963135 seconds.	
		Loading input mini-batch to GPU:	0.0053408145904541 seconds.	
		Forward pass:				0.19806408882141 seconds.	
		Backpropagation:			0.23984408378601 seconds.	

	Simple runtime statistics (wall-clock elapsed time):	
	Loading input to GPU (average runtime):		0.0065970230102539 seconds.	
	Training forward pass (average runtime):	0.24254447937012 seconds.	
	Training backward pass (average runtime):	0.29577780723572 seconds.	
	Total runtime for 25 training iterations:	77.526621818542 seconds.	
	Average runtime per training iteration:		3.1010652732849 seconds.	
	Testing forward pass (average runtime):		0.019975671768188 seconds.
	```