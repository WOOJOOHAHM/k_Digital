# k_Digital
4 channel Data in 3 channel pretrained model
https://blog.naver.com/hahmwj/222854175154

I tuned pretrained model' input size in tensorflow(res50, vgg16) but my data's shape is (28,28,4).

Solution1
Fine tuning Transfer Model 3 to 4
I tryed to fin tune model's input size 3 channels to 4channels and (28, 28, 3) to (32, 32, 3).
But it's acc is to low.

Solution2
Data Squeeze 4 channel to 3channel v2.ipynb
So I transpose mu dataset to 4 3 channels Datasets finally it got 4 kinds of model that shape (28, 28, 3)
and use augmentation method by ImageGenretor by tensorflow.
 Also, I used ZeroPadding method to transpose (28, 28, 3) to (32, 32, 3).
 
For evlaution
For test Last Model.ipynb
First, I transpose my test dataset (28, 28, 4) to (32, 32, 3) either upper one,
Second, I make 4 * len(model count) condition. and evaluate each other then choose best acc in the array.
