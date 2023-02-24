# memtrace_DeepLearning
memory access traces of four popular deep learning workloads consisting of Internet Movie DataBase (IMDB), Spam detection, Modified National Institute of Standards and Technology database (MNIST), and Fashion MNIST.

We extract memory access traces while executing TensorFlow with LSTM and Convolution layers. For collecting memory access traces of deep learning workloads, we make use of the Callgrind module of the Valgrind toolset.

The brief descriptions of these workloads are as follows.

- **IMDB** : identifying positive or negative ratings from 50,000 movie reviews by utilizing 1-dimensional Convolution layers. 
- **Spam detection** : determining whether an email is a spam or not based on the content of the email by utilizing LSTM layers.
- **Fashion MNIST** : classifying 10 kinds of clothing images including shoes, bags, and pants by utilizing 2-dimensional Convolution layers.
- **MNIST** : classifying text images of digits 0 to 9 by utilizing LSTM layers.

## 
Each trace file contains three columns: reference type, virtual address, and access size.
1. **Reference Type** : can be one of instruction read (readi), data read (readd), or data write (write)
2. **Virtual Address** : listed in hexadecimal
3. **Access Size** : listed in bytes

Up to 4.5 milion lines of trace per each file

## 
The following is an example of a trace file.
```
readi 0x04935caf 6 
write 0x1ffefff6d0 4 
readi 0x04935cbe 5 
write 0x1ffefff6b8 8 
readi 0x048e7670 4 
readi 0x048e767c 8 
readd 0x04c0ea48 4 
readi 0x048a4f97 4 
readd 0x04a44460 8 
readi 0x048a4fbc 5 
readd 0x04c0e770 8 
readi 0x04a57cc0 4 
readd 0x1ffefff738 8 
write 0x04c0ea38 8 
```
