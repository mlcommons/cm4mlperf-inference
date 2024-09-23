This experiment is generated using the [MLCommons Collective Mind automation framework (CM)](https://github.com/mlcommons/cm4mlops).

*Check [CM MLPerf docs](https://docs.mlcommons.org/inference) for more details.*

## Host platform

* OS version: Linux-6.2.0-39-generic-x86_64-with-glibc2.29
* CPU version: x86_64
* Python version: 3.8.10 (default, Sep 11 2024, 16:02:53) 
[GCC 9.4.0]
* MLCommons CM version: 2.3.6

## CM Run Command

See [CM installation guide](https://docs.mlcommons.org/inference/install/).

```bash
pip install -U cmind

cm rm cache -f

cm pull repo mlcommons@cm4mlops --checkout=0d133c9551d9b2cb5b0d10aec9114dcf92c02dd9

cm run script \
	--tags=run-mlperf,inference,_r4.1-dev,_short,_scc24-base \
	--model=sdxl \
	--implementation=nvidia \
	--framework=tensorrt \
	--category=edge \
	--scenario=Offline \
	--execution_mode=test \
	--device=cuda \
	--quiet \
	--precision=float16
```
*Note that if you want to use the [latest automation recipes](https://docs.mlcommons.org/inference) for MLPerf (CM scripts),
 you should simply reload mlcommons@cm4mlops without checkout and clean CM cache as follows:*

```bash
cm rm repo mlcommons@cm4mlops
cm pull repo mlcommons@cm4mlops
cm rm cache -f

```

## Results

Platform: 48ed6105bd85-nvidia-gpu-TensorRT-scc24-base

Model Precision: int8

### Accuracy Results 
`CLIP_SCORE`: `15.58605`, Required accuracy for closed division `>= 31.68632` and `<= 31.81332`
`FID_SCORE`: `236.80871`, Required accuracy for closed division `>= 23.01086` and `<= 23.95008`

### Performance Results 
`Samples per second`: `1.13598`
