This experiment is generated using the [MLCommons Collective Mind automation framework (CM)](https://github.com/mlcommons/cm4mlops).

*Check [CM MLPerf docs](https://docs.mlcommons.org/inference) for more details.*

## Host platform

* OS version: Linux-5.14.0-427.37.1.el9_4.x86_64-x86_64-with-glibc2.35
* CPU version: x86_64
* Python version: 3.10.12 (main, Sep 11 2024, 15:47:36) [GCC 11.4.0]
* MLCommons CM version: 3.0.1

## CM Run Command

See [CM installation guide](https://docs.mlcommons.org/inference/install/).

```bash
pip install -U cmind

cm rm cache -f

cm pull repo mlcommons@cm4mlops --checkout=769bf6afb15058ab9699c8b708fc484cc9c7b7fb

cm run script \
	--tags=run-mlperf,inference,_r4.1-dev,_short,_scc24-main \
	--model=sdxl \
	--implementation=reference \
	--framework=pytorch \
	--category=datacenter \
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

Platform: 4751fbf98487-reference-gpu-pytorch_v2.4.1-scc24-main

Model Precision: fp32

### Accuracy Results 
`CLIP_SCORE`: `13.90686`, Required accuracy for closed division `>= 31.68632` and `<= 31.81332`
`FID_SCORE`: `84.21082`, Required accuracy for closed division `>= 23.01086` and `<= 23.95008`

### Performance Results 
`Samples per second`: `0.665545`
