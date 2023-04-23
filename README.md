# adversarial_carlini_wagner_l2

https://colab.research.google.com/drive/1y_WE_hvVYt0pm9y8fNz2VAr96djiQEpQ?usp=sharing

It uses GPU for reasonable runite, so if you run it make sure you use Colab (or your own GPU). It may also have results with higher max iterations there.

Slides with thorough explainations on the original paper and the optimization problem it formulated, and the interesting objective function:
Towards evaluating the robustness of neural networks.pdf


min D(x, x+delta)

s.t. classification of (x+delta) = t
x+delta is in [0,1]^n

Reformolating using differents techniques so it can be solved using a gradient-based optimizer like ADAM or GD. Implementing ADAM itself is way out of scope of our project, we hope it's ok.

1. Expressing the formulation with different form (objective function)
2. Adding a constant
3. Box constraints using change of variables
4. Discretization

Original paper:
N. Carlini and D. Wagner, "Towards Evaluating the Robustness of Neural Networks," in 2017 IEEE Symposium on Security and Privacy (SP)
https://www.computer.org/csdl/proceedings-article/sp/2017/07958570/12OmNviHK8t
