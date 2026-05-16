# DATA425. Foundations of Deep Learning

Ten Jupyter notebook labs from the DATA425 course. Each lab pairs the lecture theory with runnable code on small datasets so the learning behaviour is easy to inspect.

## Labs

### Lab 1. Artificial Neural Networks in Keras
This lab introduces neural networks in Keras through small two-dimensional datasets where decision boundaries can be plotted directly. It contrasts a single sigmoid unit, which behaves like logistic regression, against multi-layer networks with ReLU activations. The same ideas are extended to multi-class classification using softmax on a three-class spiral problem.

[Open notebook](DATA425_Lab1_Artificial_Neural_Networks_in_Keras.ipynb)

### Lab 2. Loss Functions and Gradient Descent
This lab focuses on how neural networks actually learn by working through regression losses such as MAE and MSE, binary cross-entropy, and softmax cross-entropy. It then implements gradient descent from scratch on a linear regression problem and shows that Keras automates the same training loop using automatic differentiation.

[Open notebook](DATA425_Lab2_LossFunctions_GradientDescent.ipynb)

### Lab 3. Backpropagation, Vanishing Gradients, Weight Initialisation and Momentum
This lab opens up the mechanics of training by computing backpropagation by hand on a tiny tanh network and then exploring why gradients vanish or explode in deeper architectures. It examines activation derivatives, Xavier and He initialisation, and the behaviour of momentum and Adam on a narrow bowl-shaped loss surface, finishing with a Keras comparison of sigmoid versus ReLU on the moons dataset.

[Open notebook](DATA425_Lab3_Backpropagation_VanishingGradients_Momentum.ipynb)

### Lab 4. Adaptive Optimisers, Regularisation and Optuna
This lab compares SGD, RMSProp, and Adam on the handwritten digits dataset, then diagnoses overfitting using training and validation curves before applying L2 regularisation, dropout, and early stopping. It closes with an automated hyperparameter search using Optuna, demonstrating a full development workflow that keeps test data reserved for the final evaluation.

[Open notebook](DATA425_Lab4_AdaptiveOptimisers_Regularisation_Optuna.ipynb)

### Lab 5. Regularisation, Diagnostics, and Convolutional Neural Networks
This lab uses PyTorch to teach diagnostic reading of training and validation curves, distinguishing underfitting, good fit, and overfitting on a noisy regression task with dropout and weight decay as remedies. It then introduces convolutional neural networks by comparing a plain MLP with a small CNN on the digits dataset and inspecting learned filters and confusion matrices for error analysis.

[Open notebook](DATA425_Lab5_Regularisation_Diagnostics_CNNs.ipynb)

### Lab 6. CNNs, Training, Transfer Learning, and Fine-Tuning
This lab walks through CNN fundamentals including image tensor shapes, manual 2D convolution with edge filters, stride and padding output sizes, pooling, and a backbone-plus-head architecture trained on handwritten digits. It then demonstrates transfer learning by freezing the trained backbone for a parity task, fine-tunes the model on noisy images, and showcases residual blocks and multitask heads sharing a single embedding.

[Open notebook](DATA425_Lab6_CNN_Transfer_Finetuning.ipynb)

### Lab 7. Denoising Autoencoders
This lab builds a denoising autoencoder that maps corrupted digit images back to clean reconstructions through a tight 8-dimensional bottleneck. It connects the bottleneck to the manifold intuition, visualises the learned codes with PCA, and uses reconstruction error as a simple anomaly signal by training only on digits 0 to 4 and testing on digits 5 to 9.

[Open notebook](DATA425_Lab7_Denoising_Autoencoder.ipynb)

### Lab 8. Convolutional Autoencoders and Variational Autoencoders
This lab extends the autoencoder idea using a convolutional encoder and an Upsample plus Conv decoder that preserves spatial structure, then compares pixel-space and latent-space interpolation between two digits. It also builds a variational autoencoder with a 2D latent space, demonstrating the reparameterisation trick, the KL regularisation term, and generation by decoding samples drawn from a standard Gaussian prior.

[Open notebook](DATA425_Lab8_Convolutional_AE_and_VAE.ipynb)

### Lab 9. RNNs and LSTMs for Time-Series Forecasting
This lab forecasts a synthetic KatCoin time series with trend, seasonality, noise, and a regime shift, using sliding windows of 60 past values to predict 10 steps ahead. It compares a vanilla RNN against an LSTM with gradient clipping, illustrates vanishing and exploding gradients through long recurrent products, and benchmarks both against a last-value baseline on a held-out test period.

[Open notebook](DATA425_Lab9_RNN_LSTM_Time_Series.ipynb)

### Lab 10. Seq2Seq, Attention, and Transformers
This lab builds a tiny encoder-decoder Transformer that translates English digit words into French digit words, walking through tokens, embeddings, scaled dot-product attention, causal masking, and multi-head attention. It demonstrates autoregressive greedy decoding, visualises learned cross-attention alignments between source and target tokens, and contrasts BERT-style masked-token training with GPT-style next-token training.

[Open notebook](DATA425_Lab10_Seq2Seq_Attention_Transformers.ipynb)
