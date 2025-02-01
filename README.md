For pytorch code errors usually occur due to datatype, device type and shapes
You need the model, data and everything to be on the same device
In general first we import Data split into train and test sets and send to appropraite device
then visualize, visualize, visualize
then we make the model and choose the loss and optimzier 
for binary classification we use BCEWITHLOGITS and BCE Logits ---> Raw output of Model
for multiclass classification we use CrossEntropyLoss --> takes logits as inputs
for optimzer usually SGD AND ADAM (We can use Momentum aswell)
for Improving our model we can change the epochs, lr, loss function , optimizer, momentum, batch normalization(normalize output after each layer), dropout layers(randomly set output of neuron to 0),
we can calssify just about any shape using linear and non linear lines (we can add non linearity using Activation Functions) #ReLU usually works pretty fine
For linear Regression we dont need activation functions
number of outputs depends on the number of classes in classifcation problem
the output in regression is a number
