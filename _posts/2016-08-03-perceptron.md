---
layout: post
title:  "Perceptron"
date:  2016-08-03 13:16
categories: ml
---
### Perceptron
입력의 가중합이 임계치를 넘는지에 따라 바이너리를 출력한다.

\\[
output =
\begin{cases}
0  & \text{ if } \mathbf{w}^{T}\mathbf{x} + b \le 0 \cr
1  & \text{ if } \mathbf{w}^{T}\mathbf{x} + b \gt 0
\end{cases}
\\]

단순해 보이는데 퍼셉트론 몇개를 연결하면 NAND게이트를 구현할 수 있다. NAND 조합으로 컴퓨터의 모든 논리회로를 만들 수 있으니 계산에 있어 보편성이 있는 셈이다. 그뿐 아니라 퍼셉트론의 가중치 조정을 통해 상당히 복잡한 논리회로로가 필요한 해법도 쉽게 구현 가능하다.

하지만 퍼셉트론으로 구성된 네트워크는 학습하기 어렵다. 어느 지점까지는 \\(w_{j}\\)와 \\(b\\)의 변화에 반응이 없다가 어느 순간 출력이 바뀌는 특성때문에 가중치 변화에 따른 출력의 변화를 예상하기 힘들기 때문이다.


### Neuron
뉴런은 가중합을 어떤 함수에 한번 더 통과시킨다. 함수 \\(f(\cdot)\\)를 activation function이라 한다.

\\[
output = \f(\mathbf{w}^{T}\mathbf{x} + b)
\\]

이 함수가 \\(\sigma(\cdot)\\) 이면 함수의 이름을 따라 시그모이드 뉴런<sup>sigmoid neuron</sup>이라 부른다. 




### References
1. [http://neuralnetworksanddeeplearning.com/chap1.html](http://neuralnetworksanddeeplearning.com/chap1.html)
