For pytorch code errors usually occur due to datatype, device type, and shapes.  
You need the model, data, and everything to be on the same device.  

In general, first we import Data, split into train and test sets, and send them to the appropriate device.  
Then visualize, visualize, visualize.  

Then we make the model and choose the loss and optimizer.  

For binary classification, we use **BCEWithLogitsLoss** and **BCE Loss** → Raw output of Model.  
For multiclass classification, we use **CrossEntropyLoss** → takes logits as inputs.  

For optimizer, usually **SGD** and **Adam** (We can use Momentum as well).  

For improving our model we can change:  
- epochs  
- learning rate  
- loss function  
- optimizer  
- momentum  
- batch normalization (normalize output after each layer)  
- dropout layers (randomly set output of neuron to 0)

We can classify just about any shape using linear and non-linear lines (we can add non-linearity using Activation Functions).  
**ReLU** usually works pretty fine.

For linear regression, we don’t need activation functions.  
The number of outputs depends on the number of classes in the classification problem.  
The output in regression is a number.
We can also save and load our models using torch save and torch load and we should save the state dict and with weights only.
For saving the models we uslaly also use the PATH Module.

We can use the torchMetrics Library for evaluating our resutls.

Accuracy is useful when the different classes have equal data.

Recall means how many of the TPs were we able to correctly identify.

Precision means how many of the Tps that we identified were actually correct.

As prevision goes up recall usually goes down and vice versa.

F1 score is the combination of Recall and Precision with harmonic mean (so that the recall and precision is weighted equally).

Matplotlib expect the color channels in different place than pytorch so be aware of that.

You can individually call your block layers and see the output shapes to see what you should put in the sequential layers.

So you can pass dummy data and just print the shapes of the tensors after coming from the different blocks.
