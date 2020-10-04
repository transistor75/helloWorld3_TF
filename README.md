# helloWorld3_TF
this project is aimed to show how to use TensorFlow lite on microcontroller (XinaBox CW02 board)

download the project, open it with arduino ide and download the code into the microcontroller

the SW has been tested on XinaBox CW02 + IP01

the training of the model has been performed using Tensorflow2 and colab
it's an hello world application for TensorFlow on microcontroller.
The nn is trained to learn the behaviour of y=x/3+sin(x) in 0..2pi

the microcontroller evaluate 1500 samples in 0..2pi then
places the calculated x value in the model's input tensor

  input->data.f[0] = x_val;

and then Run inference, and report any error

  TfLiteStatus invoke_status = interpreter->Invoke();
  
the result is sent to the output via serialport and can be viewed by 
Arduino Serial Plotter
