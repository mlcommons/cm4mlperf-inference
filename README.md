Please download [summary.xlsx](summary.xlsx) to view the most recent results. 
 ```
[2024-10-07 20:56:27,354 submission_checker1.py:2936 INFO] Results=6, NoResults=0, Power Results=0
[2024-10-07 20:56:27,355 submission_checker1.py:2943 INFO] ---
[2024-10-07 20:56:27,355 submission_checker1.py:2944 INFO] Closed Results=0, Closed Power Results=0

[2024-10-07 20:56:27,355 submission_checker1.py:2949 INFO] Open Results=6, Open Power Results=0

[2024-10-07 20:56:27,355 submission_checker1.py:2954 INFO] Network Results=0, Network Power Results=0

[2024-10-07 20:56:27,355 submission_checker1.py:2959 INFO] ---
[2024-10-07 20:56:27,355 submission_checker1.py:2961 INFO] Systems=5, Power Systems=0
[2024-10-07 20:56:27,355 submission_checker1.py:2962 INFO] Closed Systems=0, Closed Power Systems=0
[2024-10-07 20:56:27,355 submission_checker1.py:2967 INFO] Open Systems=5, Open Power Systems=0
[2024-10-07 20:56:27,355 submission_checker1.py:2972 INFO] Network Systems=0, Network Power Systems=0
[2024-10-07 20:56:27,355 submission_checker1.py:2977 INFO] ---
[2024-10-07 20:56:27,355 submission_checker1.py:2982 INFO] SUMMARY: submission looks OK
INFO:root:       ! call "postprocess" from /home/runner/CM/repos/mlcommons@cm4mlops/script/run-mlperf-inference-submission-checker/customize.py

```

|    | Organization   | Availability   | Division   | SystemType   | SystemName   | Platform                                               | Model               | MlperfModel         | Scenario   |    Result | Accuracy                                                      |   number_of_nodes | host_processor_model_name   |   host_processors_per_node |   host_processor_core_count | accelerator_model_name   |   accelerators_per_node | Location                                                                                                  | framework      | operating_system                                | notes                             |   compliance |   errors | version   |   inferred | has_power   | Units     | weight_data_types   |
|---:|:---------------|:---------------|:-----------|:-------------|:-------------|:-------------------------------------------------------|:--------------------|:--------------------|:-----------|----------:|:--------------------------------------------------------------|------------------:|:----------------------------|---------------------------:|----------------------------:|:-------------------------|------------------------:|:----------------------------------------------------------------------------------------------------------|:---------------|:------------------------------------------------|:----------------------------------|-------------:|---------:|:----------|-----------:|:------------|:----------|:--------------------|
|  0 | MLCommons      | available      | open       | datacenter   | 48ed6105bd85 | 48ed6105bd85-nvidia-gpu-TensorRT-scc24-main            | stable-diffusion-xl | stable-diffusion-xl | Offline    |  1.13292  | CLIP_SCORE: 15.586050063371658  FID_SCORE: 236.8087101317688  |                 1 | Intel(R) Xeon(R) w7-2495X   |                          1 |                          24 | NVIDIA GeForce RTX 4090  |                       1 | open/MLCommons/results/48ed6105bd85-nvidia-gpu-TensorRT-scc24-main/stable-diffusion-xl/offline            | TensorRT       | Ubuntu 20.04 (linux-6.2.0-39-generic-glibc2.31) | Automated by MLCommons CM v2.3.6. |            1 |        0 | v4.1      |          0 | False       | Samples/s | int8                |
|  1 | MLCommons      | available      | open       | datacenter   | 48ed6105bd85 | 48ed6105bd85-nvidia-gpu-TensorRT-scc24-base            | stable-diffusion-xl | stable-diffusion-xl | Offline    |  1.13598  | CLIP_SCORE: 15.586050063371658  FID_SCORE: 236.8087101317688  |                 1 | Intel(R) Xeon(R) w7-2495X   |                          1 |                          24 | NVIDIA GeForce RTX 4090  |                       1 | open/MLCommons/results/48ed6105bd85-nvidia-gpu-TensorRT-scc24-base/stable-diffusion-xl/offline            | TensorRT       | Ubuntu 20.04 (linux-6.2.0-39-generic-glibc2.31) | Automated by MLCommons CM v2.3.6. |            1 |        0 | v4.1      |          0 | False       | Samples/s | int8                |
|  2 | MLCommons      | available      | open       | edge         | gh_action    | gh_action-reference-gpu-pytorch_v2.4.1-default_config  | gptj-99             | gptj-99             | Offline    | 52.9478   | nan                                                           |                 1 | Intel(R) Xeon(R) w7-2495X   |                          1 |                          24 | NVIDIA GeForce RTX 4090  |                       1 | open/MLCommons/results/gh_action-reference-gpu-pytorch_v2.4.1-default_config/gptj-99/offline              | pytorch v2.4.1 | Ubuntu 22.04 (linux-6.2.0-39-generic-glibc2.35) | Automated by MLCommons CM v2.3.4. |            1 |        0 | v4.1      |          0 | False       | Tokens/s  | fp32                |
|  3 | MLCommons      | available      | open       | edge         | gh_action    | gh_action-reference-gpu-pytorch_v2.4.1-default_config  | stable-diffusion-xl | stable-diffusion-xl | Offline    |  0.345721 | CLIP_SCORE: 15.18544016778469  FID_SCORE: 235.69504308101006  |                 1 | Intel(R) Xeon(R) w7-2495X   |                          1 |                          24 | NVIDIA GeForce RTX 4090  |                       1 | open/MLCommons/results/gh_action-reference-gpu-pytorch_v2.4.1-default_config/stable-diffusion-xl/offline  | pytorch v2.4.1 | Ubuntu 22.04 (linux-6.2.0-39-generic-glibc2.35) | Automated by MLCommons CM v2.3.4. |            1 |        0 | v4.1      |          0 | False       | Samples/s | fp32                |
|  4 | MLCommons      | available      | open       | datacenter   | 48ed6105bd85 | 48ed6105bd85-reference-gpu-pytorch_v2.1.0a0-scc24-base | stable-diffusion-xl | stable-diffusion-xl | Offline    |  0.373636 | CLIP_SCORE: 15.236237794160843  FID_SCORE: 238.78369342212613 |                 1 | Intel(R) Xeon(R) w7-2495X   |                          1 |                          24 | NVIDIA GeForce RTX 4090  |                       1 | open/MLCommons/results/48ed6105bd85-reference-gpu-pytorch_v2.1.0a0-scc24-base/stable-diffusion-xl/offline | TensorRT       | Ubuntu 20.04 (linux-6.2.0-39-generic-glibc2.31) | Automated by MLCommons CM v2.3.6. |            1 |        0 | v4.1      |          0 | False       | Samples/s | fp32                |
|  5 | MLCommons      | available      | open       | datacenter   | f9ac88850adc | f9ac88850adc-reference-gpu-pytorch_v2.4.1-scc24-base   | stable-diffusion-xl | stable-diffusion-xl | Offline    |  0.376944 | CLIP_SCORE: 15.18544016778469  FID_SCORE: 235.69504308101006  |                 1 | Intel(R) Xeon(R) w7-2495X   |                          1 |                          24 | NVIDIA GeForce RTX 4090  |                       1 | open/MLCommons/results/f9ac88850adc-reference-gpu-pytorch_v2.4.1-scc24-base/stable-diffusion-xl/offline   | pytorch v2.4.1 | Ubuntu 22.04 (linux-6.2.0-39-generic-glibc2.35) | Automated by MLCommons CM v2.3.9. |            1 |        0 | v4.1      |          0 | False       | Samples/s | fp32                |