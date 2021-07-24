**What's the advantage of a tensor over numpy arrays?**<br/>
Tensors can be run on a GPU or a TPU for faster processing.

**How to find whether a GPU is available?**
tf.config.list_physical_devices('GPU')
[PhysicalDevice(name='/physical_device:GPU:0', device_type='GPU')]

**@tf.function**
A way to speed of a regular python function

**Changeable Tensor**
tf.Variable
To change a value, <b>assign</b> method should be used

**Unchangeable Tensor**
tf.Constant

