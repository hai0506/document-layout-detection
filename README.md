# document-layout-detection

YoloV9 models for document layout detection.

The classes are text, title, list-item, table, figure.

Inference can be done with infer_onnx.ipynb and infer_triton.ipynb.

For infer_onnx, install the onnxruntime library:
```
pip install onnxruntime
```
More information at https://github.com/microsoft/onnxruntime

For infer_triton, set up a Triton inference server using Docker:
```
docker run --rm -p 8000:8000 -p 8001:8001 -p 8002:8002 -v "$(pwd)/model_repo:/models" nvcr.io/nvidia/tritonserver:22.09-py3 tritonserver --model-repository=/models --exit-on-error=false
```
More information at https://github.com/triton-inference-server/server
