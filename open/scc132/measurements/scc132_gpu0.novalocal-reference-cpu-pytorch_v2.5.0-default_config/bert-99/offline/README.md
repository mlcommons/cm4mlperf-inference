This experiment is generated using the [MLCommons Collective Mind automation framework (CM)](https://github.com/mlcommons/cm4mlops).

*Check [CM MLPerf docs](https://docs.mlcommons.org/inference) for more details.*

## Host platform

* OS version: Linux-6.1.110-1.el9.elrepo.x86_64-x86_64-with-glibc2.34
* CPU version: x86_64
* Python version: 3.11.7 (main, Oct 21 2024, 23:35:59) [GCC 11.4.1 20231218 (Red Hat 11.4.1-3)]
* MLCommons CM version: 3.2.6

## CM Run Command

See [CM installation guide](https://docs.mlcommons.org/inference/install/).

```bash
pip install -U cmind

cm rm cache -f

cm pull repo mlcommons@cm4mlops --checkout=6dbb26a3da6b8ebdbc96be3be3a0e9817d3b6d26

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

Platform: scc132_gpu0.novalocal-reference-cpu-pytorch_v2.5.0-default_config

Model Precision: fp32

### Accuracy Results 
`F1`: `90.87487`, Required accuracy for closed division `>= 89.96526`

### Performance Results 
`Samples per second`: `1.96994`
