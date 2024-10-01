This experiment is generated using the [MLCommons Collective Mind automation framework (CM)](https://github.com/mlcommons/cm4mlops).

*Check [CM MLPerf docs](https://docs.mlcommons.org/inference) for more details.*

## Host platform

* OS version: Linux-6.2.0-39-generic-x86_64-with-glibc2.35
* CPU version: x86_64
* Python version: 3.10.12 (main, Sep 11 2024, 15:47:36) [GCC 11.4.0]
* MLCommons CM version: 2.3.6

## CM Run Command

See [CM installation guide](https://docs.mlcommons.org/inference/install/).

```bash
pip install -U cmind

cm rm cache -f

cm pull repo gateoverflow@cm4mlops --checkout=3dbea4a03583d31eb1a07a026b6b316028258643

cm run script \
	--tags=app,mlperf,inference,generic,_reference,_sdxl,_pytorch,_cuda,_test,_r4.1-dev_default,_float16,_offline \
	--quiet=true \
	--env.CM_QUIET=yes \
	--env.CM_MLPERF_IMPLEMENTATION=reference \
	--env.CM_MLPERF_MODEL=sdxl \
	--env.CM_MLPERF_RUN_STYLE=test \
	--env.CM_MLPERF_BACKEND=pytorch \
	--env.CM_MLPERF_CLEAN_ALL=True \
	--env.CM_MLPERF_DEVICE=cuda \
	--env.CM_MLPERF_USE_DOCKER=True \
	--env.CM_HW_NAME=gh_action \
	--env.CM_MLPERF_MODEL_PRECISION=float16 \
	--env.OUTPUT_BASE_DIR=/home/arjun/gh_action_results \
	--env.CM_MLPERF_LOADGEN_SCENARIO=Offline \
	--env.CM_MLPERF_INFERENCE_SUBMISSION_DIR=/home/arjun/gh_action_submissions \
	--env.CM_MLPERF_SUBMITTER=MLCommons \
	--env.CM_MLPERF_LOADGEN_TARGET_QPS=1 \
	--env.CM_TEST_QUERY_COUNT=1 \
	--env.CM_MLPERF_LOADGEN_COMPLIANCE=no \
	--env.CM_MLPERF_SUBMISSION_RUN=yes \
	--env.CM_RUN_MLPERF_ACCURACY=on \
	--env.CM_RUN_SUBMISSION_CHECKER=yes \
	--env.CM_TAR_SUBMISSION_DIR=yes \
	--env.CM_MLPERF_SUBMISSION_GENERATION_STYLE=short \
	--env.CM_MLPERF_LOADGEN_ALL_MODES=yes \
	--env.CM_MLPERF_INFERENCE_VERSION=4.1-dev \
	--env.CM_RUN_MLPERF_INFERENCE_APP_DEFAULTS=r4.1-dev_default \
	--env.CM_MLPERF_LAST_RELEASE=v4.0 \
	--env.CM_TMP_CURRENT_PATH=/home/arjun/actions-runner/_work/cm4mlops/cm4mlops \
	--env.CM_TMP_PIP_VERSION_STRING= \
	--env.CM_MODEL=sdxl \
	--env.CM_MLPERF_CLEAN_SUBMISSION_DIR=yes \
	--env.CM_RERUN=yes \
	--env.CM_MLPERF_LOADGEN_EXTRA_OPTIONS= \
	--env.CM_MLPERF_LOADGEN_MODE=performance \
	--env.CM_MLPERF_LOADGEN_SCENARIOS,=Offline \
	--env.CM_MLPERF_LOADGEN_MODES,=performance,accuracy \
	--env.CM_OUTPUT_FOLDER_NAME=test_results \
	--add_deps_recursive.compiler.tags=gcc \
	--add_deps_recursive.submission-checker.tags=_short-run \
	--add_deps_recursive.get-mlperf-inference-results-dir.tags=_version.r4_1-dev \
	--add_deps_recursive.get-mlperf-inference-submission-dir.tags=_version.r4_1-dev \
	--add_deps_recursive.mlperf-inference-nvidia-scratch-space.tags=_version.r4_1-dev \
	--adr.compiler.tags=gcc \
	--adr.submission-checker.tags=_short-run \
	--adr.get-mlperf-inference-results-dir.tags=_version.r4_1-dev \
	--adr.get-mlperf-inference-submission-dir.tags=_version.r4_1-dev \
	--adr.mlperf-inference-nvidia-scratch-space.tags=_version.r4_1-dev \
	--v=False \
	--print_env=False \
	--print_deps=False \
	--dump_version_info=True \
	--env.OUTPUT_BASE_DIR=/home/arjun/gh_action_results \
	--env.CM_MLPERF_INFERENCE_SUBMISSION_DIR=/home/arjun/gh_action_submissions
```
*Note that if you want to use the [latest automation recipes](https://docs.mlcommons.org/inference) for MLPerf (CM scripts),
 you should simply reload gateoverflow@cm4mlops without checkout and clean CM cache as follows:*

```bash
cm rm repo gateoverflow@cm4mlops
cm pull repo gateoverflow@cm4mlops
cm rm cache -f

```

## Results

Platform: gh_action-reference-gpu-pytorch_v2.4.1-default_config

Model Precision: fp32

### Accuracy Results 
`CLIP_SCORE`: `15.18544`, Required accuracy for closed division `>= 31.68632` and `<= 31.81332`
`FID_SCORE`: `235.69504`, Required accuracy for closed division `>= 23.01086` and `<= 23.95008`

### Performance Results 
`Samples per second`: `0.345721`
