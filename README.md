# octoml-examples

A public repository of helpful scripts, models, and useful resources for users of the OctoML Acceleration Platform.

UPDATE: [YOLOv4](https://github.com/onnx/models/raw/master/vision/object_detection_segmentation/yolov4/model/yolov4.tar.gz) and [SSD](https://github.com/onnx/models/raw/master/vision/object_detection_segmentation/ssd/model/ssd-10.tar.gz) models are now available.

Currently, this repository includes a small number of previously converted ONNX models for trial use with the OctoML Platform.

The OctoML Platform uses ONNX-RT, the runtime for the ONNX model format, as a second inferencing engine and common comparison point with TVM.  While we will attempt to support as many models as possible in ONNX-RT, not all models will run in ONNX-RT.

If you are unfamiliar with ONNX format models, we recommend using the [ONNX tutorials](https://github.com/onnx/tutorials#converting-to-onnx-format) to convert your model from TensorFlow, PyTorch, or other common model formats.

If you are unfamiliar with identifying input layer names and shapes in ONNX models, a useful third-party tool for model inspection is Netron (either [online](https://netron.app/) or via [local use](https://github.com/lutzroeder/netron)).

For BERT-based models, the OctoML Platform takes input shapes in the order specified by the ONNX model.  In order to begin optimizations, all input layer names and shapes must be entered.  For input shapes listed as 'unknown' or 'any,' the user must specify the shape.  In generic BERT models, this is typically the batch size of the model.  


An example set of appropriate input shapes for BERT is provided here:


<img width="482" alt="Screen Shot 2021-05-19 at 9 06 05 AM" src="https://user-images.githubusercontent.com/59585799/118846317-72b9c000-b881-11eb-8fe8-f2193e229645.png">
