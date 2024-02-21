# Advancing-Embryo-Selection
In this project, we coded in google colab (model ResNet50 and VGG19) and Kaggle (model EfficientNetB0 and MobileNet)
This is link for dataset in google colab : 
**Folder** include data and weight : https://drive.google.com/drive/folders/16zJAxbMP60m8rXofWHwSpgK9qd-s_8qL?usp=sharing (folder name "cuoc_thi_wcs2023_p2")
Train dataset : https://drive.google.com/drive/folders/1PjbqQfP5SAfL5hvRxGJFfd1Lx7BqKIkP?usp=sharing
Validation dataset : https://drive.google.com/drive/folders/1WitdlpCLiU5d_EI8pYYPiUAut5zOgQZr?usp=sharing
Test dataset : https://drive.google.com/drive/folders/1Kzgktxv18shSKyhMoQKzD7RzOjmmMHg7?usp=sharing

First you need to share the **Folder** to **My drive** in google Drive, to ensure the path in your colab is "/content/drive/MyDrive/cuoc_thi_wcs2023_p2/..."
In "Load data" part, default label mode is "categorical", and output of model is 2. You can change label mode to, e.g. binary, and you need to change number of output class of model from 2 to 1, change activation function, and change loss function suitably.
In "parameter-version" part, there are some variable : 
# "version" is the number of version we train, e.g. "version" = 58 that means this is the 58th model.
# "mode_train" is the variable that help you know your model was trained with what mode, e.g you were fine tunned the original model, you set this parameter is "fine_tuning" to know in this version, you fine tuned your model.
# "activation_func" is the activation function you want to use, e.g. : softmax function.
# "loss_func" is the loss function you want to use, e.g. : categorical_crossentropy.
# "model" is the name of model you want to use, e.g. : VGG19 (just having 2 model are ResNet50 and VGG19).
# "output_class" is the number of output class of model, e.g. : 2 for categorical and 1 for binary.
# "threshold" is the threshold for classification (just use this parameter if you choose binary mode)
GradCam you need to choose layer before you run code, in this case, we use layer **conv5_block3_3_conv** for ResNet50 model and layer **block5_conv4** for VGG19 model.
