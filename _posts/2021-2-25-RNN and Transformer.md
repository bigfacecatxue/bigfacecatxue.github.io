# RNN and Transformer

## RNN
Recurrent neural networks works well for language model. It takes a sequence of words as input. Each word represented as a word embedding, with previous hidden layer together can calculate current hidden layer, multiply current hidden layer with a matrix and pass it to softmax, can predict next word.

## Vanishing and exploding gradients
RNN calculate words step by step, and share same matrix for hidden layers, so when do backpropogation, matrix parameters multiplied many times. And when a number multiplied by itself many times, it will explode or converge to 0. So gradients will explode or vanish.

## LSTM
LSTM adds hidden state and cell state at each step t, by using three gates(forget gate/ input gete/ output gate) to help control information pass through sequence words. LSTM can't guarantee that there is no vanishing or exploding gradient, but it does provide an easier way for the model to learn long-distance dependencies.

## Transformer
Transformer model is currently the most frequently used model for natural language processing. Transformer model abandoned sequential calculating, only use self-attention to represent sequence words meaning. By doing this, transformer model not only train fast, but also improved performence on almost all natural language processing tasks. Recent researches state that fine-tuning pretrained transformer model can achieve great results on many tasks.
