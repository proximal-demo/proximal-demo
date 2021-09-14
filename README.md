<h1><center>Sparse Audio Adversarial Examples via Proximal Gradient Descent</center></h1>

<center><b>Anonymous Author(s)</b></center>

## Abstract
Audio adversarial examples are constructed maliciously to deceive automatic speech recognition (ASR) systems. Until now, most researches on audio adversarial attack focus on dense examples leaving the redundancy in the audio adversarial perturbations unexplored. In this work, we propose an effective sparse audio adversarial attack algorithm that leverages proximal gradient descent to achieve targeted sparsity. Specifically, we perform proximal gradient descent with a thresholding algorithm to constrain the non-convex $ l_{0} $-norm of the perturbations after each audio adversarial iterations. Since our method is generic, it can be combined with most existing adversarial attacks to improve their performance. Experiments on the LibriSpeech dataset demonstrate the effectiveness of our algorithm: it significantly improves the imperceptibility of several state-of-the-art attack baselines via sparsification and reveal that there are 30\%$\sim$40\% redundant perturbations. Moreover, our work is the first attempt to implement a successful optimization-based sparse attack against the automatic speech recognition systems.

## Audio Adversarial Examples

Here We display three sets of audio examples of the imperceptibility test in the paper. 
In each set, there is clean examples, the adversarial examples generated by baselines in the paper and the adversarial examples generated by the corresponding baselines combined with our sparse strategy. Observe them carefully and find the differences.


*Note:*

*(1) All samples are in LibriSpeech Dataset[1].*

*(2) --> means being transcribed to*

*(3) We contains other samples in this github repo.*

**First Set: it has no beauty whatsoever no specialty of picturesqueness and all its lines are cramped and poor  -->  but the real significance and comfort of the words for our sins is lost upon them**
<div>
	<div style='text-align:center; display: inline-block;'>
    <audio controls>
        <source src="cw/0_gt.wav" type="audio/mpeg">
        Your browser does not support this audio format.
    </audio>
	<h4>clean</h4>
	</div>
	
	<div style='text-align:center; display: inline-block;'>
        <div style='height:50px; width:100px;'></div>
	</div>
	
	<div style='text-align:center; display: inline-block;'>
    <audio controls>
        <source src="cw/0.wav" type="audio/mpeg">
        Your browser does not support this audio format.
    </audio>
	<h4>C&W's</h4>
	</div>

	<div style='text-align:center; display: inline-block;'>
    <audio controls>
        <source src="cw_proximal/0.wav" type="audio/mpeg">
        Your browser does not support this audio format.
    </audio>
	<h4>C&W's + ours</h4>
	</div>
	
	<div style='text-align:center; display: inline-block;'>
    <audio controls>
        <source src="IPC/0.wav" type="audio/mpeg">
        Your browser does not support this audio format.
    </audio>
	<h4>IPC</h4>
	</div>
	
	<div style='text-align:center; display: inline-block;'>
    <audio controls>
        <source src="IPC_proximal/0.wav" type="audio/mpeg">
        Your browser does not support this audio format.
    </audio>
	<h4>IPC + ours</h4>
	</div>
	
	<div style='text-align:center; display: inline-block;'>
    <audio controls>
        <source src="imperceptible/0.wav" type="audio/mpeg">
        Your browser does not support this audio format.
    </audio>
	<h4>Imperceptible</h4>
	</div>
	
	<div style='text-align:center; display: inline-block;'>
    <audio controls>
        <source src="imperceptible_priximal/0.wav" type="audio/mpeg">
        Your browser does not support this audio format.
    </audio>
	<h4>Imperceptible + ours</h4>
	</div>
</div>

**Second Set: when we were out in the darkness of the quadrangle we again looked up at the windows  
-->  the most famous of them all was the overthrow of the island of atlantis**
<div>
	<div style='text-align:center; display: inline-block;'>
    <audio controls>
        <source src="cw/14_gt.wav" type="audio/mpeg">
        Your browser does not support this audio format.
    </audio>
	<h4>clean</h4>
	</div>
	
	<div style='text-align:center; display: inline-block;'>
        <div style='height:50px; width:100px;'></div>
	</div>
	
	<div style='text-align:center; display: inline-block;'>
    <audio controls>
        <source src="cw/14.wav" type="audio/mpeg">
        Your browser does not support this audio format.
    </audio>
	<h4>C&W's</h4>
	</div>

	<div style='text-align:center; display: inline-block;'>
    <audio controls>
        <source src="cw_proximal/14.wav" type="audio/mpeg">
        Your browser does not support this audio format.
    </audio>
	<h4>C&W's + ours</h4>
	</div>
	
	<div style='text-align:center; display: inline-block;'>
    <audio controls>
        <source src="IPC/14.wav" type="audio/mpeg">
        Your browser does not support this audio format.
    </audio>
	<h4>IPC</h4>
	</div>
	
	<div style='text-align:center; display: inline-block;'>
    <audio controls>
        <source src="IPC_proximal/14.wav" type="audio/mpeg">
        Your browser does not support this audio format.
    </audio>
	<h4>IPC + ours</h4>
	</div>
	
	<div style='text-align:center; display: inline-block;'>
    <audio controls>
        <source src="imperceptible/14.wav" type="audio/mpeg">
        Your browser does not support this audio format.
    </audio>
	<h4>Imperceptible</h4>
	</div>
	
	<div style='text-align:center; display: inline-block;'>
    <audio controls>
        <source src="imperceptible_priximal/14.wav" type="audio/mpeg">
        Your browser does not support this audio format.
    </audio>
	<h4>Imperceptible + ours</h4>
	</div>
</div>



## References
[1] Vassil Panayotov, Guoguo Chen, Daniel Povey, and San-jeev Khudanpur,  “Librispeech:  an asr corpus based onpublic domain audio books,” in2015 IEEE internationalconference on acoustics, speech and signal processing(ICASSP). IEEE, 2015, pp. 5206–5210.

[2] Carlini N, Wagner D. Audio adversarial examples: Targeted attacks on speech-to-text[C]//2018 IEEE Security and Privacy Workshops (SPW). IEEE, 2018: 1-7.

[3] Zhang H, Zhou P, Yan Q, et al. Generating robust audio adversarial examples with temporal dependency[C]//Proc. Int. Joint Conf. Artif. Intell. 2020: 1-5.

[4] Yao Qin, Nicholas Carlini, Garrison Cottrell, Ian Good-fellow,   and  Colin  Raffel,“Imperceptible,   robust,and targeted adversarial examples for automatic speechrecognition,”   inInternational  conference  on  machinelearning. PMLR, 2019, pp. 5231–5240.