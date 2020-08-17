# Course notes for fast.ai

Requires access to computer with NVIDIA GPU. I used Google Colab with [Cloud GPU](https://cloud.google.com/gpu) which has access to NVIDIA K80, P100, P4, T4, and V100 GPUs.


Google Colab : Enabling and testing the GPU
* Navigate to Edit → Notebook Settings
* Select GPU from the Hardware Accelerator drop-down

```python
%tensorflow_version 2.x
import tensorflow as tf
device_name = tf.test.gpu_device_name()
if device_name != '/device:GPU:0':
  raise SystemError('GPU device not found')
print('Found GPU at: {}'.format(device_name))
```
