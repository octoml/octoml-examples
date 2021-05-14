# octomizer-examples

A public repository of helpful scripts, models, and useful resources for users of the Octomizer.

UPDATE: [YOLOv4](https://github.com/onnx/models/raw/master/vision/object_detection_segmentation/yolov4/model/yolov4.tar.gz) and [SSD](https://github.com/onnx/models/raw/master/vision/object_detection_segmentation/ssd/model/ssd-10.tar.gz) models are now available.

Currently, this repository includes a small number of previously converted ONNX models for trial use with the Octomizer.

If you are unfamiliar with ONNX format models, we recommend using the [ONNX tutorials](https://github.com/onnx/tutorials#converting-to-onnx-format) to convert your model from TensorFlow, PyTorch, or other common model formats.

If you are unfamiliar with identifying input layer names and shapes in ONNX models, a useful third-party tool for model inspection is Netron (either [online](https://netron.app/) and via [local use](https://github.com/lutzroeder/netron).

For computer vision models, the Octomizer takes input shapes in NCHW format.

For BERT-based models, the Octomizer takes input shapes in the order specified by the ONNX model (for example, the input mask is often rendered as input_mask:0 with datatype int64 and shape [batch_size, sequence_length].  In order to begin optimizations, all input layer names and shapes must be entered.  For input shapes listed as 'unknown' or 'any,' the user must specify the shape.  In generic BERT models, this is typically the batch size of the model.  An example appropriate input name and shape is: input name=input_mask:0, datatype=int64, input shape=[1, 256]. 

The Octomizer uses ONNX-RT, the runtime for the ONNX model format, as a second inferencing engine and common comparison point with TVM.  While we will attempt to support as many models as possible in ONNX-RT, not all models will run in ONNX-RT.
