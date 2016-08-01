---
layout: post
title:  "Likelihood"
date:  2016-07-31 23:52
categories: ml
---

### Likelihood Function
우도함수<sup>likelihood function</sup>는 이산형 확률변수에서는 확률질량함수<sup>probability mass function</sup>, 연속형에서는 확률밀도함수<sup>probability density function</sup>의 수식과 완전한 동치이다. 확률질량함수와 확률밀도함수는 보통 별개로 다루지만 여기서의 논의상 차이가 없어 하나의 함수 \\(p\\)로 표현하고 확률함수로 통칭하겠다.

어떤 표본공간<sup>sample space</sup> 에서 정의된 확률변수 \\(A\\)의 값 \\(a\\)에 대하여 모수<sup>parameter</sup> \\(b\\)를 가지는 확률모델은 조건부 확률함수 \\(p(a\|b)\\)로 나타낼 수 있다. 모델의 모수 \\(b\\)는 확률함수의 모양을 결정짓는다. 이 함수는 \\(a\\)에 대한 함수로 \\(b\\)는 고정된 상수로 취급한다. 반대로 우도함수는 \\(b\\)에 대한 함수로 \\(a\\)가 고정되어 있다고 본다.

둘을 구분하기 위해 우도함수를 \\(\mathcal{L}(b\|a) \\)이나 \\(p_{b}(a)\\)와 같이 표기하기도 하지만, 표현방법은 아무래도 좋다. 문맥상 혼동의 우려가 없으면 \\(p(a\|b)\\)라 쓰고 우도함수로 취급해도 된다. 특히, 베이지안 추론에서는 고정된 관측데이터를 가지고 모수를 추정 하기 때문에 보통 \\(p(a\|b)\\)를 우도함수로써 다룬다. 문맥상 함수를 다루는 관점이 어느 쪽인지가 중요하다. (사실 정확한 표기법이 뭔지 찾다가 관뒀다.)

다음의 정규분포식을 \\(x\\)에 대한 확률밀도함수로, \\(\sigma\\)에 대한 우도함수로 각각 그려보았다.
\\[
p(x|\mu, \sigma) = \frac{1}{\sigma \sqrt {2 \pi }} e^{ { - \left( {x - \mu } \right)^2 } / {2\sigma ^2 } }
\\]

![probability_likelihood](/images/likelihood-fig1.png)

당연하게도 형태가 상당히 다르다. 특히 왼쪽그래프는 확률의 특성상 적분하면 1이 얻어지지만 오른쪽 그래프는 1이 얻어지지 않는다. 무슨값이 나오는지 계산해보진 않았지만 일단 모양이 많이 다르다.

### References
* Doing Bayesian Data Analysis, Second Edition, p125
* https://en.wikipedia.org/wiki/Likelihood_function
  * 여기의 표기법은 좀 혼동스럽다. 위키만으로는 \\(\mathcal{L}(b\|a) \\)을 우도값으로 봐야할지, 우도함수로 봐야할지 잘 모르겠다.
  * 확률과 확률밀도함수는 구분지어서 이야기하는데, 우도도 그래야하지 않을까.
* https://en.wikipedia.org/wiki/Probability_density_function
* https://en.wikipedia.org/wiki/Conditional_probability_distribution
