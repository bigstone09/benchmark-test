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

* Andy's work computer trial #2

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

* Andy's work computer trial #3

	```shell
	Training iteration 1	
		Sampling mini-batch (8 x 3 images):	1.2719349861145 seconds.	
		Loading input mini-batch to GPU:	0.0086221694946289 seconds.	
		Forward pass:				0.41344308853149 seconds.	
		Backpropagation:			0.67188906669617 seconds.	
	Training iteration 2	
		Sampling mini-batch (8 x 3 images):	1.3878390789032 seconds.	
		Loading input mini-batch to GPU:	0.0071918964385986 seconds.	
		Forward pass:				0.21254587173462 seconds.	
		Backpropagation:			0.24282693862915 seconds.	
	Training iteration 3	
		Sampling mini-batch (8 x 3 images):	1.2364678382874 seconds.	
		Loading input mini-batch to GPU:	0.0069289207458496 seconds.	
		Forward pass:				0.19832110404968 seconds.	
		Backpropagation:			0.24003791809082 seconds.	
	Training iteration 4	
		Sampling mini-batch (8 x 3 images):	1.1536428928375 seconds.	
		Loading input mini-batch to GPU:	0.0069618225097656 seconds.	
		Forward pass:				0.19831991195679 seconds.	
		Backpropagation:			0.24044704437256 seconds.	
	Training iteration 5	
		Sampling mini-batch (8 x 3 images):	1.1817200183868 seconds.	
		Loading input mini-batch to GPU:	0.0069079399108887 seconds.	
		Forward pass:				0.19780492782593 seconds.	
		Backpropagation:			0.23908281326294 seconds.	
	Training iteration 6	
		Sampling mini-batch (8 x 3 images):	0.92917895317078 seconds.	
		Loading input mini-batch to GPU:	0.0053019523620605 seconds.	
		Forward pass:				0.19800400733948 seconds.	
		Backpropagation:			0.23962688446045 seconds.	
	Training iteration 7	
		Sampling mini-batch (8 x 3 images):	1.3540949821472 seconds.	
		Loading input mini-batch to GPU:	0.00705885887146 seconds.	
		Forward pass:				0.19821190834045 seconds.	
		Backpropagation:			0.24070000648499 seconds.	
	Training iteration 8	
		Sampling mini-batch (8 x 3 images):	1.2273290157318 seconds.	
		Loading input mini-batch to GPU:	0.0069258213043213 seconds.	
		Forward pass:				0.1984121799469 seconds.	
		Backpropagation:			0.23917984962463 seconds.	
	Training iteration 9	
		Sampling mini-batch (8 x 3 images):	0.98622488975525 seconds.	
		Loading input mini-batch to GPU:	0.0053131580352783 seconds.	
		Forward pass:				0.19800400733948 seconds.	
		Backpropagation:			0.23981904983521 seconds.	
	Training iteration 10	
		Sampling mini-batch (8 x 3 images):	0.98745608329773 seconds.	
		Loading input mini-batch to GPU:	0.0053269863128662 seconds.	
		Forward pass:				0.19807195663452 seconds.	
		Backpropagation:			0.23994088172913 seconds.	
	Training iteration 11	
		Sampling mini-batch (8 x 3 images):	1.0764479637146 seconds.	
		Loading input mini-batch to GPU:	0.0054280757904053 seconds.	
		Forward pass:				0.19849586486816 seconds.	
		Backpropagation:			0.23984718322754 seconds.	
	Training iteration 12	
		Sampling mini-batch (8 x 3 images):	0.94687485694885 seconds.	
		Loading input mini-batch to GPU:	0.0054819583892822 seconds.	
		Forward pass:				0.19801878929138 seconds.	
		Backpropagation:			0.23992514610291 seconds.	
	Training iteration 13	
		Sampling mini-batch (8 x 3 images):	0.99118208885193 seconds.	
		Loading input mini-batch to GPU:	0.0050880908966064 seconds.	
		Forward pass:				0.19885206222534 seconds.	
		Backpropagation:			0.24000382423401 seconds.	
	Training iteration 14	
		Sampling mini-batch (8 x 3 images):	1.0234549045563 seconds.	
		Loading input mini-batch to GPU:	0.0054140090942383 seconds.	
		Forward pass:				0.19816088676453 seconds.	
		Backpropagation:			0.24122381210327 seconds.	
	Training iteration 15	
		Sampling mini-batch (8 x 3 images):	1.1294300556183 seconds.	
		Loading input mini-batch to GPU:	0.0068509578704834 seconds.	
		Forward pass:				0.19800615310669 seconds.	
		Backpropagation:			0.23960185050964 seconds.	
	Training iteration 16	
		Sampling mini-batch (8 x 3 images):	1.2257430553436 seconds.	
		Loading input mini-batch to GPU:	0.0080149173736572 seconds.	
		Forward pass:				0.19819307327271 seconds.	
		Backpropagation:			0.24042081832886 seconds.	
	Training iteration 17	
		Sampling mini-batch (8 x 3 images):	0.88962411880493 seconds.	
		Loading input mini-batch to GPU:	0.0054090023040771 seconds.	
		Forward pass:				0.19799709320068 seconds.	
		Backpropagation:			0.23986101150513 seconds.	
	Training iteration 18	
		Sampling mini-batch (8 x 3 images):	0.99461388587952 seconds.	
		Loading input mini-batch to GPU:	0.0063760280609131 seconds.	
		Forward pass:				0.19821286201477 seconds.	
		Backpropagation:			0.24240493774414 seconds.	
	Training iteration 19	
		Sampling mini-batch (8 x 3 images):	1.0023329257965 seconds.	
		Loading input mini-batch to GPU:	0.0050079822540283 seconds.	
		Forward pass:				0.19889903068542 seconds.	
		Backpropagation:			0.24002909660339 seconds.	
	Training iteration 20	
		Sampling mini-batch (8 x 3 images):	0.95516800880432 seconds.	
		Loading input mini-batch to GPU:	0.0081961154937744 seconds.	
		Forward pass:				0.19863486289978 seconds.	
		Backpropagation:			0.24039793014526 seconds.	
	Training iteration 21	
		Sampling mini-batch (8 x 3 images):	0.99515795707703 seconds.	
		Loading input mini-batch to GPU:	0.005169153213501 seconds.	
		Forward pass:				0.19835495948792 seconds.	
		Backpropagation:			0.23961091041565 seconds.	
	Training iteration 22	
		Sampling mini-batch (8 x 3 images):	1.1763281822205 seconds.	
		Loading input mini-batch to GPU:	0.0070259571075439 seconds.	
		Forward pass:				0.19859910011292 seconds.	
		Backpropagation:			0.24124002456665 seconds.	
	Training iteration 23	
		Sampling mini-batch (8 x 3 images):	1.2094218730927 seconds.	
		Loading input mini-batch to GPU:	0.0069379806518555 seconds.	
		Forward pass:				0.19947099685669 seconds.	
		Backpropagation:			0.2402880191803 seconds.	
	Training iteration 24	
		Sampling mini-batch (8 x 3 images):	0.93158602714539 seconds.	
		Loading input mini-batch to GPU:	0.0050740242004395 seconds.	
		Forward pass:				0.19839882850647 seconds.	
		Backpropagation:			0.2398841381073 seconds.	
	Training iteration 25	
		Sampling mini-batch (8 x 3 images):	0.93515610694885 seconds.	
		Loading input mini-batch to GPU:	0.0052120685577393 seconds.	
		Forward pass:				0.19836020469666 seconds.	
		Backpropagation:			0.2398669719696 seconds.	

	Simple runtime statistics (wall-clock elapsed time):	
	Loading input to GPU (average runtime):		0.0062805938720703 seconds.	
	Training forward pass (average runtime):	0.20750591278076 seconds.	
	Training backward pass (average runtime):	0.25752116203308 seconds.	
	Total runtime for 25 training iterations:	74.470209121704 seconds.	
	Average runtime per training iteration:		2.9788086795807 seconds.	
	Testing forward pass (average runtime):		0.019420485496521 seconds.
	```