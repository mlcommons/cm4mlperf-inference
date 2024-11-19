This experiment is generated using the [MLCommons Collective Mind automation framework (CM)](https://github.com/mlcommons/cm4mlops).

*Check [CM MLPerf docs](https://docs.mlcommons.org/inference) for more details.*

## Host platform

* OS version: Linux-5.14.0-427.26.1.el9_4.x86_64-x86_64-with-glibc2.34
* CPU version: x86_64
* Python version: 3.12.6 | packaged by Anaconda, Inc. | (main, Oct  3 2024, 07:30:27) [GCC 11.2.0]
* MLCommons CM version: 3.4.1

## CM Run Command

See [CM installation guide](https://docs.mlcommons.org/inference/install/).

```bash
pip install -U cmind

cm rm cache -f

cm pull repo mlcommons@cm4mlops --checkout=b32ded2a4c3039ad16dadc734bee03dd1a97f228

cm run script \
	--tags=run-mlperf,inference,_r4.1-dev \
	--model=bert-99 \
	--implementation=reference \
	--framework=pytorch \
	--category=edge \
	--scenario=Offline \
	--execution_mode=valid \
	--device=cpu \
	--quiet
```
*Note that if you want to use the [latest automation recipes](https://docs.mlcommons.org/inference) for MLPerf (CM scripts),
 you should simply reload mlcommons@cm4mlops without checkout and clean CM cache as follows:*

```bash
cm rm repo mlcommons@cm4mlops
cm pull repo mlcommons@cm4mlops
cm rm cache -f

```

## Results

Platform: atl1_1_02_010_5_1.pace.gatech.edu-reference-cpu-pytorch-v2.4.1-default_config

Model Precision: fp32

### Accuracy Results 
`F1`: `90.87487`, Required accuracy for closed division `>= 89.96526`

### Performance Results 
`Samples per second`: `4.46232`
