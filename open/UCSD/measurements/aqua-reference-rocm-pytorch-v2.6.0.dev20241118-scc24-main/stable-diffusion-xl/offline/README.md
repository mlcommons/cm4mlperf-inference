This experiment is generated using the [MLCommons Collective Mind automation framework (CM)](https://github.com/mlcommons/cm4mlops).

*Check [CM MLPerf docs](https://docs.mlcommons.org/inference) for more details.*

## Host platform

* OS version: Linux-5.14.0-427.42.1.el9_4.x86_64-x86_64-with-glibc2.35
* CPU version: x86_64
* Python version: 3.10.15 (main, Oct  3 2024, 07:27:34) [GCC 11.2.0]
* MLCommons CM version: 3.4.1

## CM Run Command

See [CM installation guide](https://docs.mlcommons.org/inference/install/).

```bash
pip install -U cmind

cm rm cache -f

cm pull repo mlcommons@cm4mlops --checkout=b32ded2a4c3039ad16dadc734bee03dd1a97f228

cm run script \
	--tags=run-mlperf,inference,_r4.1-dev,_scc24-main \
	--model=sdxl \
	--framework=pytorch \
	--category=datacenter \
	--scenario=Offline \
	--execution_mode=test \
	--device=rocm \
	--quiet \
	--precision=float16 \
	--adr.mlperf-implementation.tags=_branch.multinode-test,_repo.https://github.com/zixianwang2022/mlperf-scc24 \
	--adr.mlperf-implementation.version=custom \
	--env.CM_GET_PLATFORM_DETAILS=no \
	--target_qps=1.8 \
	--rerun
```
*Note that if you want to use the [latest automation recipes](https://docs.mlcommons.org/inference) for MLPerf (CM scripts),
 you should simply reload mlcommons@cm4mlops without checkout and clean CM cache as follows:*

```bash
cm rm repo mlcommons@cm4mlops
cm pull repo mlcommons@cm4mlops
cm rm cache -f

```

## Results

Platform: aqua-reference-rocm-pytorch-v2.6.0.dev20241118-scc24-main

Model Precision: fp32

### Accuracy Results 
`CLIP_SCORE`: `15.22522`, Required accuracy for closed division `>= 31.68632` and `<= 31.81332`
`FID_SCORE`: `84.25505`, Required accuracy for closed division `>= 23.01086` and `<= 23.95008`

### Performance Results 
`Samples per second`: `1.5779`
